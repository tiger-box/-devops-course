# Посмотреть последние 25 строчек лога сервиса  *systemd-logind*

При помощи команды **journalctl -u systemd-logind | tail -25**

```bash
[root@DevOps-Tutorial ~]# journalctl -u systemd-logind | tail -25
Nov 29 10:18:20 DevOps-Tutorial.local systemd-logind[672]: New session 43 of user root.
Nov 29 12:34:29 DevOps-Tutorial.local systemd-logind[672]: Session 43 logged out. Waiting for processes to exit.
Nov 29 12:34:29 DevOps-Tutorial.local systemd-logind[672]: Removed session 43.
Nov 29 14:08:18 DevOps-Tutorial.local systemd-logind[672]: New session 45 of user root.
Nov 29 16:34:44 DevOps-Tutorial.local systemd-logind[672]: New session 47 of user root.
Nov 29 18:09:12 DevOps-Tutorial.local systemd-logind[672]: Session 45 logged out. Waiting for processes to exit.
Nov 29 18:09:12 DevOps-Tutorial.local systemd-logind[672]: Removed session 45.
Nov 29 19:02:43 DevOps-Tutorial.local systemd-logind[672]: Session 47 logged out. Waiting for processes to exit.
Nov 29 19:02:43 DevOps-Tutorial.local systemd-logind[672]: Removed session 47.
Nov 30 10:33:34 DevOps-Tutorial.local systemd-logind[672]: New session 48 of user root.
Nov 30 18:50:19 DevOps-Tutorial.local systemd-logind[672]: Session 48 logged out. Waiting for processes to exit.
Nov 30 18:50:19 DevOps-Tutorial.local systemd-logind[672]: Removed session 48.
Dec 01 10:22:13 DevOps-Tutorial.local systemd-logind[672]: New session 50 of user root.
Dec 01 15:39:52 DevOps-Tutorial.local systemd-logind[672]: Session 50 logged out. Waiting for processes to exit.
Dec 01 15:39:52 DevOps-Tutorial.local systemd-logind[672]: Removed session 50.
Dec 02 08:22:15 DevOps-Tutorial.local systemd-logind[672]: New session 52 of user root.
Dec 02 12:57:17 DevOps-Tutorial.local systemd-logind[672]: Session 52 logged out. Waiting for processes to exit.
Dec 02 12:57:17 DevOps-Tutorial.local systemd-logind[672]: Removed session 52.
Dec 02 14:06:28 DevOps-Tutorial.local systemd-logind[672]: New session 54 of user root.
Dec 02 14:24:39 DevOps-Tutorial.local systemd-logind[672]: Session 54 logged out. Waiting for processes to exit.
Dec 02 14:24:39 DevOps-Tutorial.local systemd-logind[672]: Removed session 54.
Dec 02 14:25:33 DevOps-Tutorial.local systemd-logind[672]: New session 56 of user root.
Dec 02 14:27:18 DevOps-Tutorial.local systemd-logind[672]: Session 56 logged out. Waiting for processes to exit.
Dec 02 14:27:18 DevOps-Tutorial.local systemd-logind[672]: Removed session 56.
Dec 02 14:36:38 DevOps-Tutorial.local systemd-logind[672]: New session 58 of user root.
[root@DevOps-Tutorial ~]#
```

Без использование  **tail**

