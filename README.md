登入cloudflare

API_KEY：右上角点头像，点My Profile，最下面Global API Key

Zone ID：进入域名设置，overview下，右下角Zone ID

----------

获取CFid命令

找个linux系统比如debian
```
apt install -y curl python
```
```
curl -X GET "https://api.cloudflare.com/client/v4/zones/修改为zone_id/dns_records" -H "X-Auth-Email: 修改为Email" -H "X-Auth-Key: 修改为API_KEY" -H "Content-Type: application/json" | python -mjson.tool
```
显示结果中

"content": "顶级域名"

紧接着下面第二行

"id": "xxxxxxxxxxxxxxxxxxxxxxxxxxxx"

就是你需要的CFid
