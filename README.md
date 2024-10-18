# 甲骨文设置

甲骨文如何关闭防火墙设置
- 方案一：Ubuntu系统
- 1、开放所有端口
```ssh
iptables -P INPUT ACCEPT
iptables -P FORWARD ACCEPT
iptables -P OUTPUT ACCEPT
iptables -F
```
