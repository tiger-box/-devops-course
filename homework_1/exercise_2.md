# 2. Создать именованный пайп ( named pipe ). Вывести в файл через созданный pipe вывод команды ss -plnt

```bash
[root@DevOps-Tutorial ~]# mkfifo my_pipe
[root@DevOps-Tutorial ~]# ls - l
total 0
prw-r--r--. 1 root root 0 Nov 20 07:43 my_pipe 
[root@DevOps-Tutorial ~]# ss -plnt> my_pipe
```

## Используем 2-консоль

```bash
[root@DevOps-Tutorial ~]# cat my_pipe > output.txt
[root@DevOps-Tutorial ~]# ls -l
total 4
prw-r--r--. 1 root root   0 Nov 20 07:45 my_pipe
-rw-r--r--. 1 root root 154 Nov 20 07:45 output.txt
[root@DevOps-Tutorial ~]# cat output.txt
```

## Результат

```bash
State  Recv-Q Send-Q Local Address:Port Peer Address:PortProcess
LISTEN 0      128          0.0.0.0:22        0.0.0.0:*    users:(("sshd",pid=1121,fd=5))
```
