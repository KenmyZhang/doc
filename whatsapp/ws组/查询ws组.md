# ws分组

# 参数

    全量返回，无入参


# Example

curl -X GET "http://18.163.48.157:8662/api/v1/ws/user/group/list" -H "Token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTUyODQ0NjV9.i_NpRkZ3yt6B5w3dT4td47zGuZDz1rnoG4_oMRX8j_c" -i -d '{"ids":[1]}'
HTTP/1.1 200 OK
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
Access-Control-Allow-Origin: *
Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
Content-Type: application/json; charset=utf-8
Date: Thu, 21 Sep 2023 09:20:16 GMT
Content-Length: 169

{"code":200,"data":[{"id":1,"name":"测试","customer":"123","is_del":"\u0001","update_time":"2023-09-21T09:15:51Z","create_time":"2023-09-21T09:14:38Z"}],"result":"ok"}