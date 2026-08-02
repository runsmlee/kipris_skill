# 특허·실용 공개·등록공보

- **API 유형**: REST
- **오퍼레이션 수**: 61개 (구현: 7, 폐기예정: 3)
- **서비스 경로**: `patUtiModInfoSearchSevice`
- **게이트웨이**: OpenAPI (`/openapi/rest/`) + KIPO API (`/kipo-api/kipi/`) — 오퍼레이션별 상이
- **참고**: `accessKey` 또는 `ServiceKey` — 각 오퍼레이션의 Endpoint 참조

---

## 단어(폐기예정)
`getWordSearch`

- **분류**: 일반검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `word` | 검색단어 |  |
| `year` | 검색년도범위 | (0 ~ 10) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `numOfRows` | 페이지당건수 | (기본 : 30, 최대 500) |
| `pageNo` | 페이지번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `indexNo` | 일련번호 |  |
| `registerStatus` | 등록상태 |  |
| `inventionTitle` | 발명의명칭 | 한글 |
| `ipcNumber` | IPC코드 |  |
| `registerNumber` | 등록번호 |  |
| `registerDate` | 등록일자 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `openNumber` | 공개번호 |  |
| `openDate` | 공개일자 |  |
| `publicationNumber` | 공고번호 |  |
| `publicationDate` | 공고일자 |  |
| `astrtCont` | 초록 |  |
| `drawing` | 이미지경로 |  |
| `bigDrawing` | 큰이미지경로 |  |
| `applicantName` | 출원인명 |  |
| `count` |  |  |
| `numOfRows` | 페이지당건수 | (기본 : 30, 최대 500) |
| `pageNo` | 페이지번호 |  |
| `totalCount` | 전체건수 |  |

---

## 번호(폐기예정)
`getNumberSearch`

