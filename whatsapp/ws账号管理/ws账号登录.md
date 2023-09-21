# ws账号登录

## 参数

    mobile手机号

## Example 


        curl -X POST "http://170.106.67.171:8081/api/v1/ws/user/login" -i -d '{"mobile":"xxxx"}'
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Thu, 21 Sep 2023 19:42:24 GMT
    Content-Length: 176

    {"code":"SUCCESS","message":"Login success","results":{"qr_duration":30,"qr_link":"http://170.106.67.171:8081/statics/qrcode/scan-qr-b59e2a4c-b860-48c2-b625-7619a7a2906b.png"}}