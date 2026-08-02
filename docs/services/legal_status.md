# 법적 상태 이력 (특허·실용 ST.27, 상표, 디자인 ST.87)

> ✅ **ServicePath 3종 — KIPRIS Plus 포털에서 확인 + 실호출 검증 (2026-08-02)**
> 하나의 서비스처럼 보이지만 **경로도 게이트웨이도 다른 3개 그룹**입니다.

| 그룹 | ServicePath | 게이트웨이 | 인증키 | 우리 키 상태 |
|------|-------------|-----------|--------|-------------|
| 법적 상태 이력 (기본 5종) | `legStatusInfoSearchService` | KIPO (`/kipo-api/kipi/`) | `ServiceKey` | ✅ `rc=00` 정상 |
| 특허·실용 ST.27 (10종) | `legStatusST27InfoSearchService` | OpenAPI (`/openapi/rest/`) | `accessKey` | ⚠️ `rc=31` 구독 만료 |
| 디자인 ST.87 (8종) | `legStatusST87InfoSearchService` | OpenAPI (`/openapi/rest/`) | `accessKey` | ⚠️ `rc=31` 구독 만료 |

> **ST.27/ST.87은 경로가 유효한데 우리 키가 구독 만료 상태**입니다 (`rc=31 DEADLINE_HAS_EXPIRED_ERROR`).
> 무효 경로는 302를, 유효 경로는 200을 반환하므로 이 둘은 구분됩니다 — 경로 문제가 아니라 **KIPRIS Plus 활용신청/갱신** 문제입니다.

### 호출 예시

```bash
# 기본 이력 (KIPO 게이트웨이 — 현재 사용 가능)
curl -s "https://plus.kipris.or.kr/kipo-api/kipi/legStatusInfoSearchService/getLegStatusHistoryInfoSearch?ServiceKey=${ENCODED_KEY}&applicationNumber=1020188870000"

# ST.27 이력 (OpenAPI 게이트웨이 — 구독 갱신 후 사용 가능)
curl -s "https://plus.kipris.or.kr/openapi/rest/legStatusST27InfoSearchService/BasicInfo?accessKey=${ENCODED_KEY}&applicationNumber=1020188870000&supplySerialNumber=1"
```

---

## 그룹 1 — 법적 상태 이력 (KIPO 게이트웨이, `legStatusInfoSearchService`)

오퍼레이션 ID는 포털에 명시되어 있습니다.

| 오퍼레이션 | ID | 상태 |
|-----------|-----|------|
| 이력정보조회 | `getLegStatusHistoryInfoSearch` | ✅ `rc=00` 실측 |
| 이벤트정보조회 | `getLegStatusEventInfoSearch` | ✅ `rc=00` 실측 |
| 변동정보 | `getTransferListInfoSearch` | 포털 확인 |
| 현재정보조회 | `legalStatusBasicInfo` | 포털 확인 |
| 코드정보조회 | `legalStatusCodeInfo` | 포털 확인 |

## 그룹 2 — 특허·실용 ST.27 (`legStatusST27InfoSearchService`)

> 포털이 오퍼레이션 ID를 공개하지 않아 **실호출 탐침으로 확인**했습니다 (200 = 유효, 302 = 무효).
> 한글 오퍼레이션명 ↔ ID 대응은 응답 루트 키(`legalStatusST27AppInfo` 등) 기준 **추론**입니다.

| 한글 오퍼레이션명 | ID (실측 유효) |
|------------------|---------------|
| 이력 정보 조회 | `BasicInfo` |
| 출원(A) 이벤트 정보 조회 | `AppInfo` |
| 등록전·후심리(E·L·W) 이벤트 정보 조회 | `RegInfo` |
| IP권리존속기간이후의보호(G) 이벤트 정보 조회 | `AfterRightInfo` |
| IP권리중단(H) 이벤트 정보 조회 | `StopRightInfo` |
| 문서수정(P) 이벤트 정보 조회 | `DocInfo` |
| 납부(U) 이벤트 정보 조회 | `PayInfo` |
| 심판(V) 이벤트 정보 조회 | `TrialInfo` |
| 변동정보 | `transferListInfo` |
| 출원(A) 관련 추가이벤트(원출원등록) 정보 조회 | ❓ 미발견 |

## 그룹 3 — 디자인 ST.87 (`legStatusST87InfoSearchService`)

포털 기준 8종, 실호출 탐침으로 8종 전부 유효 확인:
`BasicInfo`, `AppInfo`, `RegInfo`, `StopRightInfo`, `TrialInfo`, `PayInfo`, `DocInfo`, `TransferListInfo`

> ST.87은 KIPRIS Plus 공식 입출력 CSV에 없어 파라미터 명세가 없습니다. ST.27과 동일하게
> `applicationNumber` + `supplySerialNumber`를 받는 것으로 보이나 미검증입니다.

---

## 오퍼레이션별 파라미터 명세

### 이력정보조회
`getLegStatusHistoryInfoSearch`

