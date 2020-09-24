# fan.catholic.ac.kr-api-reference - 팬 게시판 수정 (완료)
# 의도: 게시글을 수정 할 수 있습니다.

fan.catholic.ac.kr 의 API Reference Repository 입니다.

- (예시) 부분에 프론트가 백엔드에게 요청하는 경우 ( 요청 ), 프론트가 요청한 API 백엔드가 제작 완료한 경우 ( 완료 )
- URI : fan.catholic.ac.kr:5000/api/post/edit
- METHOD : PUT

- request

    | key | explanation | type |
    |--- |--- |--- |
    | board_name | 게시판명 | string |
    | title | 제목 | string |
    | writer | 로그인 된 현재 아이디 | string |
    | date | 글을 작성한 날짜 | string |
    | edit_title | 수정할 제목 | string |
    | edit_content | 수정할 내용 | string |

- response code
    - Header :
        Content-Type : application/json
    - ERROR RESPONSE
    
        |    key   | explanation |   type  |
        | -------- | ----------- |-------- |
        |error_code| 오류 코드     | integer | 
        |error_msg | 오류 내용  | string  |
        
        - error_code (오류 별 반환 내용 및 상태)
        
            | HTTP STATE | error_code | explanation |
            |----------- | ---------- | ----------- |
            | 400 |0| 파라미터 오류, 상세 내용은 error_msg 참고 |
   
    - SUCCESS RESPONSE
    
        | key | explanation | type |
        |--- |--- |--- |
        | edit | True | string |
        
    - FAIL RESPONSE : 임시로 error_code 대신 유지하도록 하겠습니다. 400 409 같은 경우 edit : False이며 401경우 token : False 
    
        | key | explanation | type |
        |--- |--- |--- |
        | edit | False | string |
        | token | False | string |
