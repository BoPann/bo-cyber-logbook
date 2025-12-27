# Linux Monitoring

### ssh
check `/var/log/auth.log`. There might be indicator for brute-force attack such as multiple failed log in attempt from the same source. 

process tree analysis
look for a suspecious process id's(pid) parent process id (ppid) and keep doing that until a complete tree is built. 
example
Continuing the example, you begin by locating the suspicious command in the logs with `ausearch -i -x whoami`. Next, you walk up the process tree using the `--pid` option until you reach PID 1, the OS process. The tree eventually shows that `whoami` was launched by a Python web application (`/opt/mywebapp/app.py`).


Auditd (Audit Daemon) is a built-in auditing solution often used by the SOC team for runtime monitoring.

We can view the generated logs in real time in `/var/log/audit/audit.log`, but it is easier to use the `ausearch` command, as it formats the output for better readability and supports filtering options.

Similar to `sysmon`, linux has similar log analysis tool. 
**Linux Audit Framework (`auditd`)** captures events at the kernel level. When a user runs a command, the kernel sees it as a "System Call" (`SYSCALL`) and records several related records linked by a unique ID.

### Attacker's first foothold

| Discovery Goal                | Typical Commands                                                       |
| ----------------------------- | ---------------------------------------------------------------------- |
| OS and Filesystem Discovery   | `pwd`, `ls /`, `env`, `uname -a`, `lsb_release -a`, `hostname`         |
| User and Groups Discovery     | `id`, `whoami`, `w`, `last`, `cat /etc/sudoers`, `cat /etc/passwd`     |
| Process and Network Discovery | `ps aux`, `top`, `ip a`, `ip r`, `arp -a`, `ss -tnlp`, `netstat -tnlp` |
| Cloud or Sandbox Discovery    | `systemd-detect-virt`, `lsmod`, `uptime`, `pgrep "<edr-or-sandbox>"`   |


### Then they will want to move laterally or steal data

| Attack Objectives                                     | Typical Commands                                                       |
| ----------------------------------------------------- | ---------------------------------------------------------------------- |
| Find and steal credentials and other sensitive data   | `history \| grep pass`, `find / -name .env`, `find /home -name id_rsa` |
| Identify how suitable the system is for crypto mining | `cat /proc/cpuinfo`, `lscpu \| grep Model`, `free -m`, `top`, `htop`   |
| Scan the internal network for other future victims    | `ping <ip>`, `for ip in 192.168.1.{1..254}; do nc -w 1 $ip 22 done`    |

Botnet
"Hack and Forget" attacks are usually automated and performed at scale by botnets
