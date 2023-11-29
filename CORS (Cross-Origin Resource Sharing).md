# CORS (Cross-Origin Resource Sharing)

CORS(Cross-Origin-Resource-Sharing)는 다른 도메인 간의 자원 공유를 제어하는 메커니즘입니다. 예를 들어, `mangkyu.com`에서 `mang.com`으로 데이터를 요청하는 경우, 특별한 설정이 없다면 CORS 에러가 발생할 수 있습니다.

## CORS의 생성 이유
CORS는 서버가 특정 도메인의 요청만을 허용하기 위해 존재합니다. 요청이 허용되기 위해서는 응답 헤더에 특정 내용을 추가해야 합니다.

### 응답 헤더 설정
- `Access-Control-Allow-Origin`: 요청을 보내는 페이지의 출처를 지정합니다. (`*` 또는 특정 도메인)
- `Access-Control-Allow-Methods`: 서버가 허용하는 요청 메소드를 지정합니다. 기본값은 `GET`, `POST`입니다.
- `Access-Control-Max-Age`: 클라이언트가 preflight 요청(서버의 응답 가능 여부 확인) 결과를 캐시할 시간을 지정합니다.
- `Access-Control-Allow-Headers`: 서버가 허용하는 헤더를 지정합니다.

### 예제

- Access-Control-Allow-Origin: *
- Access-Control-Allow-Methods: GET, POST
- Access-Control-Max-Age: 86400
- Access-Control-Allow-Headers: Content-Type
- `*`을 `Access-Control-Allow-Origin`에 설정하면 모든 도메인에 대한 요청을 허용하게 됩니다. 하지만 보안상의 이유로 특정 도메인만을 지정하는 것이 일반적입니다.
