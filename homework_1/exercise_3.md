# 3. При помощи именованного пайпа заархивировать всё, что в него отправляем

```bash
[root@DevOps-Tutorial ~]# mkfifo /tmp/archived_pipe
[root@DevOps-Tutorial ~]# tar czf /tmp/archived_messages.tar.gz -C /var/log messages < /tmp/archived_pipe &
[1] 96503
[root@DevOps-Tutorial ~]# cat /var/log/messages > /tmp/archived_pipe
```