- **분류**: 법적 상태 이력

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusBasicInfo` |  |  |
| `appReferenceNumber` | 출원참조번호 |  |
| `applicationNumber` | 출원번호 |  |
| `legalStatusCode` | 법적상태코드 |  |
| `legalStatusName` | 법적상태명 | 한글 |
| `legalStatusEngName` | 법적상태명 | 영문 |
| `legalStatusDate` | 법적상태일자 |  |
| `legalStatusComment` | 법적상태설명 | 한글 |
| `legalStatusEngComment` | 법적상태설명 | 영문 |

---

### 이벤트정보조회
`getLegStatusEventInfoSearch`

- **분류**: 법적 상태 이력

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `Item` |  |  |
| `applicationNumber` | 출원번호 |  |
| `appReferenceNumber` | 출원참조번호 |  |
| `seq` | 일련번호 |  |
| `legalStatusCode` | 법정상태코드 |  |
| `legalStatusName` | 법적상태명 |  |
| `legalStatusDate` | 법적상태일자 |  |
| `legalStatusComment` | 법적상태설명 |  |

---

### 현재정보조회
`legalStatusBasicInfo`

- **분류**: 법적 상태 이력

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `kind` | 검색코드 | (oper1 : 이력정보조회, oper2 : 이벤트정보조회) ※ oper1, oper2 중 원하는 변동정보 검색코드 입력 |
| `searchRight` | 권리 | (all : 전체, p : 특허, u : 실용신안, d : 디자인, t : 상표) ※입력방식(ex : p) |
| `transferDate` | 변동일자 | ※ 입력방식(ex : 20160713) |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `transferListInfo` |  |  |
| `transferCount` | 변동건수 |  |
| `transferList` | 출원번호리스트 | (ex : 출원번호1|출원번호2) |

---

### 코드정보조회
`legalStatusCodeInfo`

- **분류**: 법적 상태 이력

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `legalStatusCode` | 법적상태코드 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusCodeInfo` |  |  |
| `legalStatusCode` | 법적상태코드 |  |
| `legalStatusName` | 법적상태명 |  |
| `legalStatusComment` | 법적상태설명 | 한글 |
| `legalStatusEngName` | 법적상태명 | (영문) |
| `legalStatusEngComment` | 법적상태설명 | (영문) |

---

### 이력 정보 조회
`BasicInfo`

- **분류**: 특허·실용(ST.27)

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27Info` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `rightTypeCode` | 권리구분 |  |
| `applicationDate` | 출원일자 |  |
| `openNumber` | 공개번호 |  |
| `openingDate` | 공개일자 |  |
| `registrationNumber` | 등록번호 |  |
| `registrationDate` | 등록일자 |  |
| `publicationNumber` | 공고번호 |  |
| `publicationDate` | 공고일자 |  |
| `trialNumber` | 심판번호 |  |
| `demurrerNumber` | 이의신청번호 |  |
| `keyEventCode` | 주요이벤트코드 |  |
| `detailedEventCode` | 상세법이벤트코드 |  |
| `stateCode` | 법이벤트상태코드 |  |
| `previousStageCode` | 법이벤트전단계코드 |  |
| `currentStageCode` | 법이벤트후단계코드 |  |
| `eventIndicatorCode` | 법이벤트표시코드 |  |
| `nationalEventCode` | 법진행상태코드 |  |
| `eventDate` | 법이벤트일자 |  |

---

### 출원(A) 이벤트 정보 조회
`AppInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27AppInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `internationalApplicationNumber` | 국제출원번호 |  |
| `internationalApplicationDate` | 국제출원일자 |  |

---

### 등록전·후심리(E·L·W) 이벤트 정보 조회
`RegInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27RegInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `demurrerNumber` | 이의신청번호 |  |
| `oppositionDate` | 이의신청일자 |  |
| `oppositionObject` | 이의신청취지 |  |
| `oppositionMatters` | 이의신청사항 |  |
| `registrationNumber` | 등록번호 |  |
| `oppositionCancellationClauseContent` | 이의신청취소항내용 |  |

---

### IP권리존속기간이후의보호(G) 이벤트 정보 조회
`AfterRightInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27AfterRightInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `extensionTargetdemandItemCount` | 연장대상청구항수 |  |
| `extensionTargetPetitionClauseScopeContent` | 연장대상청구항범위내용 |  |
| `extensiontermDate` | 연장기간일 |  |
| `extensiontermMonth` | 연장기간월 |  |
| `extensiontermYear` | 연장기간년 |  |
| `permissionRegistrationContent` | 허가등록내용 |  |

---

### IP권리중단(H) 이벤트 정보 조회
`StopRightInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27StopRightInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `terminationRegistrationCauseDate` | 소멸등록원인일자 |  |
| `terminationRegistrationCauseName` | 소멸등록원인명 |  |

---

### 문서수정(P) 이벤트 정보 조회
`DocInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27DocInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `extensionTerminationDate` | 공고제목 |  |
| `internetOpeningPublicDate` | 공개공고일자 |  |
| `openingPublicationNumber` | 인터넷공개공고일자 |  |
| `openingPublicDate` | 공개공고번호 |  |

---

### 납부(U) 이벤트 정보 조회
`PayInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27PayInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `startAnnual` | 시작연차 |  |
| `terminationRegistrationCauseDate` | 소멸등록원인일자 |  |
| `terminationRegistrationCauseName` | 소멸등록원인명 |  |

---

### 심판(V) 이벤트 정보 조회
`TrialInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 일련번호 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusST27TrialInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `supplySerialNumber` | 보급일련번호 |  |
| `trialTypeCode` | 심판구분 |  |
| `trialNumber` | 심판번호 |  |
| `trialGradeTypeCode` | 심급구분 |  |
| `requestForPatentTrialDate` | 심판청구일자 |  |
| `trialDecisionDate` | 심결일자 |  |
| `trialDecisionPrincipleClauseContent` | 심결주문내용 |  |
| `eventIndicationContent` | 사건표시내용 |  |

---

### 변동정보
`transferListInfo`

- **분류**: 오퍼레이션

**요청 (IN)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchType` | 검색코드 | D-이력, A-출원 E-등록전·후심리, G-IP권리존속기간이후, H-IP권리중단, P-문서수정, U-납부, V-심판 |
| `transferDate` | 변동일자 |  |

**응답 (OUT)**

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `transferListInfo` |  |  |
| `transferCount` | 변동건수 |  |
| `transferList` | 출원번호리스트 | (ex : 출원번호1|출원번호2) |

---

