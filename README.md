登入cloudflare

右上角点头像，点My Profile，最下面Global API Key就是你的API_KEY

进入域名设置，overview下，右下角Zone ID就是你的Zone ID

----------

获取CFid命令

找个linux系统比如debian
```
apt install -y curl python
```
```
curl -X GET "https://api.cloudflare.com/client/v4/zones/修改为你的zone_id/dns_records" -H "X-Auth-Email: 修改为你的Email" -H "X-Auth-Key: 修改为你的API_KEY" -H "Content-Type: application/json" | python -mjson.tool
```
显示结果中
"content": "你的顶级域名"
紧接着下面第二行
"id": "xxxxxxxxxxxxxxxxxxxxxxxxxxxx"
就是你需要的CFid
