---
name: kipris
description: 한국특허청(KIPRIS) Open API로 특허, 실용신안, 디자인, 상표, 해외특허 등 한국 지식재산 정보를 검색합니다. 특허 검색, 출원번호 조회, 출원인 검색, 서지정보 확인이 필요할 때 사용합니다.
---

# KIPRIS 한국 지식재산 검색

> **스킬 범위**: 이 스킬은 **검색 도구**이며 코딩/개발 컨텍스트와 무관합니다. 코드를 작성하는 중이 아니어도, 사용자가 특허·지식재산 검색을 요청하면 즉시 이 스킬을 사용합니다.

한국특허청(KIPRIS) Open API를 사용하여 특허, 실용신안, 디자인, 상표, 해외특허 등 한국 지식재산 정보를 검색합니다.

## 트리거

코딩 여부와 관계없이 사용자가 다음과 같은 요청을 할 때 이 스킬을 사용합니다:
- 한국 특허/실용신안 검색 (키워드, 출원번호, 출원인, 등록권자)
- 특허 서지정보 조회 (상세/요약)
- 해외특허 검색 (미국, 유럽, PCT, 일본, 중국 등)
- KIPRIS API를 사용한 지식재산 데이터 조회
- "/kipris" 슬래시 명령으로 직접 호출

## API 키 확인

**필수**: 환경변수 `KIPRIS_API_KEY`가 설정되어 있어야 합니다.

```bash
echo $KIPRIS_API_KEY
```

