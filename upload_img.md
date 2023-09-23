# 上传图片

	imgfile:文件路径

## Example

	curl -X POST "http://43.139.163.35:8081/api/v3/image/upload" -i \
	 -H "token:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhY2NvdW50IjoiMTIzIiwiY3JlYXRlX3RpbWUiOjE2OTAzNzQwNDh9.v8EnBzvNZ9lPotme6RxevBMQfxw9HQkum3tQeBWKAMg" \
	 -F imgfile=@"/Users/Downloads/小程序.png"
	HTTP/1.1 100 Continue

	HTTP/1.1 200 OK
	Access-Control-Allow-Credentials: true
	Access-Control-Allow-Headers: Authorization, Content-Length, X-CSRF-Token, Token,session
	Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE,UPDATE
	Access-Control-Allow-Origin: *
	Access-Control-Expose-Headers: Content-Length, Access-Control-Allow-Origin, Access-Control-Allow-Headers
	Content-Type: application/json; charset=utf-8
	Date: Wed, 26 Jul 2023 12:47:43 GMT
	Content-Length: 114

	{"code":200,"msg":"上传成功!","result":{"path":"static/upload/2023July/e1a9571dc97cd15ac11e4edb5ce5d4d9.png"}}