- **분류**: 일반검색
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `number` | 번호 | (within 7 digits) |
| `year` | 검색년도범위 |  |
| `kind` | 특실구분 | (10 : 특허, 20 : 실용신안) |
| `right` | 권리구분 | (뒷 번호 '0000'은 제외하고 입력) (G : 등록번호, P : 공고번호, R : 공개번호, A : 출원번호) |
| `pageNo` | 페이지번호 | (검색 페이지 번호) |
| `numOfRows` | 페이지당건수 | (기본 : 30, 최대 500) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `item` |  |  |
| `applicantName` | 출원인명 |  |
| `openDate` | 공개일자 |  |
| `openNumber` | 공개번호 |  |
| `publicationNumber` | 공고번호 |  |
| `publicationDate` | 공고일자 |  |
| `registerDate` | 등록일자 |  |
| `registerNumber` | 등록번호 |  |
| `registerStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `bigDrawing` | 큰이미지경로 |  |
| `drawing` | 이미지경로 |  |
| `indexNo` | 일련번호 |  |
| `inventionTitle` | 발명의명칭 | 한글 |
| `ipcNumber` | IPC코드 |  |
| `count` |  |  |
| `numOfRows` |  |  |
| `pageNo` | 페이지번호 | (검색 페이지 번호) |
| `totalCount` | 전체건수 |  |

---

## 전체검색
`getAdvancedSearch`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `KoreanPatentSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/kipo-api/kipi/patUtiModInfoSearchSevice/getAdvancedSearch`
- **인증 키**: `ServiceKey` (공공데이터 포털)
- **응답 루트 키**: `response.body.items.item`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `word` | 자유검색 |  |
| `inventionTitle` | 발명의명칭 |  |
| `astrtCont` | 초록 |  |
| `claimScope` | 청구범위 |  |
| `ipcNumber` | IPC코드 |  |
| `applicationNumber` | 출원번호 |  |
| `openNumber` | 공개번호 |  |
| `publicationNumber` | 공보(고)번호 |  |
| `registerNumber` | 등록번호 |  |
| `priorityApplicationNumber` | 우선권주장번호 |  |
| `internationalApplicationNumber` | 국제출원번호 |  |
| `internationOpenNumber` | 국제공개번호 |  |
| `applicationDate` | 출원일자 |  |
| `openDate` | 공개일자 |  |
| `publicationDate` | 공고일자 |  |
| `registerDate` | 등록일자 |  |
| `priorityApplicationDate` | 우선권주장일자 |  |
| `internationalApplicationDate` | 국제출원일자 |  |
| `internationOpenDate` | 국제공개일자 |  |
| `applicant` | 출원인명/특허고객번호 | 출원인명 및 특허고객번호 |
| `inventors` | 발명자명/특허고객번호 | 발명자명 및 특허고객번호 |
| `agent` | 대리인명/대리인코드 | 대리인명 및 대리인코드 |
| `rightHoler` | 등록권자 | (특허권자) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `pageNo` | 페이지번호 |  |
| `numOfRows` | 페이지당건수 | (기본 : 30, 최대 500) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `indexNo` | 일련번호 |  |
| `registerStatus` | 등록상태 |  |
| `inventionTitle` | 발명의명칭 | 한글 |
| `ipcNumber` | IPC코드 |  |
| `registerNumber` | 등록번호 |  |
| `registerDate` | 등록일자 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `openNumber` | 공개번호 |  |
| `openDate` | 공개일자 |  |
| `publicationNumber` | 공고번호 |  |
| `publicationDate` | 공고일자 |  |
| `astrtCont` | 초록 |  |
| `drawing` | 이미지경로 |  |
| `bigDrawing` | 큰이미지경로 |  |
| `applicantName` | 출원인 |  |
| `count` |  |  |
| `numOfRows` | 페이지당건수 | (기본 : 30, 최대 500) |
| `pageNo` | 페이지번호 |  |
| `totalCount` | 전체건수 |  |

---

## 자유검색
`freeSearchInfo`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `KoreanPatentFreeSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/patUtiModInfoSearchSevice/freeSearchInfo`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.PatentUtilityInfo`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `word` | 자유검색 |  |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `TotalSearchCount` | 전체건수 |  |
| `SearchStartNumber` | 페이지번호 |  |
| `PatentUtilityInfo` |  |  |
| `SerialNumber` | 일련번호 |  |
| `ApplicationNumber` | 출원번호 |  |
| `ApplicationDate` | 출원일 |  |
| `OpeningNumber` | 공개번호 |  |
| `OpeningDate` | 공개일자 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationDate` | 등록일자 |  |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `InventionName` | 발명의명칭 |  |
| `Abstract` | 초록 |  |
| `Applicant` | 출원인 |  |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `RegistrationStatus` | 등록상태 |  |

---

## 출원번호 검색
`applicationNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `KoreanPatentApplicationNumberSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/patUtiModInfoSearchSevice/applicationNumberSearchInfo`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.PatentUtilityInfo`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `TotalSearchCount` | 전체건수 |  |
| `SearchStartNumber` | 페이지번호 |  |
| `PatentUtilityInfo` |  |  |
| `SerialNumber` | 일련번호 |  |
| `ApplicationNumber` | 출원번호 |  |
| `ApplicationDate` | 출원일 |  |
| `OpeningNumber` | 공개번호 |  |
| `OpeningDate` | 공개일자 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationDate` | 등록일자 |  |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `InventionName` | 발명의명칭 |  |
| `Abstract` | 초록 |  |
| `Applicant` | 출원인 |  |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `RegistrationStatus` | 등록상태 |  |

---

## CPC 검색
`cpcSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `cpcNumber` | CPC코드 |  |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `TotalSearchCount` | 전체건수 |  |
| `SearchStartNumber` | 페이지번호 |  |
| `PatentUtilityInfo` |  |  |
| `SerialNumber` | 일련번호 |  |
| `ApplicationNumber` | 출원번호 |  |
| `ApplicationDate` | 출원일 |  |
| `OpeningNumber` | 공개번호 |  |
| `OpeningDate` | 공개일자 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationDate` | 등록일자 |  |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `InventionName` | 발명의명칭 |  |
| `Abstract` | 초록 |  |
| `Applicant` | 출원인 |  |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `RegistrationStatus` | 등록상태 |  |

---

