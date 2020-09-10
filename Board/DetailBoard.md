# fan.catholic.ac.kr-api-reference - 팬 게시판 자세히 보기 (완료)
# 의도: 게시글을 자세히 볼 수 있습니다.

fan.catholic.ac.kr 의 API Reference Repository 입니다.

- (예시) 부분에 프론트가 백엔드에게 요청하는 경우 ( 요청 ), 프론트가 요청한 API 백엔드가 제작 완료한 경우 ( 완료 )
- URI : fan.catholic.ac.kr:5000/api/board/detail
- METHOD : GET

- request

    | key | explanation | type |
    |--- |--- |--- |
    | board_name | 게시판명 | string |
    | title | 제목 | string |
    | writer | 로그인 된 현재 아이디 | string |
    | date | 글을 작성한 날짜 | string |

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
        | detail | True | string |
        

