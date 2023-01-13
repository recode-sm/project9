# 설비 보전 경험 지식 공유 플랫폼 API
&nbsp; &nbsp; 
&nbsp; &nbsp; 
&nbsp; &nbsp; 

## 경험지식 요청 리스트 전체 조회

### Request

`GET https://info.oliveware.co.kr:8080/project9/getDataQnaListAll`

&nbsp; &nbsp;
### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|keyword|String|검색어| |
|industry_gubun|String|산업군| |
|process_gubun|String|상세 공정| |
|broken_sh|String|고장 상황| |
|broken_hs|String|고장 현상| |

&nbsp; &nbsp;
### Response
|이름|데이터명|유형|
|------|---|---|
|qna_list|요청글 목록| |
|qna_idx|요청글 순번|int|
|usernm|작성자|String|
|industry_gubun_name|산업군|String|
|process_gubun_name|상세공정|String|
|broken_sh_name|고장상황|String|
|broken_hs_name|고장현상|String|
|title|제목|String|
|content|내용|String|
|job_dt|작성일시|String|
|finish_yn|채택여부|int|
|reply_count|답변수|int|


&nbsp; &nbsp;
### Jquery 코드 샘플
```javascript 
function getDataQnaListAll(){
    var search ={
        user_token:" eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.
        eyJ1c2Vybm8iOjg1LCJ1c2VyaWQiOiJkbXRlazEwNiIsImlhdCI6MTY3MDk4MjY0MSwiZXhwIjoxNjc4NzU4NjQxfQ.
        iWSLtvLgUFAw8ODaDDURcILvOqJEYnx5kjOd6AZhTg8",
        keyword: '',
        industry_gubun: '',
        process_gubun: '',
        broken_sh: '',
        broken_hs: ''
    }
    $.ajax({
        url: "http://info.oliveware.co.kr:8080/project9/getDataQnaListAll",
        type: "GET",
        async: false,
        crossDomain: true,
        daraType: "json",
        contentType: "text/plain",
        mimeType: "text/plain",
        data: search,
        success:function(response){
            console.log(response)
        }
    });
}
```


&nbsp; &nbsp; 
&nbsp; &nbsp;       
## 경험지식 요청 글 상세 조회

### Request

`GET http://info.oliveware.co.kr:8080/project9/getDataQnaReply`

&nbsp; &nbsp;
### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|qna_idx|String|요청 글 번호|O|

&nbsp; &nbsp; 
### Response
|이름|데이터명|유형|
|------|---|---|
|industry_gubun_name|산업군|String|
|process_gubun_name|상세공정|String|
|model|모델명|String|
|model_com|모델제조사|String|
|model_create_dt|제조일자|String|
|model_install_dt|설치일자|String|
|broken_sh_name|고장상황|String|
|broken_hs_name|고장현상|String|
|title|제목|String|
|content|내용|String|
|job_dt|작성일시|String|
|finish_yn|채택여부|int|
|reply_count|답변수|int|
|fileList|첨부 파일 목록| |
|ata_org_name|파일 크기 | |
| |파일 크기| |
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |


&nbsp; &nbsp; 
&nbsp; &nbsp; 
## 경험지식 – 요청 등록

### Request

`POST http://info.oliveware.co.kr:8080/project9/insertDataQna_attach`

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
&nbsp; &nbsp; 

## 경험지식 – 경험 지식 수정

### Request

`GET http://info.oliveware.co.kr:8080/project9/updateMyQna`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|qna_idx|int|요청 글 번호|O|
|industry_gubun|int|산업군| |
|process_gubun|int|상세 공정|O|
|model|String|모델명| |
|model_com|String|모델제조사| |
|model_create_dt|String|제조일자| |
|model_install_dt|String|설치일자| |
|mold_break_yn|String|금형파손여부| |
|broken_sh|int|고장 상황|O|
|broken_hs|int|고장 현상| |
|title|String|제목|O|
|content|String|내용|O|

### Response
&nbsp; &nbsp; 

## 경험지식 – 답변 등록

### Request

`POST http://info.oliveware.co.kr:8080/project9/insertDataReply_attach`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|qna_idx|String|요청글 번호|O|
|content_reply|String|답변 내용|O|
|reply_attach|File|첨부파일| |

### Response
&nbsp; &nbsp; 

## 경험지식 – 답변 수정

### Request

`GET http://info.oliveware.co.kr:8080/project9/updateDataReply`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|reply_idx|String|답변 번호|O|
|content_reply|String|답변 내용|O|


### Response
&nbsp; &nbsp; 

## 경험지식 – 답변 삭제

### Request

`GET http://info.oliveware.co.kr:8080/project9/deleteDataReply`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|reply_idx|String|답변 번호|O|

### Response
&nbsp; &nbsp; 

## 경험지식 – 나의 경험 지식 리스트 조회

### Request

`GET http://info.oliveware.co.kr:8080/project9/getMyDataQnaList`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|page|int|페이지 번호| |

### Response
&nbsp; &nbsp; 

## 경험지식 – 고객센터 글 등록

### Request

`GET http://info.oliveware.co.kr:8080/project9/insertDataHelp`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|brdtitle|String|글 제목|O|
|brdmemo|String|글 내용|O|

### Response
&nbsp; &nbsp; 

## 경험지식 – 고객센터 리스트 조회

### Request

`GET http://info.oliveware.co.kr:8080/project9/getDataHelpList`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|page|int|페이지 번호| |
|keyword|String|검색어| |

### Response
&nbsp; &nbsp; 

## 경험지식 – 고객센터 글 상세 조회

### Request

`GET http://info.oliveware.co.kr:8080/project9/getDataHelpOne`

### Parameters
|이름|데이터명|유형|필수여부|
|------|---|---|:---:|
|user_token|String|외부 사용자 인증키|O|
|brdno|String|글 번호|O|

### Response
&nbsp; &nbsp; 
