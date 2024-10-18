# 甲骨文设置

甲骨文如何关闭防火墙设置
- 方案一：Ubuntu系统

1、开放所有端口
```ssh
iptables -P INPUT ACCEPT
iptables -P FORWARD ACCEPT
iptables -P OUTPUT ACCEPT
iptables -F
```
2、关闭或强制删除防火墙
```ssh
apt-get purge netfilter-persistent && reboot
或 rm -rf /etc/iptables && reboot
```
- 方案二：Centos系统

1、删除多余附件
```ssh
systemctl stop oracle-cloud-agent
systemctl disable oracle-cloud-agent
systemctl stop oracle-cloud-agent-updater
systemctl disable oracle-cloud-agent-updater
```
2、停止firewall并禁止自启动
```ssh
systemctl stop firewalld.service
systemctl disable firewalld.service
```