## 발명의명칭
`itemTLSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `inventionTitle` | 발명의명칭 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 초록
`itemABSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `astrtCont` | 초록 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 청구범위
`itemCLSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `claimScope` | 청구범위 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## IPC
`ipcSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ipcNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 공개번호
`openNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openNumber` | 공개번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 공고번호
`publicationNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `publicationNumber` | 공고번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 등록번호
`registrationNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registerNumber` | 등록번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 우선권주장번호
`priorityNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityApplicationNumber` | 우선권주장번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 국제출원번호
`internationalApplicationNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationalApplicationNumber` | 국제출원번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 국제공개번호
`internationalOpenNumberSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationOpenNumber` | 국제공개번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 출원일자
`applicationDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationDate` | 출원일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 공개일자
`openDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `openDate` | 공개일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 공고일자
`publicationDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `publicationDate` | 공고일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 등록일자
`registrationDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `registerDate` | 등록일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 우선권주장일자
`priorityDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `priorityApplicationDate` | 우선권주장일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 국제출원일자
`internationalApplicationDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationalApplicationDate` | 국제출원일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 국제공개일자
`internationalOpenDateSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `internationOpenDate` | 국제공개일자 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 출원인정보
`applicantNameSearchInfo`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `KoreanPatentApplicantSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/patUtiModInfoSearchSevice/applicantNameSearchInfo`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.PatentUtilityInfo`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicant` | 출원인정보 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 발명자정보
`inventorSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `inventors` | 발명자명/특허고객번호 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 대리인정보
`agentSearchInfo`

- **분류**: 항목별검색
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `agent` | 대리인명/대리인번호 | (대리인명 or 대리인번호) |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 등록권자정보
`rightHolerSearchInfo`

- **분류**: 항목별검색
- **상태**: ✅ 구현됨 → `KoreanPatentRighterSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/openapi/rest/patUtiModInfoSearchSevice/rightHolerSearchInfo`
- **인증 키**: `accessKey` (KIPRIS Plus)
- **응답 루트 키**: `response.body.items.PatentUtilityInfo`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `rightHoler` | 등록권자명 | (등록권자명) |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `docsCount` | 페이지당건수 | (기본 : 30, 최대 500) |
| `patent` | 특허 | (포함 : true, 미포함 : false) |
| `utility` | 실용 | (포함 : true, 미포함 : false) |
| `lastvalue` | 행정처분 | (전체:공백입력, 공개:A, 취하:C, 소멸:F, 포기:G, 무효:I, 거절:J, 등록:R) |
| `sortSpec` | 정렬기준 | (PD-공고일자, AD-출원일자, GD-등록일자, OPD-공개일자, FD-국제출원일자, FOD-국제공개일자, RD-우선권주장일자) |
| `descSort` | 정렬방식 | (asc방식 : false, desc방식 : true) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `PatentUtilityInfo` |  |  |
| `Applicant` | 출원인명 |  |
| `OpeningDate` | 공개일자 |  |
| `OpeningNumber` | 공개번호 |  |
| `PublicNumber` | 공고번호 |  |
| `PublicDate` | 공고일자 |  |
| `RegistrationDate` | 등록일자 |  |
| `RegistrationNumber` | 등록번호 |  |
| `RegistrationStatus` | 등록상태 |  |
| `ApplicationDate` | 출원일자 |  |
| `ApplicationNumber` | 출원번호 |  |
| `Abstract` | 초록 | (limited within 680 character) |
| `DrawingPath` | 큰이미지경로 |  |
| `ThumbnailPath` | 이미지경로 |  |
| `SerialNumber` | 일련번호 |  |
| `InventionName` | 발명의명칭 | 한글 |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |
| `totalSearchCount` | 전체건수 |  |

---

## 서지상세정보(공공데이터 포털 연계)
`getBibliographyDetailInfoSearch`

- **분류**: 서지정보
- **상태**: ✅ 구현됨 → `KoreanPatentDetailSearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/kipo-api/kipi/patUtiModInfoSearchSevice/getBibliographyDetailInfoSearch`
- **인증 키**: `ServiceKey` (공공데이터 포털)
- **응답 루트 키**: `response.body.item`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `item` |  |  |
| `biblioSummaryInfoArray` |  |  |
| `biblioSummaryInfo` |  |  |
| `applicationDate` | 출원일자 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationFlag` | 출원구분 |  |
| `claimCount` | 청구항수 |  |
| `examinerName` | 심사관명 |  |
| `finalDisposal` | 최종처분내용 |  |
| `inventionTitle` | 발명의명칭 | 한글 |
| `inventionTitleEng` | 발명의명칭 | 영문 |
| `openDate` | 공개일자 |  |
| `openNumber` | 공개번호 |  |
| `originalApplicationDate` | 원출원출원일자 | (신규, 국제출원, null) |
| `originalApplicationKind` | 원출원종류 |  |
| `originalApplicationNumber` | 원출원출원번호 |  |
| `originalExaminationRequestDate` | 심사청구일자 |  |
| `originalExaminationRequestFlag` | 심사청구여부 |  |
| `publicationDate` | 공고일자 |  |
| `publicationNumber` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNumber` | 등록번호 |  |
| `registerStatus` | 등록상태 |  |
| `translationSubmitDate` | 번역문제출일자 |  |
| `ipcInfoArray` |  |  |
| `ipcInfo` |  |  |
| `ipcDate` | IPC개정일자 |  |
| `ipcNumber` | IPC코드 |  |
| `familyInfoArray` |  |  |
| `familyInfo` |  |  |
| `familyApplicationNumber` | 패밀리출원번호 |  |
| `abstractInfoArray` |  |  |
| `abstractInfo` |  |  |
| `astrtCont` | 초록 |  |
| `internationalInfoArray` |  |  |
| `internationalInfo` |  |  |
| `internationOpenDate` | 국제공개일자 |  |
| `internationOpenNumber` | 국제공개번호 |  |
| `internationalApplicationDate` | 국제출원일자 |  |
| `internationalApplicationNumber` | 국제출원번호 |  |
| `claimInfoArray` |  |  |
| `claimInfo` |  |  |
| `claim` | 청구항 |  |
| `applicantInfoArray` |  |  |
| `applicantInfo` |  |  |
| `address` | 출원인주소 |  |
| `code` | 특허고객번호 | 특허고객번호 |
| `country` | 출원인국가 |  |
| `engName` | 출원인명 | 영문 |
| `name` | 출원인명 | 한글 |
| `inventorInfoArray` |  |  |
| `inventorInfo` |  |  |
| `address` | 발명자주소 |  |
| `code` | 특허고객번호(발명자번호) | 특허고객번호(발명자번호) |
| `country` | 발명자국가 |  |
| `engName` | 발명자명 | 영문 |
| `name` | 발명자명 | 한글 |
| `agentInfoArray` |  |  |
| `agentInfo` |  |  |
| `address` | 대리인주소 |  |
| `code` | 대리인번호 | 대리인번호 |
| `country` | 대리인국가 |  |
| `engName` | 대리인명 | 영문 |
| `name` | 대리인명 | 한글 |
| `priorityInfoArray` |  |  |
| `priorityInfo` |  |  |
| `priorityApplicationCountry` | 우선권주장국가 |  |
| `priorityApplicationNumber` | 우선권주장번호 |  |
| `priorityApplicationDate` | 우선권주장일자 |  |
| `designatedStateInfoArray` |  |  |
| `designatedStateInfo` |  |  |
| `kind` | 지정국가그룹 |  |
| `country` | 지정국가 |  |
| `priorArtDocumentsInfoArray` |  |  |
| `priorArtDocumentsInfo` |  |  |
| `documentsNumber` | 선행기술조사문헌번호 |  |
| `examinerQuotationFlag` | 심사관인용여부 |  |
| `legalStatusInfoArray` |  |  |
| `legalStatusInfo` |  |  |
| `commonCodeName` | 처리상태 |  |
| `documentEngName` | 서류명 | 영문 |
| `documentName` | 서류명 | 한글 |
| `receiptDate` | 접수일자 |  |
| `receiptNumber` | 접수번호 |  |
| `imagePathInfo` |  |  |
| `docName` | 파일명 |  |
| `largePath` | 큰이미지경로 |  |
| `path` | 이미지경로 |  |
| `rndInfoArray` |  |  |
| `rndInfo` |  |  |
| `rndDepartmentName` | 연구부처명 |  |
| `rndDuration` | 연구기관내용 |  |
| `rndManagingInstituteName` | 주관기관명 |  |
| `rndProjectName` | 연구사업명 |  |
| `rndSpecialInstituteName` | 연구관리전문기관명 |  |
| `rndTaskContribution` | 연구과제기여율내용 |  |
| `rndTaskName` | 연구과제명 |  |
| `rndTaskNumber` | 연구개발과제번호 |  |

---

## 서지요약정보
`getBibliographySumryInfoSearch`

- **분류**: 서지정보
- **상태**: ✅ 구현됨 → `KoreanPatentSummarySearchTool`
- **Endpoint**: `https://plus.kipris.or.kr/kipo-api/kipi/patUtiModInfoSearchSevice/getBibliographySumryInfoSearch`
- **인증 키**: `ServiceKey` (공공데이터 포털)
- **응답 루트 키**: `response.body.items.item`

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `item` |  |  |
| `applicationDate` | 출원일자 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationFlag` | 출원구분 |  |
| `claimCount` | 청구항수 |  |
| `examinerName` | 심사관명 |  |
| `finalDisposal` | 최종처분내용 |  |
| `inventionTitle` | 발명의명칭 | 한글 |
| `inventionTitleEng` | 발명의명칭 | 영문 |
| `openDate` | 공개일자 |  |
| `openNumber` | 공개번호 |  |
| `originalApplicationDate` | 원출원출원일자 |  |
| `originalApplicationKind` | 원출원종류 |  |
| `originalApplicationNumber` | 원출원출원번호 |  |
| `originalExaminationRequestDate` | 심사청구일자 |  |
| `originalExaminationRequestFlag` | 심사청구여부 |  |
| `publicationDate` | 공고일자 |  |
| `publicationNumber` | 공고번호 |  |
| `registerDate` | 등록일자 |  |
| `registerNumber` | 등록번호 |  |
| `registerStatus` | 등록상태 |  |
| `translationSubmitDate` | 번역문제출일자 |  |
| `count` |  |  |
| `numOfRows` | 페이지당건수 | (기본 : 30, 최대 500) |
| `pageNo` | 페이지번호 |  |
| `totalCount` | 전체건수 |  |

---

## IPC정보
`patentIpcInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentIpcInfo` |  |  |
| `InternationalpatentclassificationNumber` | IPC코드 |  |
| `InternationalpatentclassificationDate` | IPC개정일자 |  |

---

## CPC정보
`patentCpcInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentCpcInfo` |  |  |
| `CooperativepatentclassificationNumber` | CPC코드 |  |
| `CooperativepatentclassificationDate` | CPC개정일자 |  |

---

## 국가연구개발사업정보
`patentRndInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentRndInfo` |  |  |
| `ResearchDevelopmentTaskNumber` | 연구개발과제번호 |  |
| `ResearchMinistriesandofficesName` | 연구부처명 |  |
| `ResearchProjectName` | 연구사업명 |  |
| `ResearchTaskName` | 연구개발과제번호 |  |
| `ManagementInstitutionName` | 주관기관명 |  |
| `ResearchDevelopmentTerm` | 연구기간내용 |  |
| `ResearchManagementFulltextInstitutionName` | 연구관리전문기관명 |  |
| `ResearchTaskContributionrate` | 연구과제기여율내용 |  |

---

## 출원인정보
`patentApplicantInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentApplicantInfo` |  |  |
| `ApplicantName` | 출원인명 |  |
| `ApplicantEnglishsentenceName` | 출원인명 | 한글 |
| `ApplicantNumber` | 특허고객번호 | 특허고객번호 |
| `ApplicantAddress` | 출원인주소 |  |
| `ApplicantCountryName` | 출원인국가 |  |

---

## 발명자정보
`patentInventorInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentInventorInfo` |  |  |
| `InventorName` | 발명자명 | 한글 |
| `InventorEnglishsentenceName` | 발명자명 | 영문 |
| `InventorNumber` | 발명자번호 | 발명자번호(특허고객번호) |
| `InventorAddress` | 발명자주소 |  |
| `InventorCountryName` | 발명자국가 |  |

---

## 패밀리정보
`patentFamilyInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentFamilyInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `countryCode` | 국가코드 |  |
| `countryName` | 국가명 |  |
| `familyKind` | 패밀리종류 |  |
| `familyNumber` | 패밀리번호 |  |
| `literatureKind` | 문헌종류 |  |
| `literatureNumber` | 문헌번호 |  |
| `openingNumber` | 공개번호 |  |

