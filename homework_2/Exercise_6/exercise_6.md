# Вывести сообщения с последнего запуска системы. Вывести сообщения не старше одного часа.

При помощи команды **journalctl --since "1 hours ago"**

```bash
[root@DevOps-Tutorial ~]# journalctl --since "1 hours ago"
-- Logs begin at Thu 2024-12-05 10:38:03 UTC, end at Thu 2024-12-05 12:58:21 UTC. --
Dec 05 12:00:06 DevOps-Tutorial.local sshd[3126]: Invalid user iz from 96.67.59.65 port 57126
Dec 05 12:00:06 DevOps-Tutorial.local sshd[3126]: Received disconnect from 96.67.59.65 port 57126:11: Bye Bye [preauth]
Dec 05 12:00:06 DevOps-Tutorial.local sshd[3126]: Disconnected from invalid user iz 96.67.59.65 port 57126 [preauth]
Dec 05 12:00:19 DevOps-Tutorial.local sshd[3129]: Invalid user dmiller from 61.78.67.18 port 46092
Dec 05 12:00:19 DevOps-Tutorial.local sshd[3129]: Received disconnect from 61.78.67.18 port 46092:11: Bye Bye [preauth]
Dec 05 12:00:19 DevOps-Tutorial.local sshd[3129]: Disconnected from invalid user dmiller 61.78.67.18 port 46092 [preauth]
Dec 05 12:00:59 DevOps-Tutorial.local sudo[3133]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart rsyslog
Dec 05 12:00:59 DevOps-Tutorial.local sudo[3133]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:00:59 DevOps-Tutorial.local sudo[3133]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:00:59 DevOps-Tutorial.local systemd[1]: Stopping System Logging Service...
Dec 05 12:01:00 DevOps-Tutorial.local rsyslogd[901]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="901" x-info="https://www.rsyslog.com"] exiting on signal 15.
Dec 05 12:01:00 DevOps-Tutorial.local systemd[1]: rsyslog.service: Succeeded.
Dec 05 12:01:00 DevOps-Tutorial.local systemd[1]: Stopped System Logging Service.
Dec 05 12:01:00 DevOps-Tutorial.local systemd[1]: Starting System Logging Service...
Dec 05 12:01:00 DevOps-Tutorial.local rsyslogd[3138]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3138" x-info="https://www.rsyslog.com"] start
Dec 05 12:01:00 DevOps-Tutorial.local systemd[1]: Started System Logging Service.
Dec 05 12:01:00 DevOps-Tutorial.local sudo[3133]: pam_unix(sudo:session): session closed for user root
Dec 05 12:01:00 DevOps-Tutorial.local rsyslogd[3138]: imjournal: journal files changed, reloading...  [v8.2102.0-7.el8_6.1 try https://www.rsyslog.com/e/0 ]
Dec 05 12:01:01 DevOps-Tutorial.local CROND[3145]: (root) CMD (run-parts /etc/cron.hourly)
Dec 05 12:01:01 DevOps-Tutorial.local run-parts[3148]: (/etc/cron.hourly) starting 0anacron
Dec 05 12:01:01 DevOps-Tutorial.local run-parts[3154]: (/etc/cron.hourly) finished 0anacron
Dec 05 12:02:18 DevOps-Tutorial.local sshd[3156]: Invalid user cs from 61.78.67.18 port 54828
Dec 05 12:02:18 DevOps-Tutorial.local sshd[3156]: Received disconnect from 61.78.67.18 port 54828:11: Bye Bye [preauth]
Dec 05 12:02:18 DevOps-Tutorial.local sshd[3156]: Disconnected from invalid user cs 61.78.67.18 port 54828 [preauth]
Dec 05 12:02:35 DevOps-Tutorial.local sshd[3159]: Invalid user bash from 96.67.59.65 port 36069
Dec 05 12:02:35 DevOps-Tutorial.local sshd[3159]: Received disconnect from 96.67.59.65 port 36069:11: Bye Bye [preauth]
Dec 05 12:02:35 DevOps-Tutorial.local sshd[3159]: Disconnected from invalid user bash 96.67.59.65 port 36069 [preauth]
Dec 05 12:04:25 DevOps-Tutorial.local sshd[3162]: Invalid user abu from 61.78.67.18 port 33484
Dec 05 12:04:25 DevOps-Tutorial.local sshd[3162]: Received disconnect from 61.78.67.18 port 33484:11: Bye Bye [preauth]
Dec 05 12:04:25 DevOps-Tutorial.local sshd[3162]: Disconnected from invalid user abu 61.78.67.18 port 33484 [preauth]
Dec 05 12:06:32 DevOps-Tutorial.local sshd[3167]: Invalid user teija from 61.78.67.18 port 37490
Dec 05 12:06:33 DevOps-Tutorial.local sshd[3167]: Received disconnect from 61.78.67.18 port 37490:11: Bye Bye [preauth]
Dec 05 12:06:33 DevOps-Tutorial.local sshd[3167]: Disconnected from invalid user teija 61.78.67.18 port 37490 [preauth]
Dec 05 12:08:39 DevOps-Tutorial.local sshd[3170]: Invalid user iov from 61.78.67.18 port 59142
Dec 05 12:08:40 DevOps-Tutorial.local sshd[3170]: Received disconnect from 61.78.67.18 port 59142:11: Bye Bye [preauth]
Dec 05 12:08:40 DevOps-Tutorial.local sshd[3170]: Disconnected from invalid user iov 61.78.67.18 port 59142 [preauth]
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/tail -d /var/log/secure
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]: pam_unix(sudo:session): session closed for user root
Dec 05 12:10:53 DevOps-Tutorial.local sshd[3178]: Invalid user bbb from 61.78.67.18 port 44392
Dec 05 12:10:53 DevOps-Tutorial.local sshd[3178]: Received disconnect from 61.78.67.18 port 44392:11: Bye Bye [preauth]
Dec 05 12:10:53 DevOps-Tutorial.local sshd[3178]: Disconnected from invalid user bbb 61.78.67.18 port 44392 [preauth]
Dec 05 12:13:04 DevOps-Tutorial.local sshd[3184]: Invalid user madan from 61.78.67.18 port 36694
Dec 05 12:13:05 DevOps-Tutorial.local sshd[3184]: Received disconnect from 61.78.67.18 port 36694:11: Bye Bye [preauth]
Dec 05 12:13:05 DevOps-Tutorial.local sshd[3184]: Disconnected from invalid user madan 61.78.67.18 port 36694 [preauth]
Dec 05 12:14:01 DevOps-Tutorial.local sudo[3187]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart rsyslog
Dec 05 12:14:01 DevOps-Tutorial.local sudo[3187]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:14:01 DevOps-Tutorial.local sudo[3187]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:14:01 DevOps-Tutorial.local systemd[1]: Stopping System Logging Service...
Dec 05 12:14:02 DevOps-Tutorial.local rsyslogd[3138]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3138" x-info="https://www.rsyslog.com"] exiting on signal 15.
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: rsyslog.service: Succeeded.
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: Stopped System Logging Service.
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: Starting System Logging Service...
Dec 05 12:14:02 DevOps-Tutorial.local rsyslogd[3192]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3192" x-info="https://www.rsyslog.com"] start
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: Started System Logging Service.
Dec 05 12:14:02 DevOps-Tutorial.local sudo[3187]: pam_unix(sudo:session): session closed for user root
Dec 05 12:14:02 DevOps-Tutorial.local rsyslogd[3192]: imjournal: journal files changed, reloading...  [v8.2102.0-7.el8_6.1 try https://www.rsyslog.com/e/0 ]
Dec 05 12:14:14 DevOps-Tutorial.local sudo[3202]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/nano /etc/logrotate.d/my_ssh
Dec 05 12:14:14 DevOps-Tutorial.local sudo[3202]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:14:14 DevOps-Tutorial.local sudo[3202]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:15:12 DevOps-Tutorial.local sshd[3205]: Invalid user rmp from 61.78.67.18 port 40666
Dec 05 12:15:12 DevOps-Tutorial.local sshd[3205]: Received disconnect from 61.78.67.18 port 40666:11: Bye Bye [preauth]
Dec 05 12:15:12 DevOps-Tutorial.local sshd[3205]: Disconnected from invalid user rmp 61.78.67.18 port 40666 [preauth]
Dec 05 12:15:20 DevOps-Tutorial.local sshd[3208]: Invalid user admin from 92.255.85.107 port 44600
Dec 05 12:15:20 DevOps-Tutorial.local sshd[3208]: Connection reset by invalid user admin 92.255.85.107 port 44600 [preauth]
Dec 05 12:16:45 DevOps-Tutorial.local sudo[3202]: pam_unix(sudo:session): session closed for user root
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]: pam_unix(sudo:session): session closed for user root
Dec 05 12:17:20 DevOps-Tutorial.local sshd[3218]: Invalid user kurt from 61.78.67.18 port 37484
Dec 05 12:17:20 DevOps-Tutorial.local sshd[3218]: Received disconnect from 61.78.67.18 port 37484:11: Bye Bye [preauth]
Dec 05 12:17:20 DevOps-Tutorial.local sshd[3218]: Disconnected from invalid user kurt 61.78.67.18 port 37484 [preauth]
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart sshd
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopping OpenSSH server daemon...
Dec 05 12:17:23 DevOps-Tutorial.local sshd[902]: Received signal 15; terminating.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: sshd.service: Succeeded.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopped OpenSSH server daemon.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopped target sshd-keygen.target.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopping sshd-keygen.target.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Reached target sshd-keygen.target.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Starting OpenSSH server daemon...
Dec 05 12:17:23 DevOps-Tutorial.local sshd[3226]: Server listening on 0.0.0.0 port 22.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Started OpenSSH server daemon.
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]: pam_unix(sudo:session): session closed for user root
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart rsyslog
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Stopping System Logging Service...
Dec 05 12:17:30 DevOps-Tutorial.local rsyslogd[3192]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3192" x-info="https://www.rsyslog.com"] exiting on signal 15.
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: rsyslog.service: Succeeded.
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Stopped System Logging Service.
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Starting System Logging Service...
Dec 05 12:17:30 DevOps-Tutorial.local rsyslogd[3233]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3233" x-info="https://www.rsyslog.com"] start
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Started System Logging Service.
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]: pam_unix(sudo:session): session closed for user root
Dec 05 12:17:30 DevOps-Tutorial.local rsyslogd[3233]: imjournal: journal files changed, reloading...  [v8.2102.0-7.el8_6.1 try https://www.rsyslog.com/e/0 ]
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]: pam_unix(sudo:session): session closed for user root
Dec 05 12:19:25 DevOps-Tutorial.local sshd[3243]: Invalid user nason from 61.78.67.18 port 36350
Dec 05 12:19:26 DevOps-Tutorial.local sshd[3243]: Received disconnect from 61.78.67.18 port 36350:11: Bye Bye [preauth]
Dec 05 12:19:26 DevOps-Tutorial.local sshd[3243]: Disconnected from invalid user nason 61.78.67.18 port 36350 [preauth]
Dec 05 12:20:42 DevOps-Tutorial.local sshd[3252]: Accepted publickey for root from 147.45.170.252 port 55534 ssh2: ED25519 SHA256:J3ogJEDZdZmTdhZpEQGkEcbhUvkl5RHTMEtpNkM3oMo
Dec 05 12:20:42 DevOps-Tutorial.local systemd[1]: Started Session 9 of user root.
Dec 05 12:20:42 DevOps-Tutorial.local systemd-logind[624]: New session 9 of user root.
Dec 05 12:20:42 DevOps-Tutorial.local sshd[3252]: pam_unix(sshd:session): session opened for user root by (uid=0)
Dec 05 12:20:52 DevOps-Tutorial.local sshd[3282]: Accepted publickey for root from 147.45.170.252 port 55537 ssh2: ED25519 SHA256:J3ogJEDZdZmTdhZpEQGkEcbhUvkl5RHTMEtpNkM3oMo
Dec 05 12:20:52 DevOps-Tutorial.local systemd[1]: Started Session 10 of user root.
Dec 05 12:20:52 DevOps-Tutorial.local systemd-logind[624]: New session 10 of user root.
Dec 05 12:20:52 DevOps-Tutorial.local sshd[3282]: pam_unix(sshd:session): session opened for user root by (uid=0)
Dec 05 12:21:28 DevOps-Tutorial.local sshd[3313]: Invalid user lab from 61.78.67.18 port 36892
Dec 05 12:21:28 DevOps-Tutorial.local sshd[3313]: Received disconnect from 61.78.67.18 port 36892:11: Bye Bye [preauth]
Dec 05 12:21:28 DevOps-Tutorial.local sshd[3313]: Disconnected from invalid user lab 61.78.67.18 port 36892 [preauth]
Dec 05 12:21:55 DevOps-Tutorial.local sshd[3318]: Received disconnect from 210.91.73.167 port 53564:11: Bye Bye [preauth]
Dec 05 12:21:55 DevOps-Tutorial.local sshd[3318]: Disconnected from authenticating user root 210.91.73.167 port 53564 [preauth]
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]: pam_unix(sudo:session): session closed for user root
Dec 05 12:23:38 DevOps-Tutorial.local sshd[3327]: Invalid user msf from 61.78.67.18 port 57990
Dec 05 12:23:39 DevOps-Tutorial.local sshd[3327]: Received disconnect from 61.78.67.18 port 57990:11: Bye Bye [preauth]
Dec 05 12:23:39 DevOps-Tutorial.local sshd[3327]: Disconnected from invalid user msf 61.78.67.18 port 57990 [preauth]
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]: pam_unix(sudo:session): session closed for user root
Dec 05 12:24:39 DevOps-Tutorial.local sshd[3335]: Received disconnect from 210.91.73.167 port 43930:11: Bye Bye [preauth]
Dec 05 12:24:39 DevOps-Tutorial.local sshd[3335]: Disconnected from authenticating user root 210.91.73.167 port 43930 [preauth]
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]: pam_unix(sudo:session): session closed for user root
Dec 05 12:25:49 DevOps-Tutorial.local sshd[3341]: Invalid user damiano from 61.78.67.18 port 34376
Dec 05 12:25:49 DevOps-Tutorial.local sshd[3341]: Received disconnect from 61.78.67.18 port 34376:11: Bye Bye [preauth]
Dec 05 12:25:49 DevOps-Tutorial.local sshd[3341]: Disconnected from invalid user damiano 61.78.67.18 port 34376 [preauth]
Dec 05 12:27:02 DevOps-Tutorial.local sshd[3344]: Received disconnect from 210.91.73.167 port 60832:11: Bye Bye [preauth]
Dec 05 12:27:02 DevOps-Tutorial.local sshd[3344]: Disconnected from authenticating user root 210.91.73.167 port 60832 [preauth]
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]: pam_unix(sudo:session): session closed for user root
Dec 05 12:27:59 DevOps-Tutorial.local sshd[3352]: Invalid user operador from 61.78.67.18 port 38484
Dec 05 12:27:59 DevOps-Tutorial.local sshd[3352]: Received disconnect from 61.78.67.18 port 38484:11: Bye Bye [preauth]
Dec 05 12:27:59 DevOps-Tutorial.local sshd[3352]: Disconnected from invalid user operador 61.78.67.18 port 38484 [preauth]
Dec 05 12:29:29 DevOps-Tutorial.local sshd[3355]: Received disconnect from 210.91.73.167 port 49508:11: Bye Bye [preauth]
Dec 05 12:29:29 DevOps-Tutorial.local sshd[3355]: Disconnected from authenticating user root 210.91.73.167 port 49508 [preauth]
Dec 05 12:32:06 DevOps-Tutorial.local sshd[3361]: Received disconnect from 210.91.73.167 port 38170:11: Bye Bye [preauth]
Dec 05 12:32:06 DevOps-Tutorial.local sshd[3361]: Disconnected from authenticating user root 210.91.73.167 port 38170 [preauth]
Dec 05 12:34:59 DevOps-Tutorial.local sshd[3368]: Received disconnect from 210.91.73.167 port 55086:11: Bye Bye [preauth]
Dec 05 12:34:59 DevOps-Tutorial.local sshd[3368]: Disconnected from authenticating user root 210.91.73.167 port 55086 [preauth]
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]: pam_unix(sudo:session): session closed for user root
Dec 05 12:37:57 DevOps-Tutorial.local sshd[3375]: Received disconnect from 210.91.73.167 port 43774:11: Bye Bye [preauth]
Dec 05 12:37:57 DevOps-Tutorial.local sshd[3375]: Disconnected from authenticating user root 210.91.73.167 port 43774 [preauth]
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]: pam_unix(sudo:session): session closed for user root
Dec 05 12:40:02 DevOps-Tutorial.local sshd[3383]: error: kex_exchange_identification: Connection closed by remote host
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]: pam_unix(sudo:session): session closed for user root
Dec 05 12:40:49 DevOps-Tutorial.local sshd[3388]: Received disconnect from 210.91.73.167 port 60692:11: Bye Bye [preauth]
Dec 05 12:40:49 DevOps-Tutorial.local sshd[3388]: Disconnected from authenticating user root 210.91.73.167 port 60692 [preauth]
Dec 05 12:42:03 DevOps-Tutorial.local sshd[3391]: Connection closed by authenticating user root 45.6.188.43 port 41072 [preauth]
Dec 05 12:43:46 DevOps-Tutorial.local sshd[3395]: Received disconnect from 210.91.73.167 port 49380:11: Bye Bye [preauth]
Dec 05 12:43:46 DevOps-Tutorial.local sshd[3395]: Disconnected from authenticating user root 210.91.73.167 port 49380 [preauth]
Dec 05 12:45:09 DevOps-Tutorial.local systemd[1]: Starting dnf makecache...
Dec 05 12:45:10 DevOps-Tutorial.local dnf[3398]: Oracle Linux 8 BaseOS Latest (x86_64)            35 kB/s | 4.3 kB     00:00
Dec 05 12:45:11 DevOps-Tutorial.local dnf[3398]: Oracle Linux 8 Application Stream (x86_64)       41 kB/s | 4.5 kB     00:00
Dec 05 12:45:12 DevOps-Tutorial.local dnf[3398]: Latest Unbreakable Enterprise Kernel Release 6   32 kB/s | 3.5 kB     00:00
Dec 05 12:45:15 DevOps-Tutorial.local dnf[3398]: Metadata cache created.
Dec 05 12:45:15 DevOps-Tutorial.local systemd[1]: dnf-makecache.service: Succeeded.
Dec 05 12:45:15 DevOps-Tutorial.local systemd[1]: Started dnf makecache.
Dec 05 12:46:40 DevOps-Tutorial.local sshd[3406]: Received disconnect from 210.91.73.167 port 38064:11: Bye Bye [preauth]
Dec 05 12:46:40 DevOps-Tutorial.local sshd[3406]: Disconnected from authenticating user root 210.91.73.167 port 38064 [preauth]
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]: pam_unix(sudo:session): session closed for user root
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]: pam_unix(sudo:session): session closed for user root
Dec 05 12:49:39 DevOps-Tutorial.local sshd[3416]: Received disconnect from 210.91.73.167 port 54996:11: Bye Bye [preauth]
Dec 05 12:49:39 DevOps-Tutorial.local sshd[3416]: Disconnected from authenticating user root 210.91.73.167 port 54996 [preauth]
Dec 05 12:51:56 DevOps-Tutorial.local sshd[964]: pam_unix(sshd:session): session closed for user root
Dec 05 12:51:56 DevOps-Tutorial.local systemd[1]: session-1.scope: Succeeded.
Dec 05 12:51:56 DevOps-Tutorial.local systemd-logind[624]: Session 1 logged out. Waiting for processes to exit.
Dec 05 12:51:56 DevOps-Tutorial.local systemd-logind[624]: Removed session 1.
Dec 05 12:52:32 DevOps-Tutorial.local sshd[3422]: Received disconnect from 210.91.73.167 port 43684:11: Bye Bye [preauth]
Dec 05 12:52:32 DevOps-Tutorial.local sshd[3422]: Disconnected from authenticating user root 210.91.73.167 port 43684 [preauth]
Dec 05 12:54:07 DevOps-Tutorial.local sshd[1211]: pam_unix(sshd:session): session closed for user root
Dec 05 12:54:07 DevOps-Tutorial.local systemd[1]: session-3.scope: Succeeded.
Dec 05 12:54:07 DevOps-Tutorial.local systemd-logind[624]: Session 3 logged out. Waiting for processes to exit.
Dec 05 12:54:07 DevOps-Tutorial.local systemd-logind[624]: Removed session 3.
Dec 05 12:54:36 DevOps-Tutorial.local sshd[3426]: Connection closed by 124.48.112.228 port 60506 [preauth]
Dec 05 12:55:27 DevOps-Tutorial.local sshd[3429]: Received disconnect from 210.91.73.167 port 60602:11: Bye Bye [preauth]
Dec 05 12:55:27 DevOps-Tutorial.local sshd[3429]: Disconnected from authenticating user root 210.91.73.167 port 60602 [preauth]
Dec 05 12:56:06 DevOps-Tutorial.local sshd[3432]: Connection closed by 49.160.101.198 port 54800 [preauth]
Dec 05 12:56:12 DevOps-Tutorial.local sshd[3435]: Received disconnect from 77.221.138.170 port 58012:11: Bye Bye [preauth]
Dec 05 12:56:12 DevOps-Tutorial.local sshd[3435]: Disconnected from authenticating user root 77.221.138.170 port 58012 [preauth]
Dec 05 12:56:40 DevOps-Tutorial.local sshd[3439]: Received disconnect from 45.55.39.59 port 57886:11: Bye Bye [preauth]
Dec 05 12:56:40 DevOps-Tutorial.local sshd[3439]: Disconnected from authenticating user root 45.55.39.59 port 57886 [preauth]
Dec 05 12:57:01 DevOps-Tutorial.local sshd[3444]: error: kex_exchange_identification: client sent invalid protocol identifier "-HSS2.0-libssh_0.9.6"
Dec 05 12:58:21 DevOps-Tutorial.local sshd[3451]: Received disconnect from 210.91.73.167 port 49284:11: Bye Bye [preauth]
Dec 05 12:58:21 DevOps-Tutorial.local sshd[3451]: Disconnected from authenticating user root 210.91.73.167 port 49284 [preauth]
```

