# Вывести дату в unixtime На вход команды date через пайп подать свой формат выводимой даты

```bash
[root@DevOps-Tutorial ~]# echo "2024-11-21 11:10:00" | xargs -I {} date -d "{}" +%s | tee time.txt
1732187400b 
```
