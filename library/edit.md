# fan.catholic.ac.kr-api-reference
fan.catholic.ac.kr 의 API Reference Repository 입니다.

## 책 수정 (완료)
- URI : fan.catholic.ac.kr:5000/api/library/edit
- METHOD : POST
- request

    | key | explanation | type |
    |--- |--- |--- |
    | title | 책 제목 | string |
    | edit_title | 수정할 책 제목 | int |
    | edit_writer | 수정할 저자 | string |
    | edit_count | 수정할 책 개수 | int |
    | edit_image | 수정할 이미지 경로 | string |
    

- response code
    - Header :
        Content-Type : application/json
    - ERROR RESPONSE
    
        |    key   | explanation |   type  |
        | -------- | ----------- |-------- |
        |error_code| 오류 코드  | integer | 
        |error_msg | 오류 내용  | string  |
        
        - error_code (오류 별 반환 내용 및 상태)
        
            | HTTP STATE | error_code | explanation |
            |----------- | ---------- | ----------- |
            |  |0| 파라미터 오류, 상세 내용은 error_msg 참고 |
            |  |1| 세션 혹은 쿠키 만료 |

    
    - SUCCESS RESPONSE
    
        | key | explanation | type |
        |--- |--- |--- |
        | edit | True | string |
        | token | 발급 토큰(클라이언트에서 저장하세요!) | string |

    - FAIL RESPONSE
    
        | key | explanation | type |
        |--- |--- |--- |
        | token | False | string |
