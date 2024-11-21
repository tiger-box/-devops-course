# 1. Узнать IP-адрес интерфейса, подключенного к сети Интернет

```bash
[root@DevOps-Tutorial ~]# ip addr | grep inet | grep -v 127.0.0.1
inet 93.183.73.99/24 brd 93.183.73.255 scope global noprefixroute enp0s5
```
