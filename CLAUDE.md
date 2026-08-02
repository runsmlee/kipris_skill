# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

KIPRIS Plus Open API를 활용한 **한국 지식재산 검색 Claude Code Skill** 저장소. 한국 특허청(KIPRIS)의 49개 서비스 API 명세를 문서화하고, `/kipris` 스킬로 실시간 검색을 수행합니다.

## 파일 역할

| 파일 | 역할 |
|------|------|
| `SKILL.md` | 스킬 본체 — 오퍼레이션 매핑, URL 구성, XML 파싱, 실행 워크플로우 |
| `docs/README.md` | API 명세 인덱스 — 49개 서비스 목록, 공통 호출 정보 |
| `docs/services/*.md` | 서비스별 상세 명세 (49개 파일) — 오퍼레이션별 IN/OUT 파라미터 |
| `CLAUDE.md` | 이 파일 — 프로젝트 컨텍스트 |

## API 아키텍처

### 두 가지 게이트웨이

| 게이트웨이 | URL 패턴 | 인증 키 |
|-----------|---------|---------|
| OpenAPI (패턴 A) | `https://plus.kipris.or.kr/openapi/rest/{ServicePath}/{operation}` | `accessKey` (KIPRIS Plus 발급) |
| KIPO API (패턴 B) | `https://plus.kipris.or.kr/kipo-api/kipi/{ServicePath}/{operation}` | `ServiceKey` (공공데이터 포털 발급) |

동일 서비스라도 오퍼레이션에 따라 게이트웨이가 다를 수 있음. 각 오퍼레이션 문서의 Endpoint를 반드시 확인할 것.

### 응답 형식

- XML 응답 → JSON 변환 후 파싱
- 응답 데이터 루트 키가 오퍼레이션마다 다름 (예: `response.body.items.PatentUtilityInfo` vs `response.body.items.item`)

### 확인된 서비스 경로 (24개)

#### API 키로 검증 완료 (2개)

| 서비스 | ServicePath | 게이트웨이 |
|--------|-------------|-----------|
| 특허·실용 공개·등록공보 | `patUtiModInfoSearchSevice` | A + B |
| 해외특허 (고급검색) | `ForeignPatentAdvencedSearchService` | A |

#### 포털 크롤링 확인 (15개)

| 서비스 | ServicePath | 게이트웨이 | DBII |
|--------|-------------|-----------|------|
| 특허·실용 인용문헌 | `CitationService` | A | 004 |
| 특허 관련 문서 | `RelatedDocsonfilePatService` | A | 005 |
| 특허·실용 분류코드 변동 이력 | `PatentClassificationInfoService` | A | 007 |
| 디자인 공보 | `designInfoSearchService` | B | 008 |
| 디자인 관련 문서 | `RelatedDocsonfileDGService` | A | 009 |
| 상표 관련 문서 | `RelatedDocsonfileTMService` | A | 011 |
| 상표 출원 속보 | `trademarkInfoSearchService` | B | 012 |
| 특허·실용 통지서 마감기한 | `DueDateService` | A | 014 |
| 등록사항 | `RegistrationService` | A | 015 |
| 분류코드 | `ClassificationService` | A | 017 |
| 심판사항 | `judgmentInfoSearchService` | B | 019 |
| 대표 출원인 | `RpstApplicantService` | A | 020 |
| 시소러스 | `ThesaurusInfoService` | A | 021 |
| 한국특허영문초록(KPA) | `KpaGeneralSearchService` | A | 024 |
| 기계번역용 국문초록 | `KorAbstractInfoService` | A | 025 |

#### GitHub 코드 검색 확인 — 미검증 (7개)

| 서비스 | ServicePath | 게이트웨이 (추정) |
|--------|-------------|-----------------|
| 해외특허 (일반검색) | `ForeignPatentGeneralSearchService` | A |
| 특허·실용 피인용문헌 | `CitingService` | A |
| 특허 패밀리 | `patFamInfoSearchService` | B |
| 출원인 법인 | `CorpBsApplicantService` | A |
| 의견제출통지서 | `IntermediateDocumentOPService` | A |
| 거절결정서 | `IntermediateDocumentREService` | A |
| 상표 분류코드 | `TradeMarkClassificationInfoService` | A |

> 게이트웨이: A = OpenAPI (`/openapi/rest/`), B = KIPO API (`/kipo-api/kipi/`)
> "미검증" 경로는 GitHub 공개 코드에서 추출. API 키로 실제 호출 검증 필요.

### 서비스 지원 현황

| 상태 | 서비스 수 | 설명 |
|------|-----------|------|
| ServicePath 확인 | **20개** | 스킬에서 호출 가능 |
| ServicePath 미확인 | **29개** | 포털에 API 있으나 경로 미확인 |
| 포털 미등록 (삭제됨) | 3개 | common, patent_right_transfer, patent_legal_status_st27 |

## 구현 현황

12개 오퍼레이션이 Tier 1으로 즉시 사용 가능 (SKILL.md 참조):
- **특허·실용 (7개)**: `getAdvancedSearch`, `freeSearchInfo`, `applicationNumberSearchInfo`, `applicantNameSearchInfo`, `rightHolerSearchInfo`, `getBibliographyDetailInfoSearch`, `getBibliographySumryInfoSearch`
- **해외특허 (5개)**: `freeSearch`, `applicationNumberSearch`, `internationalOpenNumberSearch`, `applicantSearch`, `internationalApplicationNumberSearch`

ServicePath가 확인된 20개 서비스의 오퍼레이션은 `docs/services/` 문서를 참조하여 동적으로 호출 가능.

## 환경 변수

- `KIPRIS_API_KEY` — API 인증 키

## 스킬 설치

설치 방법은 `README.md`를 참조하세요.
