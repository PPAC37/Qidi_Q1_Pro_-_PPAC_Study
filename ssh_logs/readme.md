
Firmware v4.4.13

--- 

Altération déja éffectuées

https://github.com/fran6p/Qidi_X-Max3/blob/main/OS/date-heures-synchronisees.md#alternative2

<details>
  <summary>(Cliquez pour déplier!)</summary>
# ALTERNATIVE2

## PRÉALABLE

Les paquets **ntp** et **chrony** si installés doivent être désinstallés, inutiles, ils empêchent la synchronisation horaire. Le système perd l'heure et l'utilisation de git, apt provoquent des erreurs à cause de l'heure système non à jour :

```
sudo apt remove ntp chrony
```

Utiliser la commande `timedatectl` de **systemd**
- paramétrer la zone horaire :
```
timedatectl set-timezone Europe/Paris
```
- lister les zones horaires :
```
timedatectl list-timezones
```
- activer la synchronisation horaire via serveurs de temps (ntp) :
```
timedatectl set-ntp 1
```
- régler la date  et l'heure (inutile si un accès réseau est disponible utilisant la synchro ntp) :
```
timedatectl set-time '2024-02-20 18:15:22'
```

Le démarrage manuel de `systemd-timesyncd` n'est pas nécessaire, `timedatectl` s'en charge 

Pour vérifier que tout est correct, un simple `timedatectl` affichera les infos :
```bash
mks@mkspi:~$ timedatectl
               Local time: Thu 2024-02-22 18:09:36 CET
           Universal time: Thu 2024-02-22 17:09:36 UTC
                 RTC time: Thu 2024-02-22 17:09:14
                Time zone: Europe/Paris (CET, +0100)
System clock synchronized: yes
              NTP service: active
          RTC in local TZ: no
```

:smiley:
</details>

~~~
sudo apt remove ntp chrony
~~~

et utilisation de la machine

---

~~~
ssh root@192.168.1.33
~~~
<pre>
q6@q6-pc:~$ ssh root@192.168.1.33
root@192.168.1.33's password: 
┌─────────────────────────────────────────────┐
│  ___  ___ ____ ___   _____ _____ ____ _   _ │
│ / _ \|_ _|  _ \_ _| |_   _| ____/ ___| | | |│
│| | | || || | | | |    | | |  _|| |   | |_| |│
│| |_| || || |_| | |    | | | |__| |___|  _  |│
│ \__\_\___|____/___|   |_| |_____\____|_| |_|│
│                                             │
└─────────────────────────────────────────────┘
+-------------------------------------------------------------------------------+
| Warning: Modifying system files and installing unofficial plugins means that  |
| the customer is waiving their expectations of official support. They will be  |
| solely responsible for the security and safety of their printer. Any firmware |
| issues arising from these modifications will not be covered under warranty.   |
+-------------------------------------------------------------------------------+

Welcome to Armbian 22.05.0-trunk  with bleeding edge Linux 5.16.20-rockchip64

No end-user support: built from trunk

System load:   58%           	Up time:       0 min	
Memory usage:  21% of 976M   	IP:	       192.168.1.33
CPU temp:      43°C           	Usage of /:    22% of 29G    	
storage/:      4% of 15G    	

[ 0 security updates available, 235 updates total: apt upgrade ]
Last check: 2024-03-21 01:05

Failed to restart ntp.service: Unit ntp.service is masked.
root@mkspi:~#
</pre>

---

~~~
cat /root/xindi/version
~~~
<pre>
root@mkspi:~# cat /root/xindi/version
[version]
mcu             = V0.10.0
ui              = V4.4.13
soc             = V4.4.13
root@mkspi:~#
</pre>

---

~~~
env
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
root@mkspi:~# env
SHELL=/usr/bin/bash
LANGUAGE=en_US.UTF-8
PWD=/root
LOGNAME=root
XDG_SESSION_TYPE=tty
HOME=/root
LANG=en_US.UTF-8
SSH_CONNECTION=192.168.1.10 48224 192.168.1.33 22
XDG_SESSION_CLASS=user
TERM=xterm-256color
USER=root
SHLVL=1
LC_MESSAGES=en_US.UTF-8
XDG_SESSION_ID=2
XDG_RUNTIME_DIR=/run/user/0
SSH_CLIENT=192.168.1.10 48224 22
LC_ALL=en_US.UTF-8
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
MAIL=/var/mail/root
SSH_TTY=/dev/pts/2
_=/usr/bin/env
root@mkspi:~#
</pre>
</details>

