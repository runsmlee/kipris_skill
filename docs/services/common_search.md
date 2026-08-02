# 공통 (인명 검색·심판 목록)

> ✅ **ServicePath**: `CommonSearchService` (OpenAPI 게이트웨이, `accessKey`)
> 실호출 검증 2026-08-02 — `CommonSearchApplicantInfo?searchName=삼성전자` → `commonSearchPersonInfo` 반환.

출원인·대리인·발명자·창작자·등록권자를 **이름/주소로 검색해 인물번호(`PersonNumber`)를 확보**하는 서비스입니다.
동명이인·법인 표기 흔들림("삼성전자" vs "삼성전자주식회사" vs "삼성전자(중국)연구소")을 정규화할 때 씁니다.
심판 당사자(청구인·피청구인·대리인) 조회와 출원번호별 심판 목록도 여기 있습니다.

- **API 유형**: REST
- **오퍼레이션 수**: 10개

### 호출 예시

```bash
curl -s "https://plus.kipris.or.kr/openapi/rest/CommonSearchService/CommonSearchApplicantInfo?accessKey=${ENCODED_KEY}&searchName=삼성전자&docsStart=1"
```

---

## 출원인 검색
`CommonSearchApplicantInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 특허고객번호/출원인 이름 |  |
| `searchAddress` | 출원인주소 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `commonSearchPersonInfo` |  |  |
| `IndexNumber` | 순번 | (최대출력건수기준:1-30) |
| `PersonNumber` | 대리인번호 |  |
| `Address` | 출원인주소 |  |
| `Name` | 출원인명 | 한글 |
| `EnglishlanguageName` | 출원인명 | 영문 |
| `TotalSearchCount` | 전체건수 |  |

---

## 대리인 검색
`CommonSearchAgentInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 특허고객번호/대리인 이름 |  |
| `searchAddress` | 대리인주소 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `commonSearchPersonInfo` |  |  |
| `IndexNumber` | 순번 | (최대출력건수기준:1-30) |
| `PersonNumber` | 대리인번호 |  |
| `Address` | 대리인주소 |  |
| `Name` | 대리인명 | 한글 |
| `EnglishlanguageName` | 대리인명 | 영문 |
| `TotalSearchCount` | 전체건수 |  |

---

## 발명자 검색
`CommonSearchInventorInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 특허고객번호/발명자 이름 |  |
| `searchAddress` | 발명자주소 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `commonSearchPersonInfo` |  |  |
| `IndexNumber` | 순번 | (최대출력건수기준:1-30) |
| `PersonNumber` | 특허고객번호 |  |
| `Address` | 발명자주소 |  |
| `Name` | 발명자명 | 한글 |
| `EnglishlanguageName` | 발명자명 | 영문 |
| `TotalSearchCount` | 전체건수 |  |

---

## 창작자 검색
`CommonSearchCreatorInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 특허고객번호/창작자 이름 |  |
| `searchAddress` | 창작자주소 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `commonSearchPersonInfo` |  |  |
| `IndexNumber` | 순번 | (최대출력건수기준:1-30) |
| `PersonNumber` | 특허고객번호 |  |
| `Address` | 창작자주소 |  |
| `Name` | 창작자명 | 한글 |
| `EnglishlanguageName` | 창작자명 | 영문 |
| `TotalSearchCount` | 전체건수 |  |

---

## 등록권자 검색
`CommonSearchRegisterInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 특허고객번호/등록권자 이름 |  |
| `searchAddress` | 등록권자주소 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `commonSearchPersonInfo` |  |  |
| `IndexNumber` | 순번 | (최대출력건수기준:1-30) |
| `PersonNumber` | 특허고객번호 |  |
| `Address` | 등록권자주소 |  |
| `Name` | 등록권자명 | 한글 |
| `EnglishlanguageName` | 등록권자명 | 영문 |
| `TotalSearchCount` | 전체건수 |  |

---

## 심판 청구인 조회
`CommonSearchPlaintifftInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 청구인명 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `CommonSearchPlaintifftInfo` |  |  |
| `indexNo` | 순번 | (최대출력건수기준:1-30) |
| `Address` | 청구인주소 |  |
| `name` | 청구인명 |  |
| `trlno` | 심판번호 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 심판 청구대리인 조회
`CommonSearchPlaintiffAgentInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 청구대리인명 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `CommonSearchPlaintiffAgentInfo` |  |  |
| `indexNo` | 순번 | (최대출력건수기준:1-30) |
| `Address` | 청구인주소 |  |
| `name` | 청구인명 |  |
| `trlno` | 심판번호 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 심판 피청구인 조회
`CommonSearchDefendantInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 피청구인명 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `CommonSearchDefendantInfo` |  |  |
| `indexNo` | 순번 | (최대출력건수기준:1-30) |
| `Address` | 청구인주소 |  |
| `name` | 청구인명 |  |
| `trlno` | 심판번호 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 심판 피청구대리인 조회
`CommonSearchDefendantAgentInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchName` | 피청구대리인명 |  |
| `docsStart` | 시작번호 | (전체건수기준) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `CommonSearchDefendantAgentInfo` |  |  |
| `indexNo` | 순번 | (최대출력건수기준:1-30) |
| `Address` | 청구인주소 |  |
| `name` | 청구인명 |  |
| `trlno` | 심판번호 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 심판사항을 제공
`trialListInfo`

- **분류**: 오퍼레이션
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `CommonSearchtrialListInfo` |  |  |
| `trialNumber` | 심판번호 | (숫자) |
| `trialNumberNm` | 심판번호 | (문자) |
| `eventindication` | 사건의표시 |  |
| `trialDecisionDate` | 심결일자 |  |
| `trialRequestDate` | 청구일자 |  |

---

