# logger записать в общий журнал послание добра и мира посланникам из Альфа-Центавра с *facility kernel*

При помощи команды **logger** c приоритетом **info**

```bash
[root@DevOps-Tutorial ~]# logger -p kern.info "Послание добра и мира посланникам из Альфа-Центавра"
[root@DevOps-Tutorial ~]#
```

с помощью **journalctl** и **grep** - находим сообщение в общем журнале.

```bash
[root@DevOps-Tutorial ~]# journalctl | grep "Послание добра и мира посланникам из Альфа-Центавра"
Dec 02 10:14:18 DevOps-Tutorial.local root[314040]: Послание добра и мира посланникам из Альфа-Центавра
[root@DevOps-Tutorial ~]#
```

Есть другой другой способ. Это способ показывает в каком приоритете было отправлено сообщение

```bash
[root@DevOps-Tutorial ~]# journalctl -p info | grep "Послание"
Dec 02 10:14:18 DevOps-Tutorial.local root[314040]: Послание добра и мира посланникам из Альфа-Центавра
[root@DevOps-Tutorial ~]#
```

Можно прочитать через **cat**  и  **grep**.

```bash
[root@DevOps-Tutorial ~]# cat /var/log/messages |grep "Послание"
Dec  2 10:14:18 DevOps-Tutorial root[314040]: Послание добра и мира посланникам из Альфа-Центавра
[root@DevOps-Tutorial ~]#
```
