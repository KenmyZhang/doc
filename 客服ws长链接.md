# 客服长链接

## Example 

    curl 'ws://43.139.163.35:8081/ws_kefu?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjcmVhdGVfdGltZSI6MTY5MDYwNTM2MSwia2VmdV9pZCI6MSwibmFtZSI6ImtlZnUyIiwicm9sZV9pZCI6MSwidHlwZSI6ImtlZnUifQ.arbBhTdhCraq-zkF8Lxu59kl0pHJy7tbRGxfprx18Mk' \
    -H 'Pragma: no-cache' \
    -H 'Origin: http://43.139.163.35:8081' \
    -H 'Accept-Language: zh-CN,zh;q=0.9' \
    -H 'Sec-WebSocket-Key: EXBmjRWGAQBDTDefjHtvOA==' \
    -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/115.0.0.0 Safari/537.36' \
    -H 'Upgrade: websocket' \
    -H 'Cache-Control: no-cache' \
    -H 'Connection: Upgrade' \
    -H 'Sec-WebSocket-Version: 13' \
    -H 'Sec-WebSocket-Extensions: permessage-deflate; client_max_window_bits' \
    --compressed


    发送到服务端

    {
        "type":"ping",
        "data":""
    }

    {
        "type":"kfConnect",
        "data":{
            "id":"kefu2",
            "name":"智能客服系统",
            "avator":"/static/images/4.jpg",
            "to_id":"10dff9ba-2ff1-42a0-8797-3c75548815d7"
        }
    }


    {
        "type":"kfOnline",
        "data":{
            "id":"kefu2",
            "name":"智能客服系统",
            "avator":"/static/images/4.jpg",
            "to_id":""
        }
    }

    服务端返回

    {
        "type":"pong",
        "data":null
    }


    {
        "type":"userOffline",
        "data":{
            "name":"中国广东深圳网友",
            "uid":"7da7d62d-ef94-4672-bc77-fea151baa812"
        }
    }

    {
        "type":"userOnline",
        "data":{
            "avator":"http://43.139.163.35:8081/static/upload/2023July/8deb53dc7aa149239e3f0f629e21795f.png",
            "last_message":"hhhh你好",
            "uid":"10dff9ba-2ff1-42a0-8797-3c75548815d7",
            "username":"中国广东深圳网友"
        }
    }

    {
        "type":"notice",
        "data":{
            "avator":"http://43.139.163.35:8081/static/upload/2023July/8deb53dc7aa149239e3f0f629e21795f.png","content":"中国广东深圳网友来了",
            "username":"中国广东深圳网友"
        }
    }



    name:用户名称
    avator:用户头像
    id：发送方id
    group_name:群组名称，当type=2,群聊当时候才有值
    group_id:群组id，当type=2,群聊当时候才有值
    type:  消息类型： 0 好友 1 群聊 2 系统消息
    time:消息时间
    to_id:接收方id/客服ID
    content:消息内容
    msg_id: 消息ID
    content_type: 内容类型 1 文字、2 图片、 3地址、4 视频 、5 音频
    city: 城市
    client_ip: 用户IP
    



    {
        "type":"message",
        "data":{
            "name":"中国广东深圳网友",
            "avator":"static/upload/2023July/8deb53dc7aa149239e3f0f629e21795f.png",
            "id":"10dff9ba-2ff1-42a0-8797-3c75548815d7",
            "group_name":"",
            "group_id":0,
            "type":1,
            "time":"2023-07-29 13:29:41",
            "to_id":"kefu2",
            "content":"hhhh你好",
            "msg_id":236,
            "content_type":2,
            "city":"",
            "client_ip":"",
            "refer":"",
            "is_kefu":"no"
        }
    }
