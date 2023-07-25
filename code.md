# 客服码生成

    account: 账号
    avatar: 头像
    link:链接

## Example

    curl -X POST "http://43.139.163.35:8188/api/v1/customer/service/code" -d '{"account":"123"}'  -i
    HTTP/1.1 200 OK
    Content-Type: application/json; charset=utf-8
    Trace-Id: 8271eb73-f6ea-4fd6-8de8-15129ac16dd1
    Date: Tue, 25 Jul 2023 10:00:29 GMT
    Content-Length: 313

    {
        "code":200,
        "data":{
            "account":"123",
            "avatar":"https://weidupic.kimways.com/data/20230318/users/6zwcapexzjnaen75aeanzwx8we/picnenue8pb3ins6gca3tg8n7a/111_preview.jpg?e=1689663937\u0026token=n9nESx5pgwYM4xhykHrA1A1LpxycVCd_PVusYeJF:h-8_SqkBBZ52U_Me5rE3Ekh0p2s=",
            "link":"http://www.baidu.com",
            "is_del":0
        },
        "result":"ok"
    }

# 客服码查询


## Example

    curl -X GET "http://43.139.163.35:8188/api/v1/customer/service/code?account=123"  -i
    HTTP/1.1 200 OK
    Content-Type: application/json; charset=utf-8
    Trace-Id: d3714df5-d2be-4117-ae0a-5b99a47bc9d5
    Date: Tue, 25 Jul 2023 10:09:33 GMT
    Content-Length: 316


    {
        "code":200,
        "data":{
            "account":"123",
            "avatar":"https://weidupic.kimways.com/data/20230318/users/6zwcapexzjnaen75aeanzwx8we/picnenue8pb3ins6gca3tg8n7a/111_preview.jpg?e=1689663937\u0026token=n9nESx5pgwYM4xhykHrA1A1LpxycVCd_PVusYeJF:h-8_SqkBBZ52U_Me5rE3Ekh0p2s=",
            "link":"http://www.baidu.com",
            "is_del":0
        },
        "result":"ok"
    }

# 统计

    "account": 账号
    "day": 日期
    "user_amount":用户数
    "reply_amount":回复数
    "valid_user_amount":有效用户数
    "valid_reply_amount":有效回复数

## Example

    curl -X GET "http://43.139.163.35:8188/api/v1/customer/statistics?account=123&page=1&page_num=10"  -i
    HTTP/1.1 200 OK
    Content-Type: application/json; charset=utf-8
    Trace-Id: 8b904763-0015-46f0-af9c-93dd1e284cc0
    Date: Tue, 25 Jul 2023 11:03:06 GMT
    Content-Length: 153

    {
        "code":200,
        "data":[
            {
                "account":"123",
                "day":"2023-09-10",
                "user_amount":10,
                "reply_amount":30,
                "valid_user_amount":7,
                "valid_reply_amount":20
            }
        ],
        "result":"ok"
    }



# 卡信息
    account 账号，支持多个，多个用逗号分隔
    valid_days 充值天数
    created_time 开卡时间
    expired_time 过期时间
    enable 是否启用

## Example


    curl -X GET "http://43.139.163.35:8188/api/v1/customer/accounts?account=123&page=1&page_num=10"  -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Trace-Id: 2915e503-fd2a-45f8-a262-813645c80f82
        Date: Tue, 25 Jul 2023 14:22:30 GMT
        Content-Length: 192

        {
            "code":200,
            "data":[
                {
                    "id":1,
                    "account":"123",
                    "password":"333",
                    "valid_days":3,
                    "enable":true,
                    "expired_time":"2023-09-12T00:00:00Z",
                    "created_time":"2023-08-12T00:00:00Z"
                }
            ],
            "result":"ok",
            "total":1
        }



# 用户数据


    account 账号，支持多个，多个用逗号分隔
    username 用户名
    avatar 用户头像
    register_time 注册时间
    IP IP信息
    address 地址
    device 设备信息
## Example 





    curl -X GET "http://43.139.163.35:8188/api/v1/customer/users?account=123&page=1&page_num=10"  -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Trace-Id: 0f9a0483-a07e-477c-9fdf-a65736d378e7
        Date: Tue, 25 Jul 2023 14:16:35 GMT
        Content-Length: 459
        
        {
            "code":200,
            "data":[
                {
                    "id":1,
                    "account":"123",
                    "username":"uname",
                    "avatar":"https://weidupic.kimways.com/data/20230318/users/6zwcapexzjnaen75aeanzwx8we/picnenue8pb3ins6gca3tg8n7a/111_preview.jpg?e=1689663937\u0026token=n9nESx5pgwYM4xhykHrA1A1LpxycVCd_PVusYeJF:h-8_SqkBBZ52U_Me5rE3Ekh0p2s=",
                    "register_time":"2023-09-12T00:00:00Z",
                    "client_ip":"124.240.78.58",
                    "address":"广东深圳",
                    "device":"iphone",
                    "os_version":"12",
                    "mobile":"huawei"
                }
            ],
            "result":"ok",
            "total":1
        }

# 自动同步

    from_account 被同步的账号， 数据类型string
    to_accounts 同步的账号，字符串数组
    include_avatar 是否包括头像
    include_name 是否包括名称
    include_say_hello 是否包括打招呼
    include_auto_reply 是否包括自动回复
    include_quick_message 是否包括快捷消息

## Example

    curl -X POST "http://43.139.163.35:8188/api/v1/customer/sync"  -d '{"from_account":"123", "to_accounts":["123"],"include_avatar":true, "include_name":true, "include_say_hello":true,"include_auto_reply":true,"include_quick_message":true }' -i
    HTTP/1.1 200 OK
    Content-Type: application/json; charset=utf-8
    Trace-Id: 33ed4df0-2473-4d82-93bc-23abef8bb437
    Date: Tue, 25 Jul 2023 14:28:38 GMT
    Content-Length: 26

    {"code":200,"result":"ok"}