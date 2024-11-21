# При помощи HEREDOC записать в файл многострочное сообщение

```bash
[root@DevOps-Tutorial ~]# cat << EOF | tee eof.txt   > здесь сразу показано записанного файла
> hello
> world
> DevOps
> EOF
hello
world
DevOps
[root@DevOps-Tutorial ~]# ls
eof.txt  my_pipe  time.txt
[root@DevOps-Tutorial ~]#
```
