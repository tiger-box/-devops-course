# Отразить 7 последних строк из: *wtmp,last*

## WTMP

Так как **WTMP** являеться бинарным файлом, то конечно будет такой результат.

```bash
[root@DevOps-Tutorial log]# cat wtmp
0ttyS0tyS00;�*cA1tty1tty11;�*c11~~~shutdown5.4.17-2136.310.7.1.el8uek.x86_64;�*c�-~~~reboot5.4.17-2136.310.7.1.el8uek.x86_643g>3~~~runlevel5.4.17-2136.310.7.1.el8uek.x86_643gw�
                                                        Otty1tty1O3g��PttyS0tyS0P3g��PttyS0tyS0LOGINP3g��Otty1tty1LOGINO3g���pts/0ts/0root147.45.170.252�3g�Y�-��pts/08;3gS�pts/0ts/0root147.45.170.252N3ghP
��pts/0ts/0root88.201.206.219z:7gT�X����pts/1ts/1root147.45.170.252Q>7gߢ�-���pts/0�Y7�pts/1�7g�&g�
                                                                                                =pts/0ts/0root147.45.170.252��<g#h      �-��
                   =pts/0�<g␦i?pts/0ts/0root147.45.170.252�<g�U
�-�i?pts/0��<g�
               �bpts/0ts/0root147.45.170.252�|=g�f
                                                  �-��ipts/1ts/1root147.45.170.252��=gU_�-���ipts/2ts/2root147.45.170.252z�=g<L
�-��bpts/0�=gt�ipts/0ts/0root147.45.170.252Q�=g:�-��ipts/2_�=gipts/1��=g��ipts/0��=g' 0upts/0ts/0root147.45.170.252z>g���-���vpts/1ts/1root88.201.206.2194>gW�
                                      X���vpts/16>gy�           wpts/1ts/1root88.201.206.219A>g�JX����xpts/2ts/2root88.201.206.219�>gO�X����ypts/3ts/3root88.201.206.219�>g�X���ypts/3␦>g]�
                                                                   �ypts/3ts/3root88.201.206.219␦>g3�
                                                                                                     X���ypts/3F␦>gZ��yp�pts/0ts/0root147.45.170.252��>g���-���pts/1ts/1root88.201.206.219g?g>X���pts/0%?gx�
9&pts/0ts/0root147.45.170.252`@g�                                                  �pts/1�.?g�"
��pts/0ts/0root147.45.170.252!)Gg��-���pts/0FXGgPq�-pts/L�pts/0ts/0root147.45.170.252�9Hg�B�-��[root@DevOps-Tutorial log]#
[root@DevOps-Tutorial log]#