---


~~~
ls -la /root/
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
root@mkspi:~# ls -la /root/
10-armbian-header        .gitconfig               old_config.ini           .viminfo
40-usb_modeswitch.rules  .gnupg/                  run.txt                  .wget-hsts
800_480.tft.bak          hid-flash                STM32_HID_Bootloader/    .wpa_cli_history
Adaptive_Mesh.cfg        klipper.bin              sysctl.conf              www/
.bash_history            .local/                  tenda/                   .Xauthority
.bashrc                  merge.awk                timeup.sh                xindi/
.cache/                  merge.py                 uart                     .zshrc
.config/                 new_config.ini           uart-230400              
config.mksini            .oh-my-zsh/              udp_server               
root@mkspi:~#
</pre>
</details>

---

~~~
du -sh /root/
~~~
<pre>
root@mkspi:~# du -sh /root/
61M	/root/
root@mkspi:~#
</pre>

---

~~~
mount
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
root@mkspi:~# mount
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
udev on /dev type devtmpfs (rw,nosuid,relatime,size=426036k,nr_inodes=106509,mode=755)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,noexec,relatime,size=99980k,mode=755)
/dev/mmcblk1p2 on / type ext4 (rw,noatime,errors=remount-ro,commit=1)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev)
tmpfs on /run/lock type tmpfs (rw,nosuid,nodev,noexec,relatime,size=5120k)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,mode=755)
cgroup2 on /sys/fs/cgroup/unified type cgroup2 (rw,nosuid,nodev,noexec,relatime,nsdelegate)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
bpf on /sys/fs/bpf type bpf (rw,nosuid,nodev,noexec,relatime,mode=700)
cgroup on /sys/fs/cgroup/net_cls,net_prio type cgroup (rw,nosuid,nodev,noexec,relatime,net_cls,net_prio)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpu,cpuacct)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
cgroup on /sys/fs/cgroup/rdma type cgroup (rw,nosuid,nodev,noexec,relatime,rdma)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/pids type cgroup (rw,nosuid,nodev,noexec,relatime,pids)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=25,pgrp=1,timeout=0,minproto=5,maxproto=5,direct)
mqueue on /dev/mqueue type mqueue (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime,pagesize=2M)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
fusectl on /sys/fs/fuse/connections type fusectl (rw,relatime)
configfs on /sys/kernel/config type configfs (rw,relatime)
tmpfs on /tmp type tmpfs (rw,nosuid,relatime)
/dev/mmcblk1p1 on /boot type vfat (rw,relatime,fmask=0022,dmask=0022,codepage=437,iocharset=iso8859-1,shortname=mixed,utf8,errors=remount-ro)
/dev/mmcblk1p2 on /var/log.hdd type ext4 (rw,noatime,errors=remount-ro,commit=1)
/dev/zram1 on /var/log type ext4 (rw,relatime,discard)
tracefs on /sys/kernel/debug/tracing type tracefs (rw,relatime)
/dev/sda1 on /home/mks/gcode_files/sda1 type vfat (rw,nosuid,nodev,noexec,relatime,gid=100,fmask=0111,dmask=0000,allow_utime=0022,codepage=437,iocharset=iso8859-1,shortname=mixed,utf8,flush,errors=remount-ro)
tmpfs on /run/user/0 type tmpfs (rw,nosuid,nodev,relatime,size=99976k,mode=700)
root@mkspi:~# 
</pre>
</details>

---


<!-- Template 1 -->
<!--

~~~

~~~
<pre>

</pre>

---

-->

<!-- Template 1 -->
<!--

~~~

~~~
<pre>

</pre>

---

-->

<!-- Template 2 -->
<!--

~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>

</pre>
</details>

---
-->



