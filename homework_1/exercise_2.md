# 2. Создать именованный пайп ( named pipe ). Вывести в файл через созданный pipe вывод команды ss -plnt

```bash
[root@DevOps-Tutorial ~]# mkfifo my_pipe // тут создали pipe 
[root@DevOps-Tutorial ~]# ls -l // проверка на создание  pipe
total 16
-rw-r--r--. 1 root root  19 Nov 21 08:55 eof.txt
prw-r--r--. 1 root root   0 Nov 22 13:21 my_pipe // как видим он  создал pipe prw - p > означате pipe
-rw-r--r--. 1 root root 154 Nov 22 13:17 output.txt
-rw-r--r--. 1 root root 154 Nov 22 13:08 tee
-rw-r--r--. 1 root root  11 Nov 21 08:14 time.txt
[root@DevOps-Tutorial ~]# ss -plnt > my_pipe & // вывод команды ss -plnt в pipe  
[1] 143435
[root@DevOps-Tutorial ~]# cat my_pipe > output.txt // Читает данные из именованного пайпа и записывает в файл
[1]+  Done                    ss -plnt > my_pipe
[root@DevOps-Tutorial ~]# ls -l // проверяем 
total 16
-rw-r--r--. 1 root root  19 Nov 21 08:55 eof.txt
prw-r--r--. 1 root root   0 Nov 22 13:23 my_pipe
-rw-r--r--. 1 root root 154 Nov 22 13:23 output.txt
-rw-r--r--. 1 root root 154 Nov 22 13:08 tee
-rw-r--r--. 1 root root  11 Nov 21 08:14 time.txt
[root@DevOps-Tutorial ~]# cat output.txt // читаем файл и видем результат
State  Recv-Q Send-Q Local Address:Port Peer Address:PortProcess
LISTEN 0      128          0.0.0.0:22        0.0.0.0:*    users:(("sshd",pid=1121,fd=5))
[root@DevOps-Tutorial ~]# rm -rf my_pipe // удаляем pipe
```
