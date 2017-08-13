# wfg
## 极路由更新  
### 本地更新dnsmasq.conf

使用项目 [gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq.git) 中的脚本即可

```bash
# Run this under linux shell
git clone https://github.com/totogo/wfg.git
cd wfg
./g2d.sh --port 53535 -o gw-shadowsocks.dnslist --extra-domain-file extra-domain.txt

# 复制 gw-shadowsocks.dnslist 到 hiwifi-ss/etc/gw-shadowsocks/gw-shadowsocks.dnslist 打包
# 或者，直接复制到极路由 /etc/gw-shadowsocks/gw-shadowsocks.dnslist 上
```

Login to Geewan

```bash
ssh root@10.1.199.1 -p 1022
```

Copy file to Geewan

```bash
scp -P 1022 gw-shadowsocks.dnslist root@10.1.199.1:/etc/gw-shadowsocks/gw-shadowsocks.dnslist
```
