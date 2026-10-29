===============================================================================
RED HAT ENTERPRISE LINUX TECHNICAL OVERVIEW (RH024) - TERMINAL EXECUTION LOGS
===============================================================================
Date: October 29, 2026
OS: Red Hat Enterprise Linux / Linux Environment
User: student@rhel-lab

-------------------------------------------------------------------------------
1. SYSTEM INFORMATION & KERNEL VERIFICATION
-------------------------------------------------------------------------------
$ uname -a
Linux rhel-lab.local 5.14.0-362.8.1.el9_3.x86_16 #1 SMP PREEMPT_DYNAMIC x86_64 x86_64 x86_64 GNU/Linux

$ cat /etc/redhat-release
Red Hat Enterprise Linux release 9.3 (Plow)

-------------------------------------------------------------------------------
2. FILE SYSTEM NAVIGATION & DIRECTORY CREATION
-------------------------------------------------------------------------------
$ pwd
/home/student

$ mkdir -p rh024-labs/{01-cli,02-systemd,03-storage}
$ cd rh024-labs
$ ls -la
total 0
drwxr-xr-x. 5 student student 58 Oct 29 20:15 .
drwx------. 3 student student 74 Oct 29 20:15 ..
drwxr-xr-x. 2 student student  6 Oct 29 20:15 01-cli
drwxr-xr-x. 2 student student  6 Oct 29 20:15 02-systemd
drwxr-xr-x. 2 student student  6 Oct 29 20:15 03-storage

-------------------------------------------------------------------------------
3. SYSTEMD SERVICE INSPECTION & COCKPIT ACTIVATION
-------------------------------------------------------------------------------
$ systemctl status cockpit.socket
○ cockpit.socket - Cockpit Web Console Socket
Loaded: loaded (/usr/lib/systemd/system/cockpit.socket; disabled; vendor preset: disabled)
Active: inactive (dead)
Triggers: ● cockpit-session.service
Docs: man:cockpit-ws(8)

$ sudo systemctl enable --now cockpit.socket
[sudo] password for student:
Created symlink /etc/systemd/system/sockets.target.wants/cockpit.socket → /usr/lib/systemd/system/cockpit.socket.

$ systemctl status cockpit.socket
● cockpit.socket - Cockpit Web Console Socket
Loaded: loaded (/usr/lib/systemd/system/cockpit.socket; enabled; vendor preset: disabled)
Active: active (listening) since Thu 2026-10-29 20:20:11 SAST; 4s ago
Triggers: ● cockpit-session.service
Listen: [::]:9090 (Stream)
Tasks: 0 (limit: 11112)
Memory: 1.1M
CPU: 8ms
CGroup: /system.slice/cockpit.socket

-------------------------------------------------------------------------------
4. USER & PERMISSION VERIFICATION
-------------------------------------------------------------------------------
$ touch 01-cli/test-script.sh
$ ls -l 01-cli/test-script.sh
-rw-r--r--. 1 student student 0 Oct 29 20:22 01-cli/test-script.sh

$ chmod 755 01-cli/test-script.sh
$ ls -l 01-cli/test-script.sh
-rwxr-xr-x. 1 student student 0 Oct 29 20:22 01-cli/test-script.sh

-------------------------------------------------------------------------------
5. JOURNAL LOG INSPECTION
-------------------------------------------------------------------------------
$ sudo journalctl -u cockpit.socket --no-pager -n 5
-- Logs begin at Thu 2026-10-29 18:00:00 SAST, end at Thu 2026-10-29 20:25:00 SAST. --
Oct 29 20:20:11 rhel-lab.local systemd[1]: Listening on Cockpit Web Console Socket.
===============================================================================