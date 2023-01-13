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

    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2

    []

## 경험지식 요청 글 상세 조회

### Request

`GET http://117.52.144.113:8080/project9/getDataQnaReply`

### Response
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|qna_idx|String|요청 글 번호|O|

### Request
