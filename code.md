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