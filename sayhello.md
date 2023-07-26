# 增加打招呼

    type :类型 1文字、2图片
    content: 内容/或者图片链接

## Example 


    curl -X POST "http://43.139.163.35:8081/api/v3/sayhello/setting" -i -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg"  -d '{"type":1, "content":"2134"}'

    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 12:24:07 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 查询打招呼配置

    无翻页，全量返回

## Example

    curl -X GET "http://43.139.163.35:8081/api/v3/sayhello/setting" -i -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg"  
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 12:26:08 GMT
    Content-Length: 355

    {"code":200,"data":[{"id":1,"type":0,"account":"123","content":"","enable":true,"is_del":0,"updated_time":"2023-07-26T20:23:11+08:00","created_time":"2023-07-26T20:23:11+08:00"},{"id":2,"type":1,"account":"123","content":"2134","enable":true,"is_del":0,"updated_time":"2023-07-26T20:24:08+08:00","created_time":"2023-07-26T20:24:08+08:00"}],"result":"ok"}

# 更新打招呼配置
    id 配置ID，数据类型int
    content 打招呼内容，数据类型string
## Example 

    curl -X POST "http://43.139.163.35:8081/api/v3/sayhello/setting/update" -i -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg"  -d '{"id":1, "content":"6662134"}'
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 12:30:25 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 删除打招呼配置

    id ：配置id，数据类型 int
## Example  

curl -X POST "http://43.139.163.35:8081/api/v3/sayhello/setting/del" -i -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg"  -d '{"id":1}'
HTTP/1.1 200 OK
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
Access-Control-Allow-Origin: *
Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
Content-Type: application/json; charset=utf-8
Date: Wed, 26 Jul 2023 12:37:30 GMT
Content-Length: 26

{"code":200,"result":"ok"}