---

## 초록
`patentAbstractInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `patentAstrtContInfo` |  |  |
| `astrtCont` | 초록 |  |

---

## 국제출원정보
`patentInternationalInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `internationalInfo` |  |  |
| `internationOpenDate` | 국제공개일자 |  |
| `internationOpenNumber` | 국제공개번호 |  |
| `internationalApplicationDate` | 국제출원일자 |  |
| `internationalApplicationNumber` | 국제출원번호 |  |

---

## 청구항
`patentClaimInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `claimInfo` |  |  |
| `claim` | 청구항 |  |

---

## 대리인
`patentAgentInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `AgentInfo` |  |  |
| `address` | 대리인주소 |  |
| `code` | 대리인번호 |  |
| `country` | 대리인국가 |  |
| `engName` | 대리인명 | 영문 |
| `name` | 대리인명 | 한글 |

---

## 우선권정보
`patentPriorityInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `priorityInfo` |  |  |
| `priorityApplicationCountry` | 우선권주장국가 |  |
| `priorityApplicationDate` | 우선권주장일자 |  |
| `priorityApplicationNumber` | 우선권주장번호 |  |

---

## 지정국
`patentDesignatedStateInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `designatedStateInfo` |  |  |
| `country` | 지정국가 |  |
| `kind` | 지정국가그룹 |  |

