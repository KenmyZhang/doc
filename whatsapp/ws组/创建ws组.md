## 创建ws分组

## 参数


    name 组名

## Example 


    curl -X POST "http://18.163.48.157:8662/api/v1/ws/user/group" -H "Token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTUyODQ0NjV9.i_NpRkZ3yt6B5w3dT4td47zGuZDz1rnoG4_oMRX8j_c" -i -d '{"name":"测试"}'
HTTP/1.1 200 OK
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
Access-Control-Allow-Origin: *
Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
Content-Type: application/json; charset=utf-8
Date: Thu, 21 Sep 2023 09:14:38 GMT
Content-Length: 181

{"code":200,"data":{"id":1,"name":"测试","customer":"123","is_del":"","update_time":"2023-09-21T09:14:38.115247976Z","create_time":"2023-09-21T09:14:38.115247976Z"},"result":"ok"}