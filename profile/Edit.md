# fan.catholic.ac.kr-api-reference
fan.catholic.ac.kr 의 API Reference Repository 입니다.

## 회원 정보 수정 (완료)
- (예시) 부분에 프론트가 백엔드에게 요청하는 경우 ( 요청 ), 프론트가 요청한 API 백엔드가 제작 완료한 경우 ( 완료 )
- URI : fan.catholic.ac.kr:5000/api/profile/edit
- METHOD : PUT
- request

    | key | explanation | type |
    |--- |--- |--- |
    |user_id  | id:아이디    | string
    |user_pwd | pwd:비밀번호 | string
    |name     | name :이름   | string
    |student_id| student_id학번 | int
    |grade    | grade :학년  | int
    |semester |semester:학기 | int
    |phone    |phone:전화번호|string
    |email    |email:이메일  |string

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
        | edit | True | string |

    - FAIL RESPONSE : 임시로 error_code 대신 유지하도록 하겠습니다. 400 409 같은 경우 edit : False이며 401경우 token : False 
    
        | key | explanation | type |
        |--- |--- |--- |
        | edit | False | string |
        | token | False | string |