---

## 선행기술조사문헌
`patentPriorArtDocumentsInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `priorArtDocumentsInfo` |  |  |
| `documentsNumber` | 선행기술조사문헌번호 |  |
| `examinerQuotationFlag` | 심사관인용여부 |  |

---

## 행정처리
`patentLegalStatusInfo`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `legalStatusInfo` |  |  |
| `commonCodeName` | 처리상태 |  |
| `documentEngName` | 서류명 | 영문 |
| `documentName` | 서류명 | 한글 |
| `receiptDate` | 접수일자 |  |
| `receiptNumber` | 접수번호 |  |

---

## 패밀리출원정보
`patentFamilyInfoV1`

- **분류**: 서지정보
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `familyInfoV1` |  |  |
| `familyApplicationNumber` | 패밀리출원번호 |  |

---

## 공개전문PDF
`getPubFullTextInfoSearch`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `Item` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 공고전문PDF
`getAnnFullTextInfoSearch`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `Item` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 정정공고PDF(폐기예정)
`getRevisionFullTextInfoSearch`

- **분류**: 도면/전문
- **상태**: ⚠️ 폐기예정

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `Item` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |
| `date` | 일자 |  |
| `number` | 번호 |  |

---

## 대표도면
`getReprsntFloorPlanInfoSearch`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `body` |  |  |
| `docName` | 파일명 |  |
| `largePath` | 큰이미지경로 |  |
| `path` | 이미지경로 |  |

---

## 정정공고PDF_V2
`revisionfullDocPDFInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `revisionfullDocPDFInfo` |  |  |
| `applicationNumber` | 출원번호 |  |
| `number` | 번호 |  |
| `typeCode` | 코드 |  |
| `typeDescription` | 코드명 |  |
| `date` | 일자 |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 공개책자
`patentUnexPubBookInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `filePathInfo` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 공보책자
`patentExamPubBookInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `filePathInfo` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 모든 전문 및 대표도 유무
`patentFullTextCheckInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `fullTextCheckResponse` |  |  |
| `unexPubfullDocPDFCheckResult` | 공개전문유무 | (있음:Y 없음:N) |
| `examPubfullDocPDFCheckResult` | 공고전문유무 | (있음:Y 없음:N) |
| `revisionfullDocPDFCheckResult` | 정정공고유무 | (있음:Y 없음:N) |
| `abstractFigureCheckResult` | 대표도유무 | (있음:Y 없음:N) |
| `unexPubBookCheckResult` | 공개책자유무 | (있음:Y 없음:N) |
| `examPubBookCheckResult` | 공고책자유무 | (있음:Y 없음:N) |
| `registrationCheckResult` | 등록사항유무 | (있음:Y 없음:N) |

---

## 전문파일정보
`patentFullTextFileInfo`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `fullTextFileInfo` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 표준화 공개전문PDF
`getStandardPubFullTextInfoSearch`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `Item` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 표준화 공고전문PDF
`getStandardAnnFullTextInfoSearch`

- **분류**: 도면/전문
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `Item` |  |  |
| `docName` | 파일명 |  |
| `path` | 파일경로 |  |

---

## 변동정보
`getChangeInfoSearch`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `date` | 변동일자 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `itme` |  |  |
| `count` | 변동건수 |  |
| `transListString` | 출원번호리스트 | (ex : 출원번호1&#124;출원번호2) |

---

## 변동정보2
`patentTransferInfo`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `searchType` | 검색코드 | (BIB-서지, PRI-우선권, IPC, CPC, AP1-출원인(추가및삭제), AP2-출원인(이름및주소변경) AG-대리인, IN-발명자, DG-지정국, PA-선행기술문헌, PB-공보전문, RP-정정공보, AB-초록, CL-청구항, DR-대표도면, RND-국가연구개발사업, ADM-행정처리, RFO-심사청구) |
| `transferDate` | 변동일자 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentTransferInfo` |  |  |
| `transferCount` | 변동건수 |  |
| `transferList` | 출원번호리스트 | (ex : 출원번호1&#124;출원번호2) |

---

## 서지정보 조회(과제번호)
`patentBiblioInfo`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `researchDevelopmentTaskNumber` | 연구과제번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `patentUtilityInfo` |  |  |
| `serialNumber` | 일련번호 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `openingNumber` | 공개번호 |  |
| `openingDate` | 공개일자 |  |
| `publicNumber` | 공고번호 |  |
| `publicDate` | 공고일자 |  |
| `registrationNumber` | 등록번호 |  |
| `registrationDate` | 등록일자 |  |
| `internationalpatentclassificationNumber` | IPC코드 |  |
| `inventionName` | 발명자명 |  |
| `abstract` | 초록 |  |
| `applicant` | 출원인명 |  |
| `drawingPath` | 큰이미지경로 |  |
| `thumbnailPath` | 이미지경로 |  |
| `registrationStatus` | 등록상태 |  |

---

## IPC코드 조회
`ipcNumberSearchInfo`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `ipcNumber` | IPC코드 | 코드 및 단어 |
| `docsStart` | 페이지번호 | (검색 페이지 번호) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `getsearchipcinfolist` |  |  |
| `getsearchipcinfo` |  |  |
| `indexNo` | 일련번호 |  |
| `ipcNumber` | IPC코드 |  |
| `korDescription` | 한글설명 |  |
| `engDescription` | 영어설명 |  |
| `totalSearchCount` | 전체건수 |  |

---

## 속보서비스
`patentBulletinAllListInfo`

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `date` | 속보일자 | (YYYYMMDD) |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `bulletinAllListInfo` |  |  |
| `applicantName` | 출원인명 |  |
| `applicationNumber` | 출원번호 |  |
| `applicationDate` | 출원일자 |  |
| `title` | 발명의명칭 |  |

---

## 최종변동일자

- **분류**: 부가기능
- **상태**: ❌ 미구현

### 요청 파라미터 (IN)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `applicationNumber` | 출원번호 |  |

### 응답 파라미터 (OUT)

| 항목명 | 설명 | 비고 |
|--------|------|------|
| `items` |  |  |
| `lastTransferDateInfo` | 최종변동일자 |  |

---
