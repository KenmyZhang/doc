## 账号列表

## 参数
    group_id 组id
    page: 第几页
    page_num: 每页返回账号数量

## Example 


    curl -X GET "http://0:8081/api/v1/ws/user/list?group_id=1&page=1&page_num=2" -H "Token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTUyODQ0NjV9.i_NpRkZ3yt6B5w3dT4td47zGuZDz1rnoG4_oMRX8j_c" -i
    HTTP/1.1 200 OK
    Access-Control-Allow-Credentials: true
    Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
    Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
    Access-Control-Allow-Origin: *
    Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
    Content-Type: application/json; charset=utf-8
    Date: Thu, 21 Sep 2023 08:47:03 GMT
    Content-Length: 283

    {"code":200,"data":[{"id":1,"group_id":1,"customer":"123","status":0,"mobile":"123","cookie":"","create_time":"2023-09-21T16:44:29+08:00"},{"id":2,"group_id":1,"customer":"123","status":0,"mobile":"123","cookie":"","create_time":"2023-09-21T16:46:02+08:00"}],"result":"ok","total":2}

