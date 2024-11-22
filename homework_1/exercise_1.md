# 1. Узнать IP-адрес интерфейса, подключенного к сети Интернет

```bash
[root@DevOps-Tutorial ~]# ip address
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
2: enp0s5: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether ca:0b:eb:28:8a:49 brd ff:ff:ff:ff:ff:ff
    inet 93.183.73.99/24 brd 93.183.73.255 scope global noprefixroute enp0s5
       valid_lft forever preferred_lft forever
[root@DevOps-Tutorial ~]# hostname -I | awk '{print $0}'
93.183.73.99
[root@DevOps-Tutorial ~]#
```
