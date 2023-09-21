# 增加备注

    ip: ip地址
    remark: 备注

页面显示备注，需要支持换行符号

## Example

    curl 'http://43.139.163.35:8081/api/v3/ip/remark'    -X POST  -d '{"ip": "d514cd7e-5fc1-4d42-91bd-fa4bc1138d91", "remark":"备注"}' -i
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Sat, 12 Aug 2023 15:15:58 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}