При помощи команды **journalctl -b --since "1 hours ago"**

```bash
[root@DevOps-Tutorial ~]# journalctl -b --since "1 hours ago"
-- Logs begin at Thu 2024-12-05 10:38:03 UTC, end at Thu 2024-12-05 13:02:02 UTC. --
Dec 05 12:04:25 DevOps-Tutorial.local sshd[3162]: Invalid user abu from 61.78.67.18 port 33484
Dec 05 12:04:25 DevOps-Tutorial.local sshd[3162]: Received disconnect from 61.78.67.18 port 33484:11: Bye Bye [preauth]
Dec 05 12:04:25 DevOps-Tutorial.local sshd[3162]: Disconnected from invalid user abu 61.78.67.18 port 33484 [preauth]
Dec 05 12:06:32 DevOps-Tutorial.local sshd[3167]: Invalid user teija from 61.78.67.18 port 37490
Dec 05 12:06:33 DevOps-Tutorial.local sshd[3167]: Received disconnect from 61.78.67.18 port 37490:11: Bye Bye [preauth]
Dec 05 12:06:33 DevOps-Tutorial.local sshd[3167]: Disconnected from invalid user teija 61.78.67.18 port 37490 [preauth]
Dec 05 12:08:39 DevOps-Tutorial.local sshd[3170]: Invalid user iov from 61.78.67.18 port 59142
Dec 05 12:08:40 DevOps-Tutorial.local sshd[3170]: Received disconnect from 61.78.67.18 port 59142:11: Bye Bye [preauth]
Dec 05 12:08:40 DevOps-Tutorial.local sshd[3170]: Disconnected from invalid user iov 61.78.67.18 port 59142 [preauth]
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/tail -d /var/log/secure
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:10:03 DevOps-Tutorial.local sudo[3173]: pam_unix(sudo:session): session closed for user root
Dec 05 12:10:53 DevOps-Tutorial.local sshd[3178]: Invalid user bbb from 61.78.67.18 port 44392
Dec 05 12:10:53 DevOps-Tutorial.local sshd[3178]: Received disconnect from 61.78.67.18 port 44392:11: Bye Bye [preauth]
Dec 05 12:10:53 DevOps-Tutorial.local sshd[3178]: Disconnected from invalid user bbb 61.78.67.18 port 44392 [preauth]
Dec 05 12:13:04 DevOps-Tutorial.local sshd[3184]: Invalid user madan from 61.78.67.18 port 36694
Dec 05 12:13:05 DevOps-Tutorial.local sshd[3184]: Received disconnect from 61.78.67.18 port 36694:11: Bye Bye [preauth]
Dec 05 12:13:05 DevOps-Tutorial.local sshd[3184]: Disconnected from invalid user madan 61.78.67.18 port 36694 [preauth]
Dec 05 12:14:01 DevOps-Tutorial.local sudo[3187]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart rsyslog
Dec 05 12:14:01 DevOps-Tutorial.local sudo[3187]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:14:01 DevOps-Tutorial.local sudo[3187]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:14:01 DevOps-Tutorial.local systemd[1]: Stopping System Logging Service...
Dec 05 12:14:02 DevOps-Tutorial.local rsyslogd[3138]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3138" x-info="https://www.rsyslog.com"] exiting on signal 15.
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: rsyslog.service: Succeeded.
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: Stopped System Logging Service.
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: Starting System Logging Service...
Dec 05 12:14:02 DevOps-Tutorial.local rsyslogd[3192]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3192" x-info="https://www.rsyslog.com"] start
Dec 05 12:14:02 DevOps-Tutorial.local systemd[1]: Started System Logging Service.
Dec 05 12:14:02 DevOps-Tutorial.local sudo[3187]: pam_unix(sudo:session): session closed for user root
Dec 05 12:14:02 DevOps-Tutorial.local rsyslogd[3192]: imjournal: journal files changed, reloading...  [v8.2102.0-7.el8_6.1 try https://www.rsyslog.com/e/0 ]
Dec 05 12:14:14 DevOps-Tutorial.local sudo[3202]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/nano /etc/logrotate.d/my_ssh
Dec 05 12:14:14 DevOps-Tutorial.local sudo[3202]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:14:14 DevOps-Tutorial.local sudo[3202]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:15:12 DevOps-Tutorial.local sshd[3205]: Invalid user rmp from 61.78.67.18 port 40666
Dec 05 12:15:12 DevOps-Tutorial.local sshd[3205]: Received disconnect from 61.78.67.18 port 40666:11: Bye Bye [preauth]
Dec 05 12:15:12 DevOps-Tutorial.local sshd[3205]: Disconnected from invalid user rmp 61.78.67.18 port 40666 [preauth]
Dec 05 12:15:20 DevOps-Tutorial.local sshd[3208]: Invalid user admin from 92.255.85.107 port 44600
Dec 05 12:15:20 DevOps-Tutorial.local sshd[3208]: Connection reset by invalid user admin 92.255.85.107 port 44600 [preauth]
Dec 05 12:16:45 DevOps-Tutorial.local sudo[3202]: pam_unix(sudo:session): session closed for user root
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:16:57 DevOps-Tutorial.local sudo[3215]: pam_unix(sudo:session): session closed for user root
Dec 05 12:17:20 DevOps-Tutorial.local sshd[3218]: Invalid user kurt from 61.78.67.18 port 37484
Dec 05 12:17:20 DevOps-Tutorial.local sshd[3218]: Received disconnect from 61.78.67.18 port 37484:11: Bye Bye [preauth]
Dec 05 12:17:20 DevOps-Tutorial.local sshd[3218]: Disconnected from invalid user kurt 61.78.67.18 port 37484 [preauth]
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart sshd
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopping OpenSSH server daemon...
Dec 05 12:17:23 DevOps-Tutorial.local sshd[902]: Received signal 15; terminating.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: sshd.service: Succeeded.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopped OpenSSH server daemon.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopped target sshd-keygen.target.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Stopping sshd-keygen.target.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Reached target sshd-keygen.target.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Starting OpenSSH server daemon...
Dec 05 12:17:23 DevOps-Tutorial.local sshd[3226]: Server listening on 0.0.0.0 port 22.
Dec 05 12:17:23 DevOps-Tutorial.local systemd[1]: Started OpenSSH server daemon.
Dec 05 12:17:23 DevOps-Tutorial.local sudo[3221]: pam_unix(sudo:session): session closed for user root
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/bin/systemctl restart rsyslog
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Stopping System Logging Service...
Dec 05 12:17:30 DevOps-Tutorial.local rsyslogd[3192]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3192" x-info="https://www.rsyslog.com"] exiting on signal 15.
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: rsyslog.service: Succeeded.
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Stopped System Logging Service.
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Starting System Logging Service...
Dec 05 12:17:30 DevOps-Tutorial.local rsyslogd[3233]: [origin software="rsyslogd" swVersion="8.2102.0-7.el8_6.1" x-pid="3233" x-info="https://www.rsyslog.com"] start
Dec 05 12:17:30 DevOps-Tutorial.local systemd[1]: Started System Logging Service.
Dec 05 12:17:30 DevOps-Tutorial.local sudo[3229]: pam_unix(sudo:session): session closed for user root
Dec 05 12:17:30 DevOps-Tutorial.local rsyslogd[3233]: imjournal: journal files changed, reloading...  [v8.2102.0-7.el8_6.1 try https://www.rsyslog.com/e/0 ]
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:18:06 DevOps-Tutorial.local sudo[3240]: pam_unix(sudo:session): session closed for user root
Dec 05 12:19:25 DevOps-Tutorial.local sshd[3243]: Invalid user nason from 61.78.67.18 port 36350
Dec 05 12:19:26 DevOps-Tutorial.local sshd[3243]: Received disconnect from 61.78.67.18 port 36350:11: Bye Bye [preauth]
Dec 05 12:19:26 DevOps-Tutorial.local sshd[3243]: Disconnected from invalid user nason 61.78.67.18 port 36350 [preauth]
Dec 05 12:20:42 DevOps-Tutorial.local sshd[3252]: Accepted publickey for root from 147.45.170.252 port 55534 ssh2: ED25519 SHA256:J3ogJEDZdZmTdhZpEQGkEcbhUvkl5RHTMEtpNkM3oMo
Dec 05 12:20:42 DevOps-Tutorial.local systemd[1]: Started Session 9 of user root.
Dec 05 12:20:42 DevOps-Tutorial.local systemd-logind[624]: New session 9 of user root.
Dec 05 12:20:42 DevOps-Tutorial.local sshd[3252]: pam_unix(sshd:session): session opened for user root by (uid=0)
Dec 05 12:20:52 DevOps-Tutorial.local sshd[3282]: Accepted publickey for root from 147.45.170.252 port 55537 ssh2: ED25519 SHA256:J3ogJEDZdZmTdhZpEQGkEcbhUvkl5RHTMEtpNkM3oMo
Dec 05 12:20:52 DevOps-Tutorial.local systemd[1]: Started Session 10 of user root.
Dec 05 12:20:52 DevOps-Tutorial.local systemd-logind[624]: New session 10 of user root.
Dec 05 12:20:52 DevOps-Tutorial.local sshd[3282]: pam_unix(sshd:session): session opened for user root by (uid=0)
Dec 05 12:21:28 DevOps-Tutorial.local sshd[3313]: Invalid user lab from 61.78.67.18 port 36892
Dec 05 12:21:28 DevOps-Tutorial.local sshd[3313]: Received disconnect from 61.78.67.18 port 36892:11: Bye Bye [preauth]
Dec 05 12:21:28 DevOps-Tutorial.local sshd[3313]: Disconnected from invalid user lab 61.78.67.18 port 36892 [preauth]
Dec 05 12:21:55 DevOps-Tutorial.local sshd[3318]: Received disconnect from 210.91.73.167 port 53564:11: Bye Bye [preauth]
Dec 05 12:21:55 DevOps-Tutorial.local sshd[3318]: Disconnected from authenticating user root 210.91.73.167 port 53564 [preauth]
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:23:29 DevOps-Tutorial.local sudo[3324]: pam_unix(sudo:session): session closed for user root
Dec 05 12:23:38 DevOps-Tutorial.local sshd[3327]: Invalid user msf from 61.78.67.18 port 57990
Dec 05 12:23:39 DevOps-Tutorial.local sshd[3327]: Received disconnect from 61.78.67.18 port 57990:11: Bye Bye [preauth]
Dec 05 12:23:39 DevOps-Tutorial.local sshd[3327]: Disconnected from invalid user msf 61.78.67.18 port 57990 [preauth]
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:24:15 DevOps-Tutorial.local sudo[3331]: pam_unix(sudo:session): session closed for user root
Dec 05 12:24:39 DevOps-Tutorial.local sshd[3335]: Received disconnect from 210.91.73.167 port 43930:11: Bye Bye [preauth]
Dec 05 12:24:39 DevOps-Tutorial.local sshd[3335]: Disconnected from authenticating user root 210.91.73.167 port 43930 [preauth]
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:25:16 DevOps-Tutorial.local sudo[3338]: pam_unix(sudo:session): session closed for user root
Dec 05 12:25:49 DevOps-Tutorial.local sshd[3341]: Invalid user damiano from 61.78.67.18 port 34376
Dec 05 12:25:49 DevOps-Tutorial.local sshd[3341]: Received disconnect from 61.78.67.18 port 34376:11: Bye Bye [preauth]
Dec 05 12:25:49 DevOps-Tutorial.local sshd[3341]: Disconnected from invalid user damiano 61.78.67.18 port 34376 [preauth]
Dec 05 12:27:02 DevOps-Tutorial.local sshd[3344]: Received disconnect from 210.91.73.167 port 60832:11: Bye Bye [preauth]
Dec 05 12:27:02 DevOps-Tutorial.local sshd[3344]: Disconnected from authenticating user root 210.91.73.167 port 60832 [preauth]
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:27:43 DevOps-Tutorial.local sudo[3349]: pam_unix(sudo:session): session closed for user root
Dec 05 12:27:59 DevOps-Tutorial.local sshd[3352]: Invalid user operador from 61.78.67.18 port 38484
Dec 05 12:27:59 DevOps-Tutorial.local sshd[3352]: Received disconnect from 61.78.67.18 port 38484:11: Bye Bye [preauth]
Dec 05 12:27:59 DevOps-Tutorial.local sshd[3352]: Disconnected from invalid user operador 61.78.67.18 port 38484 [preauth]
Dec 05 12:29:29 DevOps-Tutorial.local sshd[3355]: Received disconnect from 210.91.73.167 port 49508:11: Bye Bye [preauth]
Dec 05 12:29:29 DevOps-Tutorial.local sshd[3355]: Disconnected from authenticating user root 210.91.73.167 port 49508 [preauth]
Dec 05 12:32:06 DevOps-Tutorial.local sshd[3361]: Received disconnect from 210.91.73.167 port 38170:11: Bye Bye [preauth]
Dec 05 12:32:06 DevOps-Tutorial.local sshd[3361]: Disconnected from authenticating user root 210.91.73.167 port 38170 [preauth]
Dec 05 12:34:59 DevOps-Tutorial.local sshd[3368]: Received disconnect from 210.91.73.167 port 55086:11: Bye Bye [preauth]
Dec 05 12:34:59 DevOps-Tutorial.local sshd[3368]: Disconnected from authenticating user root 210.91.73.167 port 55086 [preauth]
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:35:52 DevOps-Tutorial.local sudo[3371]: pam_unix(sudo:session): session closed for user root
Dec 05 12:37:57 DevOps-Tutorial.local sshd[3375]: Received disconnect from 210.91.73.167 port 43774:11: Bye Bye [preauth]
Dec 05 12:37:57 DevOps-Tutorial.local sshd[3375]: Disconnected from authenticating user root 210.91.73.167 port 43774 [preauth]
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:39:53 DevOps-Tutorial.local sudo[3379]: pam_unix(sudo:session): session closed for user root
Dec 05 12:40:02 DevOps-Tutorial.local sshd[3383]: error: kex_exchange_identification: Connection closed by remote host
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:40:04 DevOps-Tutorial.local sudo[3385]: pam_unix(sudo:session): session closed for user root
Dec 05 12:40:49 DevOps-Tutorial.local sshd[3388]: Received disconnect from 210.91.73.167 port 60692:11: Bye Bye [preauth]
Dec 05 12:40:49 DevOps-Tutorial.local sshd[3388]: Disconnected from authenticating user root 210.91.73.167 port 60692 [preauth]
Dec 05 12:42:03 DevOps-Tutorial.local sshd[3391]: Connection closed by authenticating user root 45.6.188.43 port 41072 [preauth]
Dec 05 12:43:46 DevOps-Tutorial.local sshd[3395]: Received disconnect from 210.91.73.167 port 49380:11: Bye Bye [preauth]
Dec 05 12:43:46 DevOps-Tutorial.local sshd[3395]: Disconnected from authenticating user root 210.91.73.167 port 49380 [preauth]
Dec 05 12:45:09 DevOps-Tutorial.local systemd[1]: Starting dnf makecache...
Dec 05 12:45:10 DevOps-Tutorial.local dnf[3398]: Oracle Linux 8 BaseOS Latest (x86_64)            35 kB/s | 4.3 kB     00:00
Dec 05 12:45:11 DevOps-Tutorial.local dnf[3398]: Oracle Linux 8 Application Stream (x86_64)       41 kB/s | 4.5 kB     00:00
Dec 05 12:45:12 DevOps-Tutorial.local dnf[3398]: Latest Unbreakable Enterprise Kernel Release 6   32 kB/s | 3.5 kB     00:00
Dec 05 12:45:15 DevOps-Tutorial.local dnf[3398]: Metadata cache created.
Dec 05 12:45:15 DevOps-Tutorial.local systemd[1]: dnf-makecache.service: Succeeded.
Dec 05 12:45:15 DevOps-Tutorial.local systemd[1]: Started dnf makecache.
Dec 05 12:46:40 DevOps-Tutorial.local sshd[3406]: Received disconnect from 210.91.73.167 port 38064:11: Bye Bye [preauth]
Dec 05 12:46:40 DevOps-Tutorial.local sshd[3406]: Disconnected from authenticating user root 210.91.73.167 port 38064 [preauth]
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:46:47 DevOps-Tutorial.local sudo[3409]: pam_unix(sudo:session): session closed for user root
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]:     root : TTY=pts/3 ; PWD=/root ; USER=root ; COMMAND=/sbin/logrotate -d /etc/logrotate.d/my_ssh
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]: pam_systemd(sudo:session): Cannot create session: Already running in a session or user slice
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]: pam_unix(sudo:session): session opened for user root by root(uid=0)
Dec 05 12:47:39 DevOps-Tutorial.local sudo[3413]: pam_unix(sudo:session): session closed for user root
Dec 05 12:49:39 DevOps-Tutorial.local sshd[3416]: Received disconnect from 210.91.73.167 port 54996:11: Bye Bye [preauth]
Dec 05 12:49:39 DevOps-Tutorial.local sshd[3416]: Disconnected from authenticating user root 210.91.73.167 port 54996 [preauth]
Dec 05 12:51:56 DevOps-Tutorial.local sshd[964]: pam_unix(sshd:session): session closed for user root
Dec 05 12:51:56 DevOps-Tutorial.local systemd[1]: session-1.scope: Succeeded.
Dec 05 12:51:56 DevOps-Tutorial.local systemd-logind[624]: Session 1 logged out. Waiting for processes to exit.
Dec 05 12:51:56 DevOps-Tutorial.local systemd-logind[624]: Removed session 1.
Dec 05 12:52:32 DevOps-Tutorial.local sshd[3422]: Received disconnect from 210.91.73.167 port 43684:11: Bye Bye [preauth]
Dec 05 12:52:32 DevOps-Tutorial.local sshd[3422]: Disconnected from authenticating user root 210.91.73.167 port 43684 [preauth]
Dec 05 12:54:07 DevOps-Tutorial.local sshd[1211]: pam_unix(sshd:session): session closed for user root
Dec 05 12:54:07 DevOps-Tutorial.local systemd[1]: session-3.scope: Succeeded.
Dec 05 12:54:07 DevOps-Tutorial.local systemd-logind[624]: Session 3 logged out. Waiting for processes to exit.
Dec 05 12:54:07 DevOps-Tutorial.local systemd-logind[624]: Removed session 3.
Dec 05 12:54:36 DevOps-Tutorial.local sshd[3426]: Connection closed by 124.48.112.228 port 60506 [preauth]
Dec 05 12:55:27 DevOps-Tutorial.local sshd[3429]: Received disconnect from 210.91.73.167 port 60602:11: Bye Bye [preauth]
Dec 05 12:55:27 DevOps-Tutorial.local sshd[3429]: Disconnected from authenticating user root 210.91.73.167 port 60602 [preauth]
Dec 05 12:56:06 DevOps-Tutorial.local sshd[3432]: Connection closed by 49.160.101.198 port 54800 [preauth]
Dec 05 12:56:12 DevOps-Tutorial.local sshd[3435]: Received disconnect from 77.221.138.170 port 58012:11: Bye Bye [preauth]
Dec 05 12:56:12 DevOps-Tutorial.local sshd[3435]: Disconnected from authenticating user root 77.221.138.170 port 58012 [preauth]
Dec 05 12:56:40 DevOps-Tutorial.local sshd[3439]: Received disconnect from 45.55.39.59 port 57886:11: Bye Bye [preauth]
Dec 05 12:56:40 DevOps-Tutorial.local sshd[3439]: Disconnected from authenticating user root 45.55.39.59 port 57886 [preauth]
Dec 05 12:57:01 DevOps-Tutorial.local sshd[3444]: error: kex_exchange_identification: client sent invalid protocol identifier "-HSS2.0-libssh_0.9.6"
Dec 05 12:58:21 DevOps-Tutorial.local sshd[3451]: Received disconnect from 210.91.73.167 port 49284:11: Bye Bye [preauth]
Dec 05 12:58:21 DevOps-Tutorial.local sshd[3451]: Disconnected from authenticating user root 210.91.73.167 port 49284 [preauth]
Dec 05 12:58:58 DevOps-Tutorial.local sshd[3457]: Connection reset by 52.172.170.104 port 57532 [preauth]
Dec 05 12:59:41 DevOps-Tutorial.local sshd[3460]: Received disconnect from 77.221.138.170 port 54522:11: Bye Bye [preauth]
Dec 05 12:59:41 DevOps-Tutorial.local sshd[3460]: Disconnected from authenticating user root 77.221.138.170 port 54522 [preauth]
Dec 05 12:59:58 DevOps-Tutorial.local sshd[3463]: error: kex_exchange_identification: client sent invalid protocol identifier "-HSS2.0-libssh_0.9.6"
Dec 05 13:00:14 DevOps-Tutorial.local sshd[3465]: Received disconnect from 45.55.39.59 port 56958:11: Bye Bye [preauth]
Dec 05 13:00:14 DevOps-Tutorial.local sshd[3465]: Disconnected from authenticating user root 45.55.39.59 port 56958 [preauth]
Dec 05 13:01:01 DevOps-Tutorial.local CROND[3469]: (root) CMD (run-parts /etc/cron.hourly)
Dec 05 13:01:01 DevOps-Tutorial.local run-parts[3472]: (/etc/cron.hourly) starting 0anacron
Dec 05 13:01:01 DevOps-Tutorial.local run-parts[3478]: (/etc/cron.hourly) finished 0anacron
Dec 05 13:01:18 DevOps-Tutorial.local sshd[3479]: Received disconnect from 210.91.73.167 port 37954:11: Bye Bye [preauth]
Dec 05 13:01:18 DevOps-Tutorial.local sshd[3479]: Disconnected from authenticating user root 210.91.73.167 port 37954 [preauth]
Dec 05 13:01:47 DevOps-Tutorial.local sshd[3482]: Received disconnect from 77.221.138.170 port 50416:11: Bye Bye [preauth]
Dec 05 13:01:47 DevOps-Tutorial.local sshd[3482]: Disconnected from authenticating user root 77.221.138.170 port 50416 [preauth]
Dec 05 13:02:02 DevOps-Tutorial.local sshd[3487]: Received disconnect from 45.55.39.59 port 37478:11: Bye Bye [preauth]
Dec 05 13:02:02 DevOps-Tutorial.local sshd[3487]: Disconnected from authenticating user root 45.55.39.59 port 37478 [preauth]
``
