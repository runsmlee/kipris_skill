# 해외상표

> ✅ **ServicePath**: `ForeignTradeMarkAdvencedSearchService` (OpenAPI 게이트웨이, `accessKey`)
> 실호출 검증 2026-08-02 — `advancedSearch` 결과 반환.
>
> ```bash
> curl -s "https://plus.kipris.or.kr/openapi/rest/ForeignTradeMarkAdvencedSearchService/advancedSearch?accessKey=${ENCODED_KEY}&free=apple&collectionValues=US&currentPage=1"
> ```

- **API 유형**: REST
- **오퍼레이션 수**: 22개 (구현: 0, 폐기예정: 0)

---

## 전체검색
`advancedSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `free` | 자유검색 | KW |
| `applicant` | 출원인명 | AP |
| `applicationDate` | 출원일자 | OAD |
| `applicationNumber` | 출원번호 | AN |
| `registrationDate` | 등록일자 | RN |
| `registrationNumber` | 등록번호 | ORN |
| `rightHolder` | 권리자명 | RG |
| `niceCode` | 니스코드 | NC |
| `tradeMarkClassificationCode` | 상품분류코드 | OI |
| `viennaCode` | 도형분류코드 | VC |
| `tradeMarkName` | 상표명칭 | FTN |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `sortField` | 정렬기준 |  |
| `collectionValues` | 국가코드 | (JP-일본,US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
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
| `free` | 자유검색 |  |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 상표명칭검색
`tradeMarkNameSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `tradeMarkName` | 상표명칭 | FTN |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
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
| `applicationNumber` | 출원번호 | AN |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 출원일자검색
`applicationDateSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationdate` | 출원일자 | OAD |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 등록번호검색
`registrationNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registrationNumber` | 등록번호 | RN |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 등록일자검색
`registrationDateSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registrationDate` | 등록일자 | ORD |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
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
| `applicant` | 출원인명 | AP |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
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
| `rightHolder` | 권리자명 | RG |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 상품분류검색
`tradeMarkClassificationCodeSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `tradeMarkClassificationCode` | 상품분류코드 | OD |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 니스코드검색
`niceCodeSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `niceCode` | 니스코드 | NC |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 도형분류코드검색
`viennaCodeSearch`

- **분류**: 항목별검색
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `viennaCode` | 동형분류코드 | VC |
| `currentPage` | 페이지번호 |  |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortField` | 정렬기준 |  |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (JP-일본, US-미국) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `applicant` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `imagePath` | 이미지경로 |  |
| `ltrtno` | 문헌번호 |  |
| `niceCode` | 니스코드 |  |
| `registrationDate` | 등록일자 |  |
| `registrationNumber` | 등록번호 |  |
| `rightHolder` | 권리자명 |  |
| `tradeMarkClassificationCode` | 상품분류코드 |  |
| `tradeMarkName` | 상표명칭 |  |
| `tradeMarkType` |  |  |
| `viennaCode` | 도형분류코드 |  |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 전체조회
`searchAllInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchAllInfoList` |  |  |
| `foreignTradeMarkInfoList` |  |  |
| `foreignTradeMarkInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `registrationNumber` | 등록번호 |  |
| `registrationDate` | 등록일자 |  |
| `registartionStatusInfo` | 등록상태 |  |
| `trademarkPronunciation` | 상표발음명 |  |
| `trademarkDescription` | 상표설명 |  |
| `applicantInfo` |  |  |
| `seq` | 순번 |  |
| `applicantName` | 출원인명 |  |
| `representationApplicantYN` | 대표출원인여부 |  |
| `rightHolderInfo` |  |  |
| `seq` | 순번 |  |
| `rightHolderName` | 권리자명 |  |
| `classificationCodeInfo` |  |  |
| `code` | 상품분류코드 |  |
| `languageCode` | 언어코드 |  |
| `classOfGoodServiceBusinessName` | 지정상품명 |  |
| `niceCodeInfo` |  |  |
| `code` | 니스코드 |  |
| `viennaCodeInfo` |  |  |
| `code` | 도형분류코드 |  |
| `applicantInfoList` |  |  |
| `rightHolderInfoList` |  |  |
| `classificationCodeInfoList` |  |  |
| `niceCodeInfoList` |  |  |
| `viennaCodeInfoList` |  |  |

---

## 국외상표
`foreignTradeMarkInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `foreignTradeMarkInfo` |  |  |
| `applicationNumber` | 자국출원번호 |  |
| `applicationDate` | 자국출원일자 |  |
| `registrationNumber` | 자국등록번호 |  |
| `registrationDate` | 자국등록일자 |  |
| `registrationStatusInfo` | 자국등록상태정보 |  |
| `tradeMarkPronunciation` | 상표발음명 |  |
| `tradeMarkDescription` | 상표설명 |  |

---

## 출원인
`applicantInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationInfo` |  |  |
| `seq` | 순번 |  |
| `applicantName` | 출원인명 |  |
| `representationApplicantYN` | 대표출원인여부 |  |

---

## 권리자
`rightHolderInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `rightHolderInfo` |  |  |
| `seq` | 순번 |  |
| `rightHolderName` | 권리자명 |  |

---

## 상품분류
`classificationCodeInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `classificationCodeInfo` |  |  |
| `code` | 상품분류코드 |  |
| `languageCode` | 언어코드 |  |
| `classOfGoodServiceBusinessName` | 지정상품명 |  |

---

## 니스코드
`niceCodeInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `niceCodeInfo` |  |  |
| `code` | 니스코드 |  |

---

## 도형분류코드
`viennaCodeInfo`

- **분류**: 서지정보
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `viennaCodeInfo` |  |  |
| `code` | 도형분류코드 |  |

---

## 상표이미지
`tradeMarkImageInfo`

- **분류**: 도면/전문
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (JP-일본, US-미국)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `tradeMarkImageInfo` |  |  |
| `imageName` | 이미지명 |  |
| `imagePath` | 이미지경로 |  |

---

## 변동정보
`transferListInfo`

- **분류**: 부가기능
- **상태**: ✅ 경로 확인 (호출 가능)

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `kind` | 검색코드 | (oper1 : 전체조회, oper2 : 국외상표, oper3 : 출원인, oper4 : 권리자, oper5 : 상품분류, oper6 : 니스코드, oper7 : 도형분류코드) ※ oper1, oper2, oper3, oper4, oper5, oper6, oper7 중 원하는 변동정보 검색코드 입력 |
| `countryCode` | 국가코드 | 국가코드(US : 미국, JP : 일본)※다중 국가 선택 불가, 입력방식(ex : US) |
| `transferDate` | 변동일자 | ※ 입력방식(ex : 20160713) |

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
| `countryCode` | 국가코드 | 국가코드(US : 미국, JP : 일본)※다중 국가 선택 불가, 입력방식(ex : US) |
| `literatureNumber` | 문헌번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `lastTransferDateInfo` | 최종변동일자 |  |

---