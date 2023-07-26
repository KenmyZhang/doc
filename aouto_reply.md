# 新建自动回复组

    curl -X POST "http://43.139.163.35:8081/api/v3/autoreply/group/setting" -i -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg"  -d '{"name":"组名"}'
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:19:49 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 更新自动回复组名


## Example 
    curl -X POST "http://43.139.163.35:8081/api/v3/autoreply/group/setting/update" -i -d '{"id":1, "name":"测试组"}' -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:31:54 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 删除自动回复组

    支持批量删除

##  Example


    curl -X POST "http://43.139.163.35:8081/api/v3/autoreply/group/setting" -i  -d '{"ids":[1]}'  -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:34:42 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 自动回复组列表查询
    不需要翻页

## Example

    curl -X GET "http://43.139.163.35:8081/api/v3/autoreply/group/setting" -i  -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:33:11 GMT
    Content-Length: 160

    {"code":200,"data":[{"id":2,"name":"测试组","is_del":0,"updated_time":"2023-07-26T22:31:41+08:00","created_time":"2023-07-26T22:31:41+08:00"}],"result":"ok"}



# 增加自动回复配置
    group_id: 组id，默认0，数据类型int
    type:类型 1文字、2图片，数据类型int
    question: 问题，数据类型string
    answer: 答案，数据类型string
    enable：true启动、false禁用

## example 


    curl -X POST "http://43.139.163.35:8081/api/v3/autoreply/setting" -i  -d '{"type":2, "question":"wenti", "answer":"daan" }'  -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:40:11 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 更新自动回复配置

    id: 配置ID，数据类型int
    group_id: 组id，默认0，数据类型int
    type:类型 1文字、2图片，数据类型int
    question: 问题，数据类型string
    answer: 答案，数据类型string
    enable：true启动、false禁用


## Example



    curl -X POST "http://43.139.163.35:8081/api/v3/autoreply/setting/update" -i  -d '{"id":1, "type":2, "question":"wenti", "answer":"daan" }'  -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:47:57 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 删除自动回复配置

    ids: 支持批量删除


## Example

    curl -X POST "http://43.139.163.35:8081/api/v3/autoreply/setting/del" -i  -d '{"ids":[1] }'  -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:49:24 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}


# 查询自动回复配置

    全量，不需要翻页

## Example

    curl -X GET "http://43.139.163.35:8081/api/v3/autoreply/setting" -i    -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" 
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Wed, 26 Jul 2023 14:53:11 GMT
    Content-Length: 228

    {"code":200,"data":[{"id":3,"group_id":0,"type":2,"account":"123","question":"wenti","answer":"daan","enable":null,"is_del":0,"updated_time":"2023-07-26T22:40:12+08:00","created_time":"2023-07-26T22:40:12+08:00"}],"result":"ok"}