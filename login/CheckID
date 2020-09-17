# fan.catholic.ac.kr-api-reference
fan.catholic.ac.kr 의 API Reference Repository 입니다.

## 아이디 중복 체크 (완료)
-  부분에 프론트가 백엔드에게 요청하는 경우 ( 요청 ), 프론트가 요청한 API 백엔드가 제작 완료한 경우 ( 완료 )
- URI : fan.catholic.ac.kr:5000/api/check/id
- METHOD : GET
- request

    | key | explanation | type |
    |--- |--- |--- |
    | user_id | login id | string |

- response code
    - Header :
        Content-Type : application/json
    - ERROR RESPONSE
    
        |    key   | explanation |   type  |
        | -------- | ----------- |-------- | 
        | login | False  | string  |
        |error_code| 오류 코드     | integer |
        
        - error_code (오류 별 반환 내용 및 상태)
        
            | HTTP STATE | error_code | explanation |
            |----------- | ---------- | ----------- |
            | 400 |0| 파라미터 오류, 상세 내용은 error_msg 참고 |
            | 404 |1| 아이디가 없을 때, 비밀번호가 일치하지 않을때 |
    
    - SUCCESS RESPONSE
    
        | key | explanation | type |
        |--- |--- |--- |
        | id | True | string |
        


