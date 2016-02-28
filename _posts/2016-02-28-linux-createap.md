---
layout: post
title: linux下创建热点
subtitle: create_ap
header-img: 
tags: [linux]
categories: [linux]
---
# linux创建热点

***

## create_ap

先甩个链接：

>https://github.com/oblique/create_ap

安装就不说了.


* 首先先查看你的网卡

~~~
~ » ifconfig                                                         
enp2s0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        ether 20:89:84:97:0d:ac  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 972  bytes 53280 (52.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 972  bytes 53280 (52.0 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlp3s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.202.36.11  netmask 255.255.252.0  broadcast 10.202.39.255
        inet6 fe80::26fd:52ff:fe74:c002  prefixlen 64  scopeid 0x20<link>
        ether 24:fd:52:74:c0:02  txqueuelen 1000  (Ethernet)
        RX packets 35414  bytes 17903776 (17.0 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 14346  bytes 1851081 (1.7 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

~~~

可以看到网卡是enp2s0和wlp3s0，wlp3s0是无线网卡.

***

## Examples

* No passphrase (open network):

>create_ap wlan0 eth0 MyAccessPoint

我对应的命令就是

~~~
sudo create_ap wlp3s0 enp2s0 MyAccessPoint
~~~

那么带密码：

* WPA + WPA2 passphrase:

~~~
sudo create_ap wlp3s0 enp2s0 MyAccessPoint MyPassPhrase
~~~

* Internet sharing from the same WiFi interface:

~~~
sudo create_ap wlp3s0 wlp3s0 MyAccessPoint MyPassPhrase
~~~
感觉常用的就这三个.