```bash
[root@DevOps-Tutorial ~]# journalctl -u systemd-logind -n 25
-- Logs begin at Tue 2024-11-12 07:49:43 UTC, end at Mon 2024-12-02 15:32:26 UTC. --
Nov 29 10:18:20 DevOps-Tutorial.local systemd-logind[672]: New session 43 of user root.
Nov 29 12:34:29 DevOps-Tutorial.local systemd-logind[672]: Session 43 logged out. Waiting for processes to exit.
Nov 29 12:34:29 DevOps-Tutorial.local systemd-logind[672]: Removed session 43.
Nov 29 14:08:18 DevOps-Tutorial.local systemd-logind[672]: New session 45 of user root.
Nov 29 16:34:44 DevOps-Tutorial.local systemd-logind[672]: New session 47 of user root.
Nov 29 18:09:12 DevOps-Tutorial.local systemd-logind[672]: Session 45 logged out. Waiting for processes to exit.
Nov 29 18:09:12 DevOps-Tutorial.local systemd-logind[672]: Removed session 45.
Nov 29 19:02:43 DevOps-Tutorial.local systemd-logind[672]: Session 47 logged out. Waiting for processes to exit.
Nov 29 19:02:43 DevOps-Tutorial.local systemd-logind[672]: Removed session 47.
Nov 30 10:33:34 DevOps-Tutorial.local systemd-logind[672]: New session 48 of user root.
Nov 30 18:50:19 DevOps-Tutorial.local systemd-logind[672]: Session 48 logged out. Waiting for processes to exit.
Nov 30 18:50:19 DevOps-Tutorial.local systemd-logind[672]: Removed session 48.
Dec 01 10:22:13 DevOps-Tutorial.local systemd-logind[672]: New session 50 of user root.
Dec 01 15:39:52 DevOps-Tutorial.local systemd-logind[672]: Session 50 logged out. Waiting for processes to exit.
Dec 01 15:39:52 DevOps-Tutorial.local systemd-logind[672]: Removed session 50.
Dec 02 08:22:15 DevOps-Tutorial.local systemd-logind[672]: New session 52 of user root.
Dec 02 12:57:17 DevOps-Tutorial.local systemd-logind[672]: Session 52 logged out. Waiting for processes to exit.
Dec 02 12:57:17 DevOps-Tutorial.local systemd-logind[672]: Removed session 52.
Dec 02 14:06:28 DevOps-Tutorial.local systemd-logind[672]: New session 54 of user root.
Dec 02 14:24:39 DevOps-Tutorial.local systemd-logind[672]: Session 54 logged out. Waiting for processes to exit.
Dec 02 14:24:39 DevOps-Tutorial.local systemd-logind[672]: Removed session 54.
Dec 02 14:25:33 DevOps-Tutorial.local systemd-logind[672]: New session 56 of user root.
Dec 02 14:27:18 DevOps-Tutorial.local systemd-logind[672]: Session 56 logged out. Waiting for processes to exit.
Dec 02 14:27:18 DevOps-Tutorial.local systemd-logind[672]: Removed session 56.
Dec 02 14:36:38 DevOps-Tutorial.local systemd-logind[672]: New session 58 of user root.
[root@DevOps-Tutorial ~]#
```

При помощи команды **grep**  и **tail**

```bash
[root@DevOps-Tutorial ~]# journalctl | grep systemd-logind | tail -25
Nov 29 10:18:20 DevOps-Tutorial.local systemd-logind[672]: New session 43 of user root.
Nov 29 12:34:29 DevOps-Tutorial.local systemd-logind[672]: Session 43 logged out. Waiting for processes to exit.
Nov 29 12:34:29 DevOps-Tutorial.local systemd-logind[672]: Removed session 43.
Nov 29 14:08:18 DevOps-Tutorial.local systemd-logind[672]: New session 45 of user root.
Nov 29 16:34:44 DevOps-Tutorial.local systemd-logind[672]: New session 47 of user root.
Nov 29 18:09:12 DevOps-Tutorial.local systemd-logind[672]: Session 45 logged out. Waiting for processes to exit.
Nov 29 18:09:12 DevOps-Tutorial.local systemd-logind[672]: Removed session 45.
Nov 29 19:02:43 DevOps-Tutorial.local systemd-logind[672]: Session 47 logged out. Waiting for processes to exit.
Nov 29 19:02:43 DevOps-Tutorial.local systemd-logind[672]: Removed session 47.
Nov 30 10:33:34 DevOps-Tutorial.local systemd-logind[672]: New session 48 of user root.
Nov 30 18:50:19 DevOps-Tutorial.local systemd-logind[672]: Session 48 logged out. Waiting for processes to exit.
Nov 30 18:50:19 DevOps-Tutorial.local systemd-logind[672]: Removed session 48.
Dec 01 10:22:13 DevOps-Tutorial.local systemd-logind[672]: New session 50 of user root.
Dec 01 15:39:52 DevOps-Tutorial.local systemd-logind[672]: Session 50 logged out. Waiting for processes to exit.
Dec 01 15:39:52 DevOps-Tutorial.local systemd-logind[672]: Removed session 50.
Dec 02 08:22:15 DevOps-Tutorial.local systemd-logind[672]: New session 52 of user root.
Dec 02 12:57:17 DevOps-Tutorial.local systemd-logind[672]: Session 52 logged out. Waiting for processes to exit.
Dec 02 12:57:17 DevOps-Tutorial.local systemd-logind[672]: Removed session 52.
Dec 02 14:06:28 DevOps-Tutorial.local systemd-logind[672]: New session 54 of user root.
Dec 02 14:24:39 DevOps-Tutorial.local systemd-logind[672]: Session 54 logged out. Waiting for processes to exit.
Dec 02 14:24:39 DevOps-Tutorial.local systemd-logind[672]: Removed session 54.
Dec 02 14:25:33 DevOps-Tutorial.local systemd-logind[672]: New session 56 of user root.
Dec 02 14:27:18 DevOps-Tutorial.local systemd-logind[672]: Session 56 logged out. Waiting for processes to exit.
Dec 02 14:27:18 DevOps-Tutorial.local systemd-logind[672]: Removed session 56.
Dec 02 14:36:38 DevOps-Tutorial.local systemd-logind[672]: New session 58 of user root.
[root@DevOps-Tutorial ~]#
```
