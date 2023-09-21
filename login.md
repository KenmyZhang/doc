# 登录

    只需要输入账号登录，不需要密码，登录成功后，后续的请求需要带上token请求头

## Example 

    curl -X POST "http://43.139.163.35:8081/api/v3/customer/login" -i  -d '{"account":"123"}'
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 12:20:48 GMT
    Content-Length: 406

    {"code":200,"msg":"验证成功,正在跳转","result":{"created_time":1690374048,"ref_token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDgsInJlZl90b2tlbiI6dHJ1ZX0.lce_OSmq4BOgbrANLDSAbwYcNuR2S-iFb5Yuq5M6ZYI","token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg"}}