# 설비 보전 경험 지식 공유 플랫폼 API
&nbsp; &nbsp; 
&nbsp; &nbsp; 
&nbsp; &nbsp; 

## 경험지식 요청 리스트 전체 조회

### Request

`GET http://117.52.144.113:8080/project9/getDataQnaListAll`

#### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|keyword|String|검색어| |
|industry_gubun|String|산업군| |
|process_gubun|String|상세 공정| |
|broken_sh|String|고장 상황| |
|broken_hs|String|고장 현상| |

### Response
       
## 경험지식 요청 글 상세 조회

### Request

`GET http://117.52.144.113:8080/project9/getDataQnaReply`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|qna_idx|String|요청 글 번호|O|

### Response

## 경험지식 – 요청 등록

### Request

`POST http://117.52.144.113:8080/project9/insertDataQna_attach`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|industry_gubun|String|산업군| |
|process_gubun|String|상세 공정|O|
|broken_sh|String|고장 상황|O|
|broken_hs|String|고장 현상| |
|model|String|모델명| |
|model_com|String|모델제조사| |
|model_create_dt|String|제조일자| |
|model_install_dt|String|설치일자| |
|mold_break_yn|String|금형파손여부| |
|title|String|제목|O|
|content|String|내용|O|
|qna_attach|File|첨부파일| |

### Response
