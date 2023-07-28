# 获取长链接ws

    content：消息内容
    content_type: 内容类型， 0和1文字、2图片、3 位置、 4、视频
    group_id: 群组ID
    group_name: 群组名称
    msg_id:消息id
    id: 发送用户ID
    to_id:接收用户ID
    time:发送时间
    name:发送用户名称
    avator： 发送用户头像


## Example

    curl 'ws://43.139.163.35:8081/api/v3/visitor/ws?visitor_id=10dff9ba-2ff1-42a0-8797-3c75548815d7' \
  -H 'Pragma: no-cache' \
  -H 'Origin: http://43.139.163.35:8081' \
  -H 'Accept-Language: zh-CN,zh;q=0.9' \
  -H 'Sec-WebSocket-Key: z+Py543Qu1jjjSnRNPT7hg==' \
  -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/115.0.0.0 Safari/537.36' \
  -H 'Upgrade: websocket' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: Upgrade' \
  -H 'Sec-WebSocket-Version: 13' \
  -H 'Sec-WebSocket-Extensions: permessage-deflate; client_max_window_bits' \
  --compressed




    接收到的消息
    {
        "type":"message",
        "data":{
            "name":"智能客服系统",
            "avator":"/static/images/4.jpg",
            "id":"kefu2",
            "visitor_id":"",
            "group_name":"",
            "group_id":0,
            "time":"2023-07-27 15:14:44",
            "to_id":"10dff9ba-2ff1-42a0-8797-3c75548815d7",
            "content":"你好1222",
            "msg_id":19,
            "content_type":0,
            "city":"",
            "client_ip":"",
            "refer":"",
            "is_kefu":"no"
        }
    }





   客户端发送ping
  {
      "type":"ping",
      "data":"visitor:10dff9ba-2ff1-42a0-8797-3c75548815d7"
  }

   服务端返回
   {
      "type":"pong",
      "data":null
    }


    2min钟没有发送消息，发送关闭event，发送消息检查到断链，提示“连接关闭!请重新打开页面”
    {
        "type":"auto_close",
        "data":"10dff9ba-2ff1-42a0-8797-3c75548815d7"
    }
