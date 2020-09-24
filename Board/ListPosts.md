# fan.catholic.ac.kr-api-reference - 팬 자유 게시판 리스트 (완료)
# 의도: 게시판의 리스트 목록이 뜰 예정 입니다.

fan.catholic.ac.kr 의 API Reference Repository 입니다.

- (예시) 부분에 프론트가 백엔드에게 요청하는 경우 ( 요청 ), 프론트가 요청한 API 백엔드가 제작 완료한 경우 ( 완료 )
- URI : fan.catholic.ac.kr:5000/api/post/list
- METHOD : GET

- request

    | key | explanation | type |
    |--- |--- |--- |
    | board_name | 게시판명 | string |

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
        | list | 게시글 전체 정보 | string |
        
    - FAIL RESPONSE : 임시로 error_code 대신 유지하도록 하겠습니다. 401경우 token : False 
    
        | key | explanation | type |
        |--- |--- |--- |
        | token | False | string |