```

Для удобства, помощью **xxd wtmp | tail -7**, преобразуем бинарный файл в 16-ю систему счисления с выводом 7 последних строк

```bash
[root@DevOps-Tutorial log]# xxd wtmp | tail -7
00005390: 0000 0000 0000 0000 0000 0000 0000 0000  ................
000053a0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
000053b0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
000053c0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
000053d0: 0000 0000 ee39 4867 c642 0100 932d aafc  .....9Hg.B...-..
000053e0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
000053f0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
[root@DevOps-Tutorial log]#
```

Другой способ с использованием комманды **hexdump | tail -7**

```bash
[root@DevOps-Tutorial log]# hexdump wtmp | tail -7
00052d0 3534 312e 3037 322e 3235 0000 0000 0000
00052e0 0000 0000 0000 0000 0000 0000 0000 0000
*
00053d0 0000 0000 39ee 6748 42c6 0001 2d93 fcaa
00053e0 0000 0000 0000 0000 0000 0000 0000 0000
*
0005400
[root@DevOps-Tutorial log]#
```

Преобразуем бинарный файл в читаемый текст, с помощью команды **utmpdump wtmp  | tail -7**

```bash
[root@DevOps-Tutorial log]# utmpdump wtmp  | tail -7
Utmp dump of wtmp
[7] [142135] [ts/0] [root    ] [pts/0       ] [147.45.170.252      ] [147.45.170.252 ] [2024-11-22T12:36:26,564550+00:00]
[8] [142135] [    ] [        ] [pts/0       ] [                    ] [0.0.0.0        ] [2024-11-22T13:00:04,936119+00:00]
[7] [142834] [ts/0] [root    ] [pts/0       ] [147.45.170.252      ] [147.45.170.252 ] [2024-11-22T13:00:13,991932+00:00]
[8] [142834] [    ] [        ] [pts/0       ] [                    ] [0.0.0.0        ] [2024-11-22T17:52:17,882458+00:00]
[7] [234391] [ts/0] [root    ] [pts/0       ] [147.45.170.252      ] [147.45.170.252 ] [2024-11-27T14:13:53,574455+00:00]
[8] [234391] [    ] [        ] [pts/0       ] [                    ] [0.0.0.0        ] [2024-11-27T17:35:02,618832+00:00]
[7] [253260] [ts/0] [root    ] [pts/0       ] [147.45.170.252      ] [147.45.170.252 ] [2024-11-28T09:37:50,082630+00:00]
[root@DevOps-Tutorial log]#
```

## LAST

использовано камнда **last**

```bash
[root@DevOps-Tutorial ~]# last
root     pts/0        147.45.170.252   Thu Nov 28 09:37   still logged in
root     pts/0        147.45.170.252   Wed Nov 27 14:13 - 17:35  (03:21)
root     pts/0        147.45.170.252   Fri Nov 22 13:00 - 17:52  (04:52)
root     pts/0        147.45.170.252   Fri Nov 22 12:36 - 13:00  (00:23)
root     pts/0        147.45.170.252   Fri Nov 22 10:42 - 12:36  (01:53)
root     pts/1        88.201.206.219   Thu Nov 21 10:58 - 12:59  (02:00)
root     pts/0        147.45.170.252   Thu Nov 21 07:01 - 11:23  (04:21)
root     pts/3        88.201.206.219   Wed Nov 20 17:20 - 19:21  (02:01)
root     pts/3        88.201.206.219   Wed Nov 20 17:18 - 17:20  (00:01)
root     pts/3        88.201.206.219   Wed Nov 20 17:18 - 17:18  (00:00)
root     pts/2        88.201.206.219   Wed Nov 20 17:08 - 19:10  (02:01)
root     pts/1        88.201.206.219   Wed Nov 20 16:37 - 18:50  (02:13)
root     pts/1        88.201.206.219   Wed Nov 20 16:37 - 16:37  (00:00)
root     pts/0        147.45.170.252   Wed Nov 20 15:51 - 18:06  (02:14)
root     pts/0        147.45.170.252   Wed Nov 20 07:40 - 09:57  (02:17)
root     pts/2        147.45.170.252   Wed Nov 20 07:36 - 07:44  (00:08)
root     pts/1        147.45.170.252   Wed Nov 20 07:28 - 09:57  (02:28)
root     pts/0        147.45.170.252   Wed Nov 20 06:07 - 07:38  (01:31)
root     pts/0        147.45.170.252   Tue Nov 19 18:20 - 18:49  (00:28)
root     pts/0        147.45.170.252   Tue Nov 19 14:45 - 17:51  (03:05)
root     pts/1        147.45.170.252   Fri Nov 15 12:28 - 21:19  (08:51)
root     pts/0        88.201.206.219   Fri Nov 15 12:11 - 14:25  (02:13)
root     pts/0        147.45.170.252   Tue Nov 12 16:16 - 19:41  (03:24)
root     pts/0        147.45.170.252   Tue Nov 12 08:46 - 11:25  (02:39)
reboot   system boot  5.4.17-2136.310. Tue Nov 12 07:49   still running

wtmp begins Wed Sep 21 08:11:39 2022
[root@DevOps-Tutorial ~]#
```

```bash
[root@DevOps-Tutorial ~]# last | tail -7
root     pts/1        147.45.170.252   Fri Nov 15 12:28 - 21:19  (08:51)
root     pts/0        88.201.206.219   Fri Nov 15 12:11 - 14:25  (02:13)
root     pts/0        147.45.170.252   Tue Nov 12 16:16 - 19:41  (03:24)
root     pts/0        147.45.170.252   Tue Nov 12 08:46 - 11:25  (02:39)
reboot   system boot  5.4.17-2136.310. Tue Nov 12 07:49   still running

wtmp begins Wed Sep 21 08:11:39 2022
[root@DevOps-Tutorial ~]#
```
