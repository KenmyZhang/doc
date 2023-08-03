# IP文件上传

## Example

    curl -X POST "http://127.0.0.1:8081/api/v3/ip/data/file"  -i -F realfile=@"/Users/zhangkunming/go/src/go-fly/static/ipinfo/ip3.csv"
    HTTP/1.1 100 Continue

    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 02 Aug 2023 10:32:26 GMT
    Content-Length: 185


    {
        "code": 200,
        "msg": "上传成功!",
        "result": {
            "ext": ".csv",
            "name": "ip3.csv",
            "path": "http://43.139.163.35:8081/static/ipinfo/2023August/100b585c66cc206a5f1a44c476c6e6e4.csv",
            "size": 32298
        }
    }