미설정 시 안내:
1. [KIPRIS Plus](https://plus.kipris.or.kr) 회원가입 → API 키 발급 (OpenAPI 게이트웨이용 `accessKey`)
2. [공공데이터 포털](https://www.data.go.kr) 활용신청 → API 키 발급 (KIPO 게이트웨이용 `ServiceKey`)
3. `export KIPRIS_API_KEY="발급받은키"` 설정

> 두 게이트웨이가 동일 키를 공유할 수도 있고, 별도일 수도 있습니다. 사용자에게 확인하세요.

## 구현된 오퍼레이션 (Tier 1) — 즉시 사용 가능 (16개)

### 한국 특허·실용신안 (7개)

| 오퍼레이션 | ID | 게이트웨이 | 인증키 | ServicePath | 응답 루트 키 | 주요 파라미터 |
|-----------|-----|----------|--------|-------------|------------|-------------|
| 전체검색 | `getAdvancedSearch` | KIPO | `ServiceKey` | `patUtiModInfoSearchSevice` | `response.body.items.item` | `word`, `inventionTitle`, `applicationNumber`, `applicant`, `patent=true`, `utility=true`, `numOfRows`, `pageNo` |
| 자유검색 | `freeSearchInfo` | OpenAPI | `accessKey` | `patUtiModInfoSearchSevice` | `response.body.items.PatentUtilityInfo` | `word`, `patent=true`, `utility=true`, `docsStart`, `docsCount` |
| 출원번호검색 | `applicationNumberSearchInfo` | OpenAPI | `accessKey` | `patUtiModInfoSearchSevice` | `response.body.items.PatentUtilityInfo` | `applicationNumber`, `patent=true`, `utility=true` |
| 출원인검색 | `applicantNameSearchInfo` | OpenAPI | `accessKey` | `patUtiModInfoSearchSevice` | `response.body.items.PatentUtilityInfo` | `applicant`, `patent=true`, `utility=true` |
| 등록권자검색 | `rightHolerSearchInfo` | OpenAPI | `accessKey` | `patUtiModInfoSearchSevice` | `response.body.items.PatentUtilityInfo` | `rightHoler`, `patent=true`, `utility=true` |
| 서지상세 | `getBibliographyDetailInfoSearch` | KIPO | `ServiceKey` | `patUtiModInfoSearchSevice` | `response.body.item` | `applicationNumber` |
| 서지요약 | `getBibliographySumryInfoSearch` | KIPO | `ServiceKey` | `patUtiModInfoSearchSevice` | `response.body.items.item` | `applicationNumber` |

### 해외특허 (9개)

| 오퍼레이션 | ID | 게이트웨이 | 인증키 | ServicePath | 응답 루트 키 | 주요 파라미터 |
|-----------|-----|----------|--------|-------------|------------|-------------|
| 전체검색(항목별) | `advancedSearch` | OpenAPI | `accessKey` | `ForeignPatentAdvencedSearchService` | `response.body.items.searchResult` | `free`, `inventionName`, `applicant`, `inventors`, `agents`, `ipc`, `upc`, `fi`, `fterm`, `epc`, `applicationNo`, `openNo`, `registerNo`, `priorityNo`, `internationalOpenNo`, `internationalApplicationNo`, `applicationdate`, `openDate`, `registerDate`, `priorityDate`, `internationalOpenDate`, `internationalApplicationDate`, `abstracts`, `claimExtend`, `detailsDescription`, `collectionValues`, `currentPage`, `sortField`, `sortState` (전체 31개 필드 → `docs/services/foreign_patent.md`) |
| 서지상세 | `bibliographicInfo` | OpenAPI | `accessKey` | `ForeignPatentBibliographicService` | `response.body.items` | `literatureNumber` (검색 결과의 `ltrtno`), `countryCode` |
| 청구항 | `demandParagraphInfo` | OpenAPI | `accessKey` | `ForeignPatentBibliographicService` | `response.body.items` | `literatureNumber`, `countryCode` |
| 공개전문 경로 | `openFullTextInfo` | OpenAPI | `accessKey` | `ForeignPatentImageAndFullTextService` | `response.body.items.openFullTextInfo.path` | `literatureNumber`, `countryCode` |
| 자유검색 | `freeSearch` | OpenAPI | `accessKey` | `ForeignPatentAdvencedSearchService` | `response.body.items.searchResult` | `free`, `collectionValues` (국가코드), `currentPage` |
| 출원번호 | `applicationNumberSearch` | OpenAPI | `accessKey` | `ForeignPatentAdvencedSearchService` | `response.body.items.searchResult` | `applicationNumber`, `collectionValues`, `currentPage` |
| 국제공개번호 | `internationalOpenNumberSearch` | OpenAPI | `accessKey` | `ForeignPatentAdvencedSearchService` | `response.body.items.searchResult` | `internationalOpenNumber`, `collectionValues`, `currentPage` |
| 출원인 | `applicantSearch` | OpenAPI | `accessKey` | `ForeignPatentAdvencedSearchService` | `response.body.items.searchResult` | `applicant`, `collectionValues`, `currentPage` |
| 국제출원번호 | `internationalApplicationNumberSearch` | OpenAPI | `accessKey` | `ForeignPatentAdvencedSearchService` | `response.body.items.searchResult` | `internationalApplicationNumber`, `collectionValues`, `currentPage` |

### 해외특허 국가코드

`collectionValues` 파라미터 값 (다중 선택 불가):

| 코드 | 국가 | 코드 | 국가 |
|------|------|------|------|
| `US` | 미국 | `JP` | 일본 |
| `EP` | 유럽 | `PJ` | 일본영문초록 |
| `WO` | PCT | `CP` | 중국 |
| `CN` | 중국영문초록 | `TW` | 대만영문초록 |
| `RU` | 러시아 | `CO` | 콜롬비아 |
| `SE` | 스웨덴 | `ES` | 스페인 |
| `IL` | 이스라엘 | | |

## URL 구성 규칙

```
# OpenAPI 게이트웨이 (accessKey)
https://plus.kipris.or.kr/openapi/rest/{ServicePath}/{operationId}?accessKey={KIPRIS_API_KEY}&param1=value1

# KIPO 게이트웨이 (ServiceKey)
https://plus.kipris.or.kr/kipo-api/kipi/{ServicePath}/{operationId}?ServiceKey={KIPRIS_API_KEY}&param1=value1
```

> **⚠️ 반드시 `https://`.** 같은 키·같은 경로라도 `http://`로 호출하면 `resultCode: 30`
> (`SERVICE_KEY_IS_NOT_REGISTERED_ERROR` / `AccessKey Is Not Registerd Error`)이 돌아옵니다.
> 키 미등록으로 오진하기 쉬우니 `rc=30`이 뜨면 프로토콜부터 확인하세요. (실측 검증 2026-08-02)

### 해외 서지·청구항은 2단계 호출

`ForeignPatentBibliographicService`는 출원번호가 아니라 **문헌번호(`ltrtno`)**를 받습니다:

1. `ForeignPatentAdvencedSearchService`로 검색 → 결과의 `ltrtno` 확보 (예: `000012573236B2`)
2. `bibliographicInfo` / `demandParagraphInfo` / `openFullTextInfo`에 `literatureNumber={ltrtno}&countryCode={국가코드}` 전달

`openFullTextInfo`는 데이터가 아니라 **KIPRIS 전문 다운로드 URL**(`path`)을 돌려줍니다.

## API 사용 제한

- **⚠️ 초당 호출 횟수: 반드시 50회 미만 유지** (초과 시 IP 차단)
- **월간 무료 호출**: 1,000회/월 (무료 가입자 기준, 매월 1일 초기화)
- **미신청 API**: 신청하지 않은 API 호출 시 `resultCode: 101` (`AccessKey&ServiceID Is Not Registerd Error`) 등의 에러 반환
- **복합 호출 주의**: 일부 검색(등록권자 검색 등)은 API 설계상 추가 호출이 필요하여 1회 검색에 여러 번 API를 소모합니다. 무료 사용자(월 1,000회)는 호출 횟수가 소중하므로, 복합 호출 전 반드시 사용자에게 안내하고 동의를 구하세요
- 반복 검색이나 페이지네이션 시 요청 간 적절한 간격을 유지할 것

## 실행 워크플로우

> 아래는 Claude가 사용자 검색 요청을 처리하기 위해 내부적으로 수행하는 단계입니다. 사용자는 자연어로 요청만 하면 됩니다.

### 1단계: API 키 확인
```bash
echo $KIPRIS_API_KEY
```

### 2단계: 사용자 의도 → 오퍼레이션 매핑
- 키워드 검색 → `freeSearchInfo` (국내) / `freeSearch` (해외)
- 출원번호로 조회 → `applicationNumberSearchInfo` (국내) / `applicationNumberSearch` (해외)
- 출원인 검색 → `applicantNameSearchInfo` (국내) / `applicantSearch` (해외)
- 등록권자 검색 → `rightHolerSearchInfo` (**⚠️ 아래 "등록권자 검색 주의사항" 참고**)
- 상세 서지정보 → `getBibliographyDetailInfoSearch`
- 요약 서지정보 → `getBibliographySumryInfoSearch`
- 전체검색 (다항목) → `getAdvancedSearch` (국내) / `advancedSearch` (해외, IPC·CPC·F-Term 등 31개 필드)
- 해외 서지상세·청구항·전문 → `bibliographicInfo` / `demandParagraphInfo` / `openFullTextInfo` (**`ltrtno` 선확보 필요 — 위 "2단계 호출" 참고**)
- 출원인·대리인·발명자 이름 정규화, 인물번호 확보 → `CommonSearchService` (`docs/services/common_search.md`)
- 권리 이전·권리자 변경 이력 → `RightHolderService` (**등록번호 기준** — `docs/services/right_holder_history.md`)
- 법적 상태(출원→소멸 전주기) → `legStatusInfoSearchService` (KIPO 게이트웨이·`ServiceKey`) / ST.27·ST.87은 OpenAPI 게이트웨이 별도 경로 — `docs/services/legal_status.md`

### 3단계: URL 구성 및 curl 실행

API 키에 `/`, `+`, `=` 등 특수문자가 포함될 수 있으므로 반드시 URL 인코딩합니다:

```bash
# API 키 URL 인코딩
ENCODED_KEY=$(python3 -c "import urllib.parse; print(urllib.parse.quote('${KIPRIS_API_KEY}', safe=''))")

# 예: 국내 자유검색
curl -s "https://plus.kipris.or.kr/openapi/rest/patUtiModInfoSearchSevice/freeSearchInfo?accessKey=${ENCODED_KEY}&word=인공지능&patent=true&utility=true&docsCount=10&docsStart=1"
```

### 4단계: XML → JSON 파싱
```bash
curl -s "URL" | python3 -c "
import sys, xml.etree.ElementTree as ET, json

def xml_to_dict(el):
    d = {}
    for child in el:
        tag = child.tag
        if len(child):
            val = xml_to_dict(child)
        else:
            val = (child.text or '').strip()
        if tag in d:
            if not isinstance(d[tag], list):
                d[tag] = [d[tag]]
            d[tag].append(val)
        else:
            d[tag] = val
    return d

tree = ET.parse(sys.stdin)
print(json.dumps(xml_to_dict(tree.getroot()), ensure_ascii=False, indent=2))
"
```

### 등록권자 검색 주의사항

`rightHolerSearchInfo`는 등록권자 기준으로 검색하지만, **API 응답에 등록권자 필드가 포함되지 않습니다** (출원인만 반환). 이는 KIPRIS API의 설계 한계입니다.

등록권자를 결과에 표시하려면 2단계 호출이 필요합니다:

1. `rightHolerSearchInfo`로 검색 → 출원번호 목록 획득
2. 각 출원번호로 `registrationLastRightHolderInfo` (등록사항 서비스) 추가 호출 → 최종권리자명 획득

**⚠️ API 호출 횟수 주의**: 이 과정에서 결과 N건을 표시하면 **1 + N회** API를 호출합니다. 무료 사용자는 월 1,000회 제한이 있으므로, 반드시 사용자에게 추가 호출이 발생한다는 점을 사전 안내하고 동의를 구하세요.

예시 안내 문구:
> "등록권자 기준으로 검색합니다. KIPRIS API 제약으로 등록권자명을 표시하려면 결과 건수만큼 추가 API 호출이 필요합니다 (5건 요청 시 총 6회 호출). 진행할까요?"

### 5단계: 결과를 읽기 좋은 테이블 형식으로 사용자에게 제공

국내특허 결과 주요 필드:
- `InventionName` / `inventionTitle` — 발명의명칭
- `ApplicationNumber` / `applicationNumber` — 출원번호
- `ApplicationDate` / `applicationDate` — 출원일자
- `Applicant` / `applicantName` — 출원인
- `RegistrationNumber` / `registerNumber` — 등록번호
- `RegistrationStatus` / `registerStatus` — 등록상태
- `Abstract` / `astrtCont` — 초록

해외특허 결과 주요 필드:
- `inventionName` — 발명(고안)의명칭
- `applicationNo` — 출원번호
- `applicationDate` — 출원일자
- `applicant` — 출원인명
- `registerNo` — 등록번호
- `colString` — 국가코드
- `ipc` — IPC코드

## 전체 서비스 카탈로그 (Tier 2) — 50개 서비스

Tier 1에 없는 오퍼레이션 요청 시, `docs/services/` 디렉토리의 해당 문서를 읽어 파라미터를 확인하세요.
경로 열: ✅ = ServicePath 확인 (즉시 호출 가능), ⚠️ = ServicePath 미확인

| # | 서비스명 | 문서 | 오퍼레이션 | 경로 |
|---|---------|------|-----------|------|
| 1 | 특허·실용 공개·등록공보 | `docs/services/patent_utility.md` | 61 | ✅ |
| 2 | 특허·실용 인용문헌 | `docs/services/patent_citation.md` | 5 | ✅ |
| 3 | 특허·실용 행정처리 이력 | `docs/services/patent_admin_history.md` | 3 | ⚠️ |
| 4 | 특허·실용 분류코드 변동 이력 | `docs/services/patent_classification_history.md` | 3 | ✅ |
| 5 | 디자인 공보 | `docs/services/design.md` | 51 | ✅ |
| 6 | 디자인 행정처리 이력 | `docs/services/design_admin_history.md` | 2 | ⚠️ |
| 7 | 상표 행정처리 이력 | `docs/services/trademark_admin_history.md` | 2 | ⚠️ |
| 8 | 상표 출원 속보 | `docs/services/trademark.md` | 54 | ✅ |
| 9 | 법적 상태 이력 (ST.27/ST.87) | `docs/services/legal_status.md` | 23 | ✅ |
| 10 | 특허·실용 통지서 마감기한 | `docs/services/patent_notice_deadline.md` | 6 | ✅ |
| 11 | 등록사항 | `docs/services/registration.md` | 12 | ✅ |
| 12 | 권리자 변동 이력 | `docs/services/right_holder_history.md` | 8 | ✅ |
| 13 | 분류코드 | `docs/services/classification_code.md` | 8 | ✅ |
| 14 | 심판사항 | `docs/services/trial.md` | 31 | ✅ |
| 15 | 대표 출원인 | `docs/services/representative_applicant.md` | 4 | ✅ |
| 16 | 시소러스 | `docs/services/thesaurus.md` | 2 | ✅ |
| 17 | 한국특허영문초록(KPA) | `docs/services/kpa_english_abstract.md` | 26 | ✅ |
| 18 | 기계번역용 국문초록 | `docs/services/machine_translation_abstract.md` | 1 | ✅ |
| 19 | 해외특허 | `docs/services/foreign_patent.md` | 81 | ✅ |
| 20 | 특허 패밀리 | `docs/services/patent_family.md` | 5 | ✅ |
| 21 | 다인용 선행문헌 | `docs/services/multi_citation.md` | 2 | ⚠️ |
| 22 | 국유특허 | `docs/services/government_patent.md` | 2 | ⚠️ |
| 23 | 특허 기탁 미생물 | `docs/services/patent_microorganism.md` | 4 | ⚠️ |
| 24 | 인터넷 기술공지 | `docs/services/internet_tech_notice.md` | 2 | ⚠️ |
| 25 | 공모전 아이디어 | `docs/services/contest_idea.md` | 1 | ⚠️ |
| 26 | IP-Biz 하나로 서비스 기술분류 | `docs/services/ipbiz_hanaro.md` | 1 | ⚠️ |
| 27 | 디자인맵 형태분류 | `docs/services/design_map.md` | 2 | ⚠️ |
| 28 | 의견제출통지서 | `docs/services/opinion_notice.md` | 12 | ✅ |
| 29 | 거절결정서 | `docs/services/rejection_decision.md` | 12 | ✅ |
| 30 | 정정공보 | `docs/services/amendment_gazette.md` | 24 | ⚠️ |
| 31 | 출원인 법인 | `docs/services/applicant_corporation.md` | 5 | ✅ |
| 32 | 디자인 분류코드 변동 이력 | `docs/services/design_classification_history.md` | 3 | ⚠️ |
| 33 | 상표 분류코드 변동 이력 | `docs/services/trademark_classification_history.md` | 2 | ✅ |
| 34 | 해외디자인 | `docs/services/foreign_design.md` | 31 | ✅ |
| 35 | 해외상표 | `docs/services/foreign_trademark.md` | 22 | ✅ |
| 36 | 출원인 명칭 변동 이력 | `docs/services/applicant_name_history.md` | 3 | ⚠️ |
| 37 | 출원인 기술분야 | `docs/services/applicant_tech_field.md` | 2 | ⚠️ |
| 38 | 등록결정서 | `docs/services/registration_decision.md` | 9 | ⚠️ |
| 39 | 청구항 변동 이력 | `docs/services/claim_history.md` | 3 | ⚠️ |
| 40 | 특허 염기서열 | `docs/services/patent_sequence.md` | 7 | ⚠️ |
| 41 | 특허 합금조성비 | `docs/services/patent_alloy.md` | 2 | ⚠️ |
| 42 | TM5 공통상태 지표 | `docs/services/tm5_indicator.md` | 2 | ⚠️ |
| 43 | 특허·실용 피인용문헌 | `docs/services/patent_cited.md` | 3 | ✅ |
| 44 | 특허권 존속기간 연장등록 공보 | `docs/services/patent_extension.md` | 4 | ⚠️ |
| 45 | 의약품 국제일반명칭 | `docs/services/inn_medicine.md` | 3 | ⚠️ |
| 46 | 상표 원산지 명칭 | `docs/services/trademark_origin.md` | 3 | ⚠️ |
| 47 | 품종보호권 등록 식물 명칭 | `docs/services/variety_protection.md` | 3 | ⚠️ |
| 48 | 일본 특허 합금조성비 | `docs/services/japan_patent_alloy.md` | 5 | ⚠️ |
| 49 | 특허 중한 코퍼스 | `docs/services/patent_cn_kr_corpus.md` | 1 | ⚠️ |
| 50 | 공통 (인명 검색·심판 목록) | `docs/services/common_search.md` | 10 | ✅ |

## 사용 예시

### 예시 1: 키워드로 국내 특허 검색
> "인공지능 관련 특허를 검색해줘"

→ `freeSearchInfo` 사용, `word=인공지능&patent=true&utility=true`

### 예시 2: 출원번호로 상세정보 조회
> "출원번호 1020200123456의 상세 서지정보를 알려줘"

→ `getBibliographyDetailInfoSearch` 사용, `applicationNumber=1020200123456`

### 예시 3: 특정 회사의 특허 검색
> "삼성전자가 출원한 특허를 찾아줘"

→ `applicantNameSearchInfo` 사용, `applicant=삼성전자&patent=true&utility=true`

### 예시 4: 미국 특허 검색
> "artificial intelligence 관련 미국 특허를 검색해줘"

→ `freeSearch` 사용, `free=artificial+intelligence&collectionValues=US`

### 예시 5: 등록권자로 검색
> "LG에너지솔루션이 보유한 등록특허를 찾아줘"

→ `rightHolerSearchInfo` 사용, `rightHoler=LG에너지솔루션&patent=true&utility=true`

## 에러 처리

### API 키 미설정
`KIPRIS_API_KEY` 환경변수가 비어있으면 사용자에게 키 발급 방법을 안내합니다.

### 서버 오류 / 빈 응답
- HTTP 오류 시 상태 코드 확인 후 재시도 안내
- XML 파싱 실패 시 원본 응답 일부를 사용자에게 보여주고 진단
- `resultCode`가 `00`이 아닌 경우 `resultMsg` 확인

### 미구현 오퍼레이션 요청
Tier 1 테이블에 없는 서비스 요청 시:
1. Tier 2 카탈로그에서 해당 서비스 문서 경로 확인
2. `docs/services/{file}.md`를 읽어 오퍼레이션 ID, 파라미터, 응답 구조 파악
3. **ServicePath가 미확인 상태**일 수 있음을 사용자에게 안내
4. 확인된 정보로 URL을 구성하여 시도

### 공통 파라미터 참고
- 페이징: OpenAPI 계열은 `docsStart`/`docsCount`, KIPO 계열은 `pageNo`/`numOfRows`
- 정렬: `sortSpec`(또는 `sortField`) + `descSort`(또는 `sortState`)
- 행정처분 필터: `lastvalue` (공백=전체, A=공개, R=등록, J=거절 등)
