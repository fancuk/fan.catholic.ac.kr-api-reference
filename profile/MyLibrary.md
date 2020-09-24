# fan.catholic.ac.kr-api-reference
fan.catholic.ac.kr 의 API Reference Repository 입니다.

## 회원 대여 목록 (완료)
- (예시) 부분에 프론트가 백엔드에게 요청하는 경우 ( 요청 ), 프론트가 요청한 API 백엔드가 제작 완료한 경우 ( 완료 )
- URI : fan.catholic.ac.kr:5000/api/user/library
- METHOD : GET
- request

    | key | explanation | type |
    |--- |--- |--- |
    |user_id  | id:아이디    | string

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
            | 400 |0| 파라미터 오류 | 상세 내용은 error_msg 참고 |
            | 401 |1| 쿠키, 세션 만료 | 쿠키, 세셔 만료 혹은 존재 X |
    
    - SUCCESS RESPONSE
    
        | key | explanation | type |
        |--- |--- |--- |
        | list | Book List | json |
        
    - FAIL RESPONSE : 임시로 error_code 대신 유지하도록 하겠습니다. 401경우 token : False 
    
        | key | explanation | type |
        |--- |--- |--- |
        | token | False | string |
