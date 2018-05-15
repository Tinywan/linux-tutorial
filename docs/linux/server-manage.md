Linux网络管理
========================

简介：本课程会为你解决Linux网络配置的问题。首先会介绍网络基础知识，然后进行IP地址的配置，并总结了在配置网络环境中经常遇到的问题，最后介绍了几种常用远程登录工具的使用，如XShell和SecureCRT。 


## 第一章 网络基础 

#### 1-1 七层模型 
* ISO：国际标准化组织
* OSI：开放系统互联网模型 [ 物理层，数据链路层，网络层，传输层，会话层，表示层，应用层 ]
* IOS：苹果操作系统

* 应用层：用户接口
* 表示层：数据的表现形式、特定功能的实现，如加密，压缩
* 会话层：对应用会话的管理、同步
* 传输层：可靠与不可靠的传输（TCP/UDP），传输前的错误检测、流控（确定传输协议）
* 网络层：提供逻辑地址、选路
* 数据链路层：成帧，用Mac地址访问媒介，错误检测与修正
* 物理层：设备之间的比特流的传输，物理接口，电气特性等

7 应用层：老板
6 表示层：相当于公司中演示稿老板、替老板写信的助理
5 会话层：相当于公司中收寄信、写信封与拆信封的秘书
4 传输层：相当于公司中跑邮局的送信职员
3 网络层：相当于邮局中的排序工人
2 数据链路层：相当于邮局中的装拆箱工人
1 物理层：相当于邮局中的搬运工人

#### 1-2 TCP/IP四层模型
* 应用层（上三层）：（FTP，）
* 传输层：TCP（安全、慢），UDP（快、会丢失）
* 国际互联层：IP，IGMP，ICMP
* 网络接入层（下两层）：

#### 1-3 IP

#### 1-3 端口

#### 1-4 域名
C:\Windows\System32\drivers\etc

#### 1-5 网关的作用
网关：Gateway，网间连接器、协议转换器，在网络层以上实现网络互连，是最复杂的网络互连设备，仅用户两个高层协议不同的网络互连。


## 第二章 Linux网络配置 

#### 2-1 IP地址配置
* ifconfig命令：
* 临时设置网络IP：ifconfig eth0 192.168.254.200 netmask 255.255.255.0
* 配置文件设置IP：vi /etc/sysconfig/network-scripts/ifcfg-ens33

# 类型为以太网
TYPE=Ethernet
# 是否自动获取IP（none/static/dhcp）
BOOTPROTO=dhcp
DEFROUTE=yes
PEERDNS=yes
PEERROUTES=yes
IPV4_FAILURE_FATAL=no
IPV6INIT=yes
IPV6_AUTOCONF=yes
IPV6_DEFROUTE=yes
IPV6_PEERDNS=yes
IPV6_PEERROUTES=yes
IPV6_FAILURE_FATAL=no
IPV6_ADDR_GEN_MODE=stable-privacy
NAME=ens33
# 唯一识别码
UUID=e5aaeb5f-91d1-4375-834b-45d9576f5526
# 网卡设备名
DEVICE=ens33
# IP地址
IPADDR=192.169.0.252
# 子网掩码
NETMASK=255.255.255.0
# 网关
GATEWAY=192.168.0.1
# DNS
DNS1=114.114.114.114
# 不允许非root用户控制此网卡
USERCTL=no
# 是否随网络服务启动，ens33生效
ONBOOT=yes

#### 2-2 主机名配置
* vi /etc/sysconfig/network
NETWORKING=yes
HOSTNAME=localhost.localdomain

#### 2-3 DNS
* vi /etc/resolv.conf
nameserver 202.106.0.20
search localhost


## 第三章 Linux网络命令



## 第四章 远程登录工具
