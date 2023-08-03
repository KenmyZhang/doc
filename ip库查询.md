# ip库查询

## Example 

    curl -X GET "http://127.0.0.1:8081/api/v3/ip/datas?page=1&page_num=3" 
   


    {
            "code": 500,
            "data": [{
                "id": 1,
                "ip": "117.188.55.214",
                "continent": "亚洲",
                "country": "中国",
                "zipcode": "563000",
                "timezone": "UTC+8",
                "accuracy": "区县",
                "owner": "中国移动",
                "isp": "中国移动",
                "source": "数据挖掘",
                "areacode": "CN",
                "adcode": "520302",
                "asnumber": "9808",
                "lat": "27.667669",
                "lng": "106.912441",
                "radius": "39.7073",
                "prov": "贵州省",
                "city": "遵义市",
                "district": "红花岗区",
                "create_time": "2023-08-02T18:09:13+08:00"
            }],
            "result": "ok",
            "total": 678
        }