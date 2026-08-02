# 해외디자인

> ✅ **ServicePath**: `ForeignDesignAdvencedSearchService` (OpenAPI 게이트웨이, `accessKey`)
> 실호출 검증 2026-08-02 — `advancedSearch` 결과 반환.
>
> ```bash
> curl -s "https://plus.kipris.or.kr/openapi/rest/ForeignDesignAdvencedSearchService/advancedSearch?accessKey=${ENCODED_KEY}&free=chair&collectionValues=US&currentPage=1"
> ```

- **API 유형**: REST
- **오퍼레이션 수**: 31개 (구현: 0, 폐기예정: 0)

---

## 전체검색
`advancedSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `free` | 자유검색 | (전문)KW |
| `articleName` | 물품명칭 | IT |
| `applicationNo` | 출원번호 | AN |
| `pubNo` | 공고번호 | PN |
| `registerNo` | 등록번호 | RN |
| `priorityNo` | 우선권주장번호 | PRN |
| `applicationdate` | 출원일자 | AD |
| `pubDate` | 공고일자 | PD |
| `registerDate` | 등록일자 | RD |
| `priorityDate` | 우선권주장일자 | PRD |
| `applicant` | 출원인명 | AP |
| `creator` | 창작자명 | IV |
| `agents` | 대리인명 | AG |
| `rightHolder` | 권리자명 | RG |
| `designMainClassification` | 디자인분류 | DC |
| `locarnoCode` | 로카르노분류 | LC |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortState` | 정렬방식 | (true,false) |
| `sortField` | 정렬기준 |  |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 | 한글 |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 자유검색
`freeSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `free` | 자유검색 | (전문) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 대리인검색
`agentsSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `agents` | 대리인명 | AG |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 출원인검색
`applicantSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicant` | 출원인명 | (출원인) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 출원일자검색
`applicationdateSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationdate` | 출원일자 | (출원일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 출원번호검색
`applicationNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 | (출원번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 물품명칭검색
`articleNameSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `articleName` | 물품명칭 | (물품명칭) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 창작자검색
`creatorSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `creator` | 창작자명 | IV |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 한국분류검색
`designMainClassificationSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `designMainClassification` | 한국분류 | (한국분류) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 국제분류검색
`locarnoSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `locarnoCode` | 국제분류 | (국제분류) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 우선권주장일자검색
`priorityDateSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityDateSearch` | 우선권주장일자 | (우선권주장일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 공고일자검색
`publicationDateSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `publicationDateSearch` | 공고일자 | (공고일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 우선권주장번호검색
`priorityNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityNo` | 우선권주장번호 | (우선권주장번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 공고번호검색
`publicationNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `pubNo` | 공고번호 | (공고번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 등록일자검색
`registerDateSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registerDateSearch` | 등록일자 | (등록일자검색) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 등록번호검색
`registerNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registerNo` | 등록번호 | (등록번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 권리자검색
`rightHolderSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `rightHolder` | 권리자 | RG |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (US-미국, JP-일본, CN-중국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationDate` | 출원일자 |  |
| `applicationNo` | 출원번호 |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭 |  |
| `countryCode` | 국가코드 |  |
| `creator` | 창작자명 |  |
| `designMainClassification` | 디자인분류 |  |
| `designSeq` | 디자인일련번호 |  |
| `locarnoCode` | 로카르노분류 |  |
| `ltrtno` | 문헌번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `priorityNo` | 우선권주장번호 |  |
| `pubDate` | 공고일자 |  |
| `pubNo` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNo` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `thumbnailPath` | 작은이미지경로 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 전체조회
`searchAllInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchAllInfoList` |  |  |
| `foreignDesingInfoList` |  |  |
| `foreignDesignInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `publicNumber` | 공고번호 |  |
| `publicDate` | 공고일자 |  |
| `registrationNumber` | 등록번호 |  |
| `registrationDate` | 등록일자 |  |
| `creatContent` | 창작내용 |  |
| `creatFunction` | 창작기능 |  |
| `creatSummary` | 창작요약 |  |
| `foreignDesignDetailInfoList` |  |  |
| `foreignDesignDetailInfo` |  |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭(국문) |  |
| `designMainClassification` | 디자인주분류 |  |
| `designSubClassification` | 디자인부분류 |  |
| `cgdesignClassification` | 화상디자인분류 |  |
| `priorityInfoList` |  |  |
| `priorityInfo` |  |  |
| `prioritySequence` | 순번 |  |
| `priorityNumber` | 우선권주장번호 |  |
| `priorityDate` | 우선권주장일자 |  |
| `locarnoCodeInfoList` |  |  |
| `locarnoCodeInfo` |  |  |
| `locarnoSequence` | 순번 |  |
| `locarnoCode` | 로카르노코드 |  |
| `dTermInfoList` |  |  |
| `dTermInfo` |  |  |
| `dTermSequence` | 순번 |  |
| `dTerm` | D-Term |  |
| `applicantInfoList` |  |  |
| `applicantInfo` |  |  |
| `sequence` | 순번 |  |
| `applicant` | 출원인명 |  |
| `address` | 주소 |  |
| `agentsInfoList` |  |  |
| `agentInfo` |  |  |
| `sequence` | 순번 |  |
| `agent` | 대리인명 |  |
| `address` | 주소 |  |
| `creatorInfoList` |  |  |
| `creatorInfo` |  |  |
| `sequence` | 순번 |  |
| `creator` | 창작자명 |  |
| `address` | 주소 |  |
| `rightHolderInfoList` |  |  |
| `rightHolderInfo` |  |  |
| `sequence` | 순번 |  |
| `rightholder` | 권리자명 |  |
| `address` | 주소 |  |

---

## 국외디자인
`foreignDesignInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `foreignDesignInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `publicNumber` | 공고번호 |  |
| `publicDate` | 공고일자 |  |
| `registrationNumber` | 등록번호 |  |
| `registrationDate` | 등록일자 |  |
| `creatContent` | 창작내용 |  |
| `creatFunction` | 창작기능 |  |
| `creatSummary` | 창작요약 |  |

---

## 국외디자인상세
`foreignDesignDetailInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `foreignDesignDetailInfo` |  |  |
| `articleName` | 물품명칭 |  |
| `articleNameKR` | 물품명칭(국문) |  |
| `designMainClassification` | 디자인주분류 |  |
| `designSubClassification` | 디자인부분류 |  |
| `cgdesignClassification` | 화상디자인분류 |  |

---

## 우선권주장
`priorityInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityInfo` |  |  |
| `prioritySequence` | 순번 |  |
| `priorityNumber` | 우선권주장번호 |  |
| `priorityDate` | 우선권주장일자 |  |

---

## 국제분류
`locarnoCodeInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `locarnoCodeInfo` |  |  |
| `locarnoSequence` | 순번 |  |
| `locarnoCode` | 로카르노코드 |  |

---

## DTERM
`dTermInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `dTermInfo` |  |  |
| `dTermSequence` | 순번 |  |
| `dTerm` | D-Term |  |

---

## 출원인
`applicantInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicantInfo` |  |  |
| `sequence` | 순번 |  |
| `applicant` | 출원인명 |  |
| `address` | 주소 |  |

---

## 대리인
`agentInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `agentInfo` |  |  |
| `sequence` | 순번 |  |
| `agent` | 대리인명 |  |
| `address` | 주소 |  |

---

## 창작자
`creatorInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `creatorInfo` |  |  |
| `sequence` | 순번 |  |
| `creator` | 창작자명 |  |
| `address` | 주소 |  |

---

## 권리자
`rightHolderInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `rightHolderInfo` |  |  |
| `sequence` | 순번 |  |
| `rightholder` | 권리자명 |  |
| `address` | 주소 |  |

---

## 디자인이미지
`designImageInfo`

- **분류**: 도면/전문
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `designImageInfo` |  |  |
| `imageName` | 이미지명 |  |
| `imagePath` | 이미지경로 |  |

---

## 디자인썸네일
`designThumbnail`

- **분류**: 도면/전문
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (US-미국, JP-일본, CN-중국) ※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `designThumbnailInfo` |  |  |
| `thumbnailName` | 작은이미지명 |  |
| `thumbnailPath` | 작은이미지경로 |  |

---

## 변동정보
`transferListInfo`

- **분류**: 부가기능
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `kind` | 검색코드 | (oper1 : 전체조회, oper2 : 국외디자인, oper3 : 국외디자인상세, oper4 : 우선권주장, oper5 : 국제분류, oper6 : DTERM, oper7 : 출원인, oper8 : 대리인, oper9 : 창작자, oper10 : 권리자) ※ oper1, oper2, oper3, oper4, oper5, oper6, oper7, oper8, oper9, oper10 중 원하는 변동정보 검색코드 입력 |
| `countryCode` | 국가코드 | (US : 미국, JP : 일본, CN : 중국)※다중 국가 선택 불가, 입력방식(ex : US) |
| `transferDate` | 변동일자 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `transferListInfo` |  |  |
| `transferCount` | 변동건수 |  |
| `transferList` | 문헌번호 리스트 | (ex : 문헌번호1&#124;문헌번호2&#124;...) |

---

## 최종변동일자

- **분류**: 부가기능
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `countryCode` | 국가코드 | (US : 미국, JP : 일본, CN : 중국)※다중 국가 선택 불가, 입력방식(ex : US) |
| `literatureNumber` | 문헌번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `lastTransferDateInfo` | 최종변동일자 |  |

---