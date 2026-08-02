# 해외특허

- **API 유형**: REST
- **오퍼레이션 수**: 81개 (구현: 5, 폐기예정: 15)
- **서비스 경로**: `ForeignPatentAdvencedSearchService` (검증됨), `ForeignPatentGeneralSearchService` (미검증)
- **게이트웨이**: OpenAPI (`/openapi/rest/`)
- **인증 키**: `accessKey`
- **공통 응답 루트 키**: `response.body.items.searchResult`

---

## 단어(폐기예정)
`wordSearch`

- **분류**: 일반검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchWord` | 검색단어 |  |
| `searchWordRange` | 검색기간 |  |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 번호(폐기예정)
`numberSearch`

- **분류**: 일반검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchNumber` | 검색번호 |  |
| `searchNumberKind` | 검색번호종류 |  |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 전체검색
`advancedSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `abstracts` | 초록 | AB |
| `agents` | 대리인명 | AG |
| `applicant` | 출원인명 | AP |
| `applicationNo` | 출원번호 | AN |
| `applicationdate` | 출원일자 | AD |
| `claimExtend` | 청구범위 | CL |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |
| `currentPage` | 페이지번호 |  |
| `detailsDescription` | 상세설명 | DC |
| `epc` | EPC코드 | EC |
| `fi` | FI코드 | FI |
| `free` | 자유검색 | KW |
| `fterm` | F-TERM코드 | FT |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `internationalOpenNo` | 국제공개번호 | ION |
| `inventionName` | 발명(고안)의명칭 | TL |
| `inventors` | 발명자명 | IN |
| `ipc` | IPC코드 | IPC |
| `openDate` | 공개일자 | OD |
| `openNo` | 공개번호 | OPN |
| `otherRef` | - | 미사용 |
| `priorityDate` | 우선권주장일자 | RD |
| `priorityNo` | 우선권주장번호 | RN |
| `registerDate` | 등록일자 | GD |
| `registerNo` | 등록번호 | GN |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `upc` | UPC코드 | CLAS |
| `usPatentDocument` | U.S.PatentDocument | UR |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 자유검색
`freeSearch`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `ForeignPatentFreeSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/ForeignPatentAdvencedSearchService/freeSearch`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.searchResult`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `free` | 자유검색 | (자유) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## IPC
`ipcSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ipc` | IPC코드 | (ipc) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## USCD
`upcSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `upc` | UPC코드 | CLAS |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## FI
`fiSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fi` | FI코드 | (fi) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## F-Term
`ftermSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fterm` | F-TERM코드 | (fterm) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## EPC
`epcSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `epc` | EPC코드 | (epc) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 발명의명칭
`inventionNameSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `invention` | 발명의명칭 | (발명의 명칭) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 초록정보
`abstractSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `abstracts` | 초록 | (초록) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 청구범위
`claimExtendSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `claimExtend` | 청구범위 | (청구범위) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## US Patent Document(폐기예정)
`usPatentDocumentSearch`

- **분류**: 항목별검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `usPatentDocument` | usPatentDocument | (US patent Document) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 출원번호
`applicationNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `ForeignPatentApplicationNumberSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/ForeignPatentAdvencedSearchService/applicationNumberSearch`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.searchResult`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 | (출원번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 공개번호
`openNumberSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openNumber` | 공개번호 | (공개번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 등록번호
`registerNumberSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registerNumber` | 등록번호 | (등록번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 우선권번호
`priorityNumberSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityNumber` | 우선권번호 | (우선권번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 국제공개번호
`internationalOpenNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `ForeignPatentInternationalOpenNumberSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/ForeignPatentAdvencedSearchService/internationalOpenNumberSearch`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.searchResult`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationalOpenNumber` | 국제공개번호 | (국제공개번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## ForeignRef 번호(폐기예정)
`foreignRefNumberSearch`

- **분류**: 항목별검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `foreignRefNumber` | ForeignRef번호 | (foreignRef 번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 필드(폐기예정)
`fieldSearch`

- **분류**: 항목별검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `field` | field | (field) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 출원일자
`applicationdateSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationdate` | 출원일자 | (출원일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 공개일자
`openDateSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openDate` | 공개일자 | (공개일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 등록일자
`registerDateSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registerDate` | 등록일자 | (등록일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 우선권일자
`priorityDateSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityDate` | 우선권주장일자 | (우선권일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 출원인
`applicantSearch`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `ForeignPatentApplicantSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/ForeignPatentAdvencedSearchService/applicantSearch`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.searchResult`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicant` | 출원인명 | (출원인) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 발명자
`inventorsSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `inventors` | 발명자명 | (발명자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 대리인
`agentsSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `agents` | 대리인명 | (대리인) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 국제출원번호
`internationalApplicationNumberSearch`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `ForeignPatentInternationalApplicationNumberSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/ForeignPatentAdvencedSearchService/internationalApplicationNumberSearch`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.searchResult`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationalApplicationNumber` | 국제출원번호 | (국제출원번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## Relation US Search(폐기예정)
`relationUSSearch`

- **분류**: 항목별검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `relationUS` | RelationUS | (relationUS) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 국제출원일자
`internationalApplicationDateSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationalApplicationDate` | 국제출원일자 | (국제출원일자) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 항목별검색상세
`detailsDescriptionSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `detailsDescription` | 상세설명 | (상세설명) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## CPC 검색
`cpcSearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `cpc` | CPC코드 | (cpc) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자), OPD(공개일자), GD(등록일자), PD(공보일자), IDT(국제출원일자), IOD(국제공개일자), RD(우선권주장일자) |
| `sortState` | 정렬방식 | (true-desc, false-asc) |
| `collectionValues` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `totalSearchCount` | 전체건수 |  |
| `colString` | 국가코드 |  |

---

## 우선권주장국가
`priorityCountrySearch`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityCountrySearch` | 우선권번호 | (우선권번호) |
| `currentPage` | 페이지번호 |  |
| `sortField` | 정렬기준 | AD(출원일자) OPD(공개일자) GD(등록일자) PD(공보일자) IDT(국제출원일자) IOD(국제공개일자) RD(우선권주장일자) |
| `sortState` | 정렬방식 | 내림정렬 (true-desc false-asc) |
| `collectionValues` | 국가코드 | (미국-US 유럽-EP PCT-WO 일본-JP 일본영문초록-PJ 중국-CP 중국특허영문초록-CN 대만영문초록-TW |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `searchResult` |  |  |
| `ltrtno` | 문헌번호 |  |
| `ipc` | IPC코드 | IPC |
| `upc` | UPC코드 | CLAS |
| `fi` | FI코드 | FI |
| `fterm` | F-TERM코드 | FT |
| `epc` | EPC코드 | EC |
| `applicationNo` | 출원번호 | AN |
| `registerNo` | 등록번호 | GN |
| `publishrNo` | 공보번호 | PN |
| `priorityNo` | 우선권주장번호 | (RNV) |
| `internationalOpenNo` | 국제공개번호 | ION |
| `familyNo` | 패밀리번호 | (FMV) |
| `applicationDate` | 출원일자 | AD |
| `openDate` | 공개일자 | (ODV) |
| `registerDate` | 등록일자 | GD |
| `priorityDate` | 우선권주장일자 | (RND) |
| `internationalOpenDate` | 국제공개일자 | IOD |
| `applicant` | 출원인명 | AP |
| `inventors` | 발명자명 | IN |
| `agents` | 대리인명 | AG |
| `internationalApplicationNo` | 국제출원번호 | IAN |
| `internationalApplicationDate` | 국제출원일자 | IDT |
| `vdkVgwKey` | 국가코드/문헌번호/조회순번 |  |
| `openNumber` | 공개번호 | OPN |
| `inventionName` | 발명 | (고안)의명칭 |
| `colString` | 국가코드 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 서지상세정보
`bibliographicInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `bibliographicInfo` |  |  |
| `bibliographicSummaryInfo` |  |  |
| `countryCode` | 국가매체코드 |  |
| `ltrtNo` | 문헌번호 |  |
| `inventionTitle` | 발명의 명칭 |  |
| `usKind` | 상태 |  |
| `usNo` | 등록번호/등록일자/공개번호/공개일자 |  |
| `patTpcd` | 국외문헌식별코드 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `openNumber` | 공개번호 |  |
| `openDate` | 공개일자 |  |
| `publicationNumber` | 공보번호 |  |
| `repubFg` | 정정공보유무 |  |
| `publishDate` | 공보일자 |  |
| `imageStandardCode` | 대표도면출처상태코드 |  |
| `pubFg` | 공고공보유무 |  |
| `ipcInfo` |  |  |
| `ipcCd` | IPC코드 |  |
| `ipcVersion` | IPC버전 |  |
| `fiInfo` |  |  |
| `publKey` | 순번 |  |
| `clssCd` | FI코드 |  |
| `ftermInfo` |  |  |
| `ftermCode` | F-TERM코드 |  |
| `themeCodeInfo` |  |  |
| `temaCode` | F_TERM주제코드 |  |
| `summation` |  |  |
| `astrtCont` | 요약 |  |
| `openNumberInfo` |  |  |
| `openNumber` | 공개번호/공개일자 |  |
| `applicantInfo` |  |  |
| `applicantName` | 출원인명 |  |
| `applicantAddress` | 출원인주소 |  |
| `applicantCountry` | 출원인국가 |  |
| `inventorsInfo` |  |  |
| `inventorName` | 발명자명 |  |
| `inventorAddress` | 발명자주소 |  |
| `inventorCountry` | 발명자국가 |  |
| `priorityNumberDateInfo` |  |  |
| `priorityApplicationNumber` | 우선권주장번호 |  |
| `priorityApplicationDate` | 우선권주장일자 |  |
| `priorityApplicationCountry` | 우선권국가코드 |  |
| `docdbFamilyInfo` |  |  |
| `docdbLiteratureNumber` | DOCDB문헌번호 |  |
| `docdbCountryCode` | DOCDB국가코드 |  |
| `epodocPublicNumber` | EPODOC공보번호 |  |
| `docdbLiteratureIdCode` | DOCDB문헌식별코드 |  |
| `foreignBiblio` |  |  |
| `publKey` | DOCDB문헌번호 |  |
| `ipcVersionInfo` |  |  |
| `versionDate` | IPC버전/IPC개정일자 | IPC8판 적용일자 |
| `upcInfo` |  |  |
| `upcUspdCd` | UPC코드 |  |
| `getfield` |  |  |
| `clssCd` | 코드내역 |  |
| `agentInfo` |  |  |
| `agentAddr` | 대리인주소 |  |
| `agentName` | 대리인명 |  |
| `judgesInfo` |  |  |
| `seq` | 고유번호 |  |
| `kind` | 심사관종류 |  |
| `name` | 심사관명 |  |
| `internationalApplicationOpenInfo` |  |  |
| `internationalApplicationNumber` | 국제출원번호 |  |
| `internationalApplicationDate` | 국제출원일자 |  |
| `internationPublicationNumber` | 국제공개번호 |  |
| `internationPublicationDate` | 국제공개일자 |  |
| `publKey` | 문헌번호 |  |
| `demandParagraphInfo` |  |  |
| `claimText` | 청구범위내용 |  |
| `usPatentDocumentsInfo` |  |  |
| `corgPatno` | 외국참조번호 |  |
| `patTpcd` | 국외문헌식별코드 |  |
| `exam` | 심사관인용여부 |  |
| `patDt` | 공보일자 |  |
| `name` | 심사관명 |  |
| `clssCd` | 코드내역 |  |
| `ltrtnoLink` | 재구성공고번호등록 |  |
| `cntryCodeLink` | 국가코드 링크 |  |
| `foreignPatentDocumentsInfo` |  |  |
| `corgPatno` | 외국참조번호 |  |
| `patTpcd` | 국외문헌식별코드 |  |
| `exam` | 심사관인용여부 |  |
| `patDt` | 공보일자 |  |
| `countryCode` | 국가매체코드 |  |
| `clssCd` | 코드내역 |  |
| `otherPublicationsInfo` |  |  |
| `data` | 외국참조번호 |  |
| `relatedUsApplicationDataInfo` |  | 해당 정보는 미국만 제공 |
| `patno` | 공보번호 |  |
| `patDt` | 공보일자 |  |
| `kind` | 출원종류 |  |
| `stcd` | 상태코드 |  |
| `relatedUsApplicationDataDetailInfo` |  | 해당 정보는 미국만 제공 |
| `patno` | 공보번호 |  |
| `patDt` | 공보일자 |  |
| `kind` | 출원종류 |  |
| `stcd` | 상태코드 |  |
| `ltrtnoLink` | 재구성공고번호등록 |  |
| `actionStatus` | 관련출원 코드설명 |  |
| `openAnnounceNumberInfo` |  |  |
| `openAnnounceNumber` | 공개번호/공개일자 |  |
| `eclaInfo` |  |  |
| `clssCd` | 코드내역 |  |
| `designationInfo` |  |  |
| `nationalNameKR` | 지정국가명(한글) |  |
| `nationalNameCode` | 지정국가코드 |  |
| `representationImageInfo` |  |  |
| `tifPath` | tif 경로 |  |
| `jpgPath` | jpg 경로 |  |
| `cpcInfo` |  |  |
| `cpcCd` | CPC코드 |  |

---

## 서지요약정보
`bibliographicSummaryInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `bibliographicSummaryInfo` |  |  |
| `countryCode` | 국가매체코드 |  |
| `ltrtNo` | 문헌번호 |  |
| `inventionTitle` | 발명의명칭 |  |
| `usKind` | 번호종류 |  |
| `usNo` | 등록번호/등록일자/공개번호/공개일자 |  |
| `patTpcd` | 국외문헌식별코드 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `openNumber` | 공개번호 |  |
| `openDate` | 공개일자 |  |
| `publicationNumber` | 공보번호 |  |
| `publishDate` | 공보일자 |  |
| `imageStandardCode` | 대표도면출처상태코드 |  |
| `pubFg` | 공고공보유무 |  |
| `repubFg` | 정정공보유무 |  |

---

## IPC
`ipcInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ipcInfo` |  |  |
| `ipcCd` | IPC코드 |  |
| `ipcVersion` | IPC버전 |  |

---

## FI(일본)
`fiInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fiInfo` |  |  |
| `publKey` | 순번 |  |
| `clssCd` | FI코드 |  |

---

## F-Term(일본)
`ftermInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ftermInfo` |  |  |
| `ftermCode` | F-TERM코드 |  |

---

## Theme코드(일본)
`themeCodeInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `themeCodeInfo` |  |  |
| `temaCode` | F_TERM주제코드 |  |

---

## 초록
`summation`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `summation` |  |  |
| `astrtCont` | 요약 |  |

---

## 공개번호(폐기예정)
`openNumberInfo`

- **분류**: 서지정보
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openNumberInfo` |  |  |
| `openNumber` | 공개번호/공개일자 |  |

---

## 출원인
`applicantInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicantInfo` |  |  |
| `applicantName` | 출원인명 |  |
| `applicantAddress` | 출원인주소 |  |
| `applicantCountry` | 출원인국가 |  |

---

## 발명자
`inventorsInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `inventorsInfo` |  |  |
| `inventorName` | 발명자명 |  |
| `inventorAddress` | 발명자주소 |  |
| `inventorCountry` | 발명자국가 |  |

---

## 우선권번호,일자
`prriorityNumberDateInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityNumberDateInfo` |  |  |
| `priorityApplicationNumber` | 우선권주장번호 |  |
| `priorityApplicationDate` | 우선권주장일자 |  |
| `priorityApplicationCountry` | 우선권주장국가코드 |  |

---

## DOC,패밀리(폐기예정)
`docdbFamilyInfo`

- **분류**: 서지정보
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `docdbFamilyInfo` |  |  |
| `docdbLiteratureNumber` | DOCDB문헌번호 |  |
| `docdbCountryCode` | DOCDB국가코드 |  |
| `epodocPublicNumber` | EPODOC공보번호 |  |
| `docdbLiteratureIdCode` | DOCDB문헌식별코드 |  |

---

## 해외 서지(폐기예정)
`foreignBiblio`

- **분류**: 서지정보
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `foreignBiblio` |  |  |
| `publKey` | DOCDB문헌번호 |  |

---

## IPC버전(폐기예정)
`ipcVersionInfo`

- **분류**: 서지정보
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ipcVersionInfo` |  |  |
| `versionDate` | IPC버전/IPC개정일자 | IPC8판 적용일자 |

---

## USCD
`upcInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `upcInfo` |  |  |
| `upcUspdCd` | UPC코드 |  |

---

## Field of Search
`getfield`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `getfield` |  |  |
| `clssCd` | 검색항목 |  |

---

## 대리인
`agentInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `agentInfo` |  |  |
| `agentAddr` | 대리인주소 |  |
| `agentName` | 대리인명 |  |

---

## 국제출원/공개 번호,일자 정보
`internationalApplicationOpenInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationalApplicationOpenInfo` |  |  |
| `internationalApplicationNumber` | 국제출원번호 |  |
| `internationalApplicationDate` | 국제출원일자 |  |
| `internationPublicationNumber` | 국제공개번호 |  |
| `internationPublicationDate` | 국제공개일자 |  |
| `publKey` | 문헌번호 |  |

---

## 청구항
`demandParagraphInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL)※다중 국가 선택 불가, PCT 조회 제한 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `demandParagraphInfo` |  |  |
| `claimText` | 청구범위내용 |  |

---

## 인용(자국 문헌)
`usPatentDocumentsInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `usPatentDocumentsInfo` |  |  |
| `corgPatno` | 외국참조번호 |  |
| `patTpcd` | 보고서종류 |  |
| `exam` | 심사관인용여부 |  |
| `patDt` | 공보일자 |  |
| `name` | 출원인명 |  |
| `clssCd` | UPC코드 |  |
| `ltrtnoLink` | 재구성공고번호등록 |  |
| `cntryCodeLink` | 국가코드링크 |  |

---

## 인용(타국 문헌)
`foreignPatentDocumentsInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `foreignPatentDocumentsInfo` |  |  |
| `corgPatno` | 외국참조번호 |  |
| `patTpcd` | 보고서종류 |  |
| `exam` | 심사관인용여부 |  |
| `patDt` | 공보일자 |  |
| `countryCode` | 국가코드 |  |
| `clssCd` | UPC코드 |  |

---

## 인용(Other Publication)
`otherPublicationsInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `otherPublicationsInfo` |  |  |
| `data` | 외국참조번호 |  |

---

## Related US Application Data
`relatedUsApplicationDataInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `relatedUsApplicationDataInfo` |  |  |
| `patno` | 공보번호 |  |
| `patDt` | 공보일자 |  |
| `kind` | 출원종류 |  |
| `stcd` | 상태코드 |  |
| `ltrtnoLink` | 관련출원번호링크 |  |

---

## Relation출원상세(폐기예정)
`relatedUsApplicationDataDetailInfo`

- **분류**: 서지정보
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `relatedUsApplicationDataDetailInfo` |  |  |
| `patno` | 공보번호 |  |
| `patDt` | 공보일자 |  |
| `kind` | 출원종류 |  |
| `stcd` | 상태코드 |  |
| `ltrtnoLink` | 관련출원번호링크 |  |
| `actionStatus` | 관련출원코드설명 |  |

---

## 공개,공고번호(폐기예정)
`getOpenAnnounceNumber`

- **분류**: 서지정보
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openAnnounceNumberInfo` |  |  |
| `openAnnounceNumber` | 공개번호/공개일자 |  |

---

## ECLA
`eclaInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `eclaInfo` |  |  |
| `clssCd` | 구분코드 |  |

---

## 지정국
`designationInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `designationInfo` |  |  |
| `nationalNameKR` | 지정국가명 | 한글 |
| `nationalNameCode` | 지정국가코드 |  |

---

## CPC
`cpcInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `cpcInfo` |  |  |
| `cpcCd` | CPC코드 |  |

---

## 패밀리정보(DOCDB 패밀리 정보 포함)
`familyInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `familyInfo` |  |  |
| `applicationDate` | 출원일자 |  |
| `applicationNumber` | 출원번호 |  |
| `countryCode` | 국가코드 |  |
| `countryName` | 국가명 |  |
| `familyKind` | 패밀리종류 |  |
| `familyNumber` | 패밀리번호 |  |
| `literatureCode` | 문헌코드 |  |
| `applicationDate` | 출원일자 |  |
| `literatureNumber` | 문헌번호 |  |
| `openingDate` | 공개일자 |  |
| `openingNumber` | 공개번호 |  |
| `gazetteDate` | 공보일자 |  |
| `gazetteNumber` | 공보번호 |  |
| `registrationNumber` | 등록번호 |  |
| `inventionName` | 발명의명칭 |  |

---

## 전문(폐기예정)
`fullTextInfo`

- **분류**: 도면/전문
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fullTextInfo` |  |  |
| `path` | 파일경로 |  |

---

## 대표도
`representationImageInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `representationImageInfo` |  |  |
| `tifPath` | - | (미사용) |
| `tifFileName` | - | (미사용) |
| `jpgPath` | 이미지경로 |  |
| `jpgFileName` | 이미지명 |  |

---

## 정정공고(폐기예정)
`revisionAnnounceInfo`

- **분류**: 도면/전문
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `revisionAnnounceInfo` |  |  |
| `path` | 파일경로 |  |

---

## 공개전문
`openFullTextInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openFullTextInfo` |  |  |
| `path` | 파일경로 |  |

---

## 공고전문
`registrationFullTextInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registrationFullTextInfo` |  |  |
| `path` | 파일경로 |  |

---

## 정정정보(폐기예정)
`revisionInfo`

- **분류**: 도면/전문
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `revisionInfo` |  |  |
| `repubFg` | 정정정보유무 |  |

---

## 전문정보출력
`fullTextDisplayInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fullTextDisplayInfo` |  |  |
| `openNumber` | 공개전문번호 |  |
| `registerNumber` | 공고전문번호 |  |
| `revisionNumber` | - | (미사용) |

---

## 공개번호링크
`openNumberLinkInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openNumberLinkInfo` |  |  |
| `no` | 번호 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 등록번호링크
`registrationNumberLinkInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registrationNumberLinkInfo` |  |  |
| `no` | 번호 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 모든 전문 및 대표도 유무
`fullTextCheck`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `literatureNumber` | 문헌번호 |  |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fullTextCheckResult` |  |  |
| `openFullTextCheckResult` | 공개전문유무 | (있음:Y,없음:N) |
| `registrationFullTextCheckResult` | 공고전문유무 | (있음:Y,없음:N) |
| `representationImageInfo` | 대표도면유무 | (있음:Y,없음:N) |
| `revisionAnnounceFullTextCheckResult` | - | 미사용 |

---

## IPC코드
`getIpcCode`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ipcCd` | IPC코드 | (IPC) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchCodeResult` |  |  |
| `section` | IPC코드 | (출력용) |
| `koreanExplanation` | 한글설명 |  |
| `originalTextExplanation` | 원문설명 |  |

---

## EPC코드
`getEpcCode`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `epcCode` | EPC코드 | (EPC) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchCodeResult` |  |  |
| `section` | EPC코드 |  |
| `koreanExplanation` | 한글설명 |  |
| `originalTextExplanation` | 원문설명 |  |

---

## UPC코드
`getUpcCode`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `upcUspdCd` | UPC코드 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchCodeResult` |  |  |
| `section` | UPC코드 | (출력용) |
| `koreanExplanation` | 한글설명 |  |
| `originalTextExplanation` | 원문설명 |  |

---

## FI코드
`getFiCode`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `fiCode` | FI코드 | (FI) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchCodeResult` |  |  |
| `section` | FI코드 | (출력용) |
| `koreanExplanation` | 한글설명 |  |
| `originalTextExplanation` | 원문설명 |  |

---

## F-TERM 코드
`getFtermCode`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ftermCode` | F-TREM코드 | (F-TERM) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchCodeResult` |  |  |
| `section` | F-TERM코드 |  |
| `koreanExplanation` | 한글설명 |  |
| `originalTextExplanation` | 원문설명 |  |

---

## 문헌번호(LTRTNO)조회
`getLtrtno`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |
| `applicationNumber` | 출원번호 | (OR?조건) |
| `openNumber` | 공개번호 | (OR?조건) |
| `registNumber` | 등록번호 | (OR?조건) |
| `publicationNumber` | 공보번호 | (OR?조건) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `LtrtnoInfo` |  |  |
| `ltrtno` | 문헌번호 | (LTRTNO) |

---

## CPC코드
`getCpcCode`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `cpcCd` | CPC코드 | (CPC) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchCodeResult` |  |  |
| `section` | CPC코드 | (출력용) |
| `koreanExplanation` | 한글설명 |  |
| `originalTextExplanation` | 원문설명 |  |

---

## 변동정보
`transferListInfo`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `kind` | 검색코드 | (oper1 : 서지상세정보, oper2 : 서지요약정보, oper3 : IPC, oper4 : FI(일본), oper5 : F-Term(일본), oper6 : Theme코드(일본), oper7 : 초록, oper9 : 출원인, oper10 : 발명자, oper11 : 우선권번호·일자, oper15 : USCD, oper16 : Field of Search, oper17 : 대리인, oper18 : 국제출원/공개 번호,일자 정보, oper19 : 청구항, oper20 : 인용(자국 문헌), oper21 : 인용(타국 문헌), oper22 : 인용(Ohter Publication), oper23 : Related US Application Data, oper26 : ECLA, oper27 : 지정국, oper28 : CPC, oper29 : 패밀리정보(DOCDB 패밀리정보 포함)) ※ oper1, oper2, oper3, oper4, oper5, oper6, oper7, oper9, oper10, oper11, oper15, oper16, oper17, oper18, oper19, oper20, oper21, oper22, oper23, oper26, oper27, oper28, oper29 중 원하는 변동정보 검색코드 입력 |
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |
| `transferDate` | 변동일자 | ※ 입력방식(ex : 20160713) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `transferListInfo` |  |  |
| `transferCount` | 전체건수 |  |
| `transferList` | 문헌번호 리스트 | (ex : 문헌번호1&#124;문헌번호2&#124;...) |

---

## 최종변동일자

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `countryCode` | 국가코드 | (미국-US, 유럽-EP, PCT-WO, 일본-JP, 일본영문초록-PJ, 중국-CP, 중국특허영문초록-CN, 대만영문초록-TW, 러시아-RU, 콜롬비아-CO, 스웨덴-SE, 스페인-ES, 이스라엘-IL, 인도-IN, 베트남-VN)※다중 국가 선택 불가 |
| `literatureNumber` | 문헌번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `lastTransferDateInfo` | 최종변동일자 |  |

---
