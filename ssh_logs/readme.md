
Firmware v4.4.13

---

~~~
ssh 10.42.0.45 -l root
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
q6@q6-pc:~$ ssh 10.42.0.45 -l root
root@10.42.0.45's password: 
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

System load:   14%           	Up time:       55 min	
Memory usage:  19% of 976M   	IP:	       10.42.0.45
CPU temp:      45°C           	Usage of /:    20% of 29G    	

[ 0 security updates available, 235 updates total: apt upgrade ]
Last check: 2023-10-29 01:18

[ General system configuration (beta): armbian-config ]

Last login: Sun Mar 10 05:47:27 2024 from 10.42.0.1
root@mkspi:~# 

</pre>
</details>

---

~~~
fdisk -l
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
root@mkspi:~# fdisk -l
Disk /dev/mmcblk1: 28.9 GiB, 31037849600 bytes, 60620800 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x6a783df4

Device         Boot  Start      End  Sectors  Size Id Type
/dev/mmcblk1p1       32768   557055   524288  256M  e W95 FAT16 (LBA)
/dev/mmcblk1p2      557056 59998207 59441152 28.4G 83 Linux


Disk /dev/zram0: 488.2 MiB, 511893504 bytes, 124974 sectors
Units: sectors of 1 * 4096 = 4096 bytes
Sector size (logical/physical): 4096 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes


Disk /dev/zram1: 50 MiB, 52428800 bytes, 12800 sectors
Units: sectors of 1 * 4096 = 4096 bytes
Sector size (logical/physical): 4096 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes
root@mkspi:~# 
</pre>
</details>

---

~~~
ls -la /root
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
root@mkspi:~# ls -la
total 13320
drwx------ 11 root root     4096 Mar 10 06:27 .
drwxr-xr-x 19 root root     4096 Oct 28 21:18 ..
-rwxr-xr-x  1 root root     4521 Jan 12 10:14 10-armbian-header
-rw-r--r--  1 root root    41178 Sep 19 15:13 40-usb_modeswitch.rules
-rw-r--r--  1 root root 13279128 Oct 28 21:18 800_480.tft.bak
-rw-r--r--  1 root root    13916 May 28  2023 Adaptive_Mesh.cfg
-rw-------  1 root root     5964 Mar 10 06:27 .bash_history
-rw-r--r--  1 root root     3523 Jul 25  2022 .bashrc
drwx------  3 root root     4096 Sep 26 17:47 .cache
drwx------  7 root root     4096 Dec 10  2022 .config
-rw-r--r--  1 root root      195 Oct 28 21:18 config.mksini
-rw-r--r--  1 root root       58 Dec 10  2022 .gitconfig
drwx------  3 root root     4096 Jul 25  2022 .gnupg
-rwxr-xr-x  1 root root    44264 May 28  2023 hid-flash
-rw-r--r--  1 root root    26540 Dec 10  2022 klipper.bin
drwxr-xr-x  3 root root     4096 Jul 26  2022 .local
-rw-r--r--  1 root root      204 May 28  2023 merge.awk
-rwxr-xr-x  1 root root     2643 May 28  2023 merge.py
-rwxr-xr-x  1 root root      441 May 28  2023 new_config.ini
drwxr-xr-x  3 root root     4096 Jul 25  2022 .oh-my-zsh
-rwxr-xr-x  1 root root      195 Oct 28 21:18 old_config.ini
-rw-r--r--  1 root root      667 Sep 19 17:29 run.txt
drwxr-xr-x  6 root root     4096 Dec 10  2022 STM32_HID_Bootloader
-rw-r--r--  1 root root     2439 May 28  2023 sysctl.conf
drwxr-xr-x  3 root root     4096 Oct 11 16:50 tenda
-rwxr-xr-x  1 root root     2149 Sep 27 14:06 timeup.sh
-rwxr-xr-x  1 root root    35000 May 28  2023 uart
-rwxrwxrwx  1 root root    35000 Feb 15  2019 uart-230400
-rwxrwxrwx  1 root root    20272 May 28  2023 udp_server
-rw-------  1 root root    10842 Oct 16 16:25 .viminfo
-rw-r--r--  1 root root      215 Jul 25  2022 .wget-hsts
-rw-------  1 root root      210 Dec 10  2022 .wpa_cli_history
drwxr-xr-x  2 root root     4096 Oct 28 21:18 www
-rw-------  1 root root      153 Oct 16 16:40 .Xauthority
drwxrwxrwx  3 root root     4096 Oct 28 21:18 xindi
-rw-r--r--  1 root root     3979 Jul 25  2022 .zshrc
root@mkspi:~# 
</pre>
</details>

---

// connecté en utilisateur mks

~~~
ls -la /home/mks
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
mks@mkspi:~$ ls -la
total 240
drwxr-xr-x 35 mks  mks   4096 Mar 10 06:30 .
drwxr-xr-x  3 root root  4096 Jul 25  2022 ..
-rw-------  1 mks  mks   1516 Mar 10 06:35 .bash_history
-rw-r--r--  1 mks  mks    220 Jul 25  2022 .bash_logout
-rw-r--r--  1 mks  mks   3601 Jul 25  2022 .bashrc
drwxr-xr-x  7 mks  mks   4096 Jul 26  2022 .cache
drwxrwxr-x  3 mks  mks   4096 Jul 25  2022 .cinnamon
drwxr-xr-x 10 mks  mks   4096 Dec 10  2022 .config
drwx------  3 mks  mks   4096 Jul 25  2022 .dbus
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Desktop
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Documents
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Downloads
drwxr-xr-x  6 mks  mks   4096 Oct 16 16:03 fluidd
drwxr-xr-x  4 mks  mks   4096 Oct 29 00:51 gcode_files
-rwxr-xr-x  1 root root  2493 May 27  2023 gene4.py
-rwxr-xr-x  1 root root   738 Jan  2 15:31 gene5.py
drwx------  3 mks  mks   4096 Jul 25  2022 .gnupg
drwx------  2 mks  mks   4096 Jul 25  2022 .gvfs
-rw-------  1 mks  mks    314 Jul 25  2022 .ICEauthority
drwxr-xr-x  7 mks  mks   4096 Jul 25  2022 kiauh
drwxr-xr-x  4 mks  mks   4096 Jul 25  2022 kiauh-backups
-rw-r--r--  1 mks  mks    589 Mar 10 06:30 .kiauh.ini
drwxrwxr-x 12 mks  mks   4096 Oct 16 19:50 klipper
drwxrwxr-x  2 mks  mks   4096 Oct 29 01:17 klipper_config
drwxr-xr-x  2 mks  mks   4096 Mar 10 05:47 klipper_logs
drwxr-xr-x  9 mks  mks   4096 Jul 25  2022 KlipperScreen
drwxr-xr-x  6 mks  mks   4096 Jul 25  2022 .KlipperScreen-env
drwxr-xr-x  7 mks  mks   4096 Jul 25  2022 klippy-env
-rwxr-xr-x  1 root root 12448 May 27  2023 libColPic.so
drwxrwxr-x  3 mks  mks   4096 Jul 25  2022 .local
drwxr-xr-x 10 mks  mks   4096 Jul 25  2022 mjpg-streamer
drwxrwxr-x  8 mks  mks   4096 Sep 26 15:21 moonraker
drwxr-xr-x  2 mks  mks   4096 Oct 28 13:17 .moonraker_database
drwxr-xr-x  6 mks  mks   4096 Jul 25  2022 moonraker-env
drwxr-xr-x  8 mks  mks   4096 Sep 27 13:44 moonraker-timelapse
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Music
drwxrwxr-x  3 mks  mks   4096 Jul 25  2022 .oh-my-zsh
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Pictures
drwxrwxrwx  2 root root  4096 Oct 28 21:18 plr
-rw-r--r--  1 mks  mks    807 Jul 25  2022 .profile
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Public
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Templates
drwxr-xr-x  2 mks  mks   4096 Oct  5 17:10 timelapse
-rwxr-xr-x  1 root root  6424 Oct 29 01:17 tjc
drwxr-xr-x  2 mks  mks   4096 Jul 25  2022 Videos
-rw-------  1 mks  mks   1052 Dec 10  2022 .viminfo
-rw-r--r--  1 mks  mks    215 Jul 25  2022 .wget-hsts
-rw-------  1 mks  mks    203 Oct 16 16:29 .Xauthority
-rw-r--r--  1 mks  mks   9441 Jul 25  2022 .xfce4-session.verbose-log
-rwxrwxr-x  1 mks  mks     20 Jul 25  2022 .xscreensaver
-rw-------  1 mks  mks   7460 Jul 25  2022 .xsession-errors
-rw-r--r--  1 root root    78 Jul 25  2022 .xsessionrc
-rw-rw-r--  1 mks  mks   3979 Jul 25  2022 .zshrc
mks@mkspi:~$ 
</pre>
</details>

---

// connecté en utilisateur mks

~~~
/home/mks/kiauh/kiauh.sh 
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
mks@mkspi:~$ ./kiauh/kiauh.sh 

/=======================================================\
|              New KIAUH update available!              |
|-------------------------------------------------------|
|  View Changelog: https://git.io/JnmlX                 |
|                                                       |
|  It is recommended to keep KIAUH up to date. Updates  |
|  usually contain bugfixes, important changes or new   |
|  features. Please consider updating!                  |
\=======================================================/
###### Do you want to update now? (Y/n): n
/=======================================================\
|     ~~~~~~~~~~~~~~~~~ [ KIAUH ] ~~~~~~~~~~~~~~~~~     |
|        Klipper Installation And Update Helper         |
|     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~     |
\=======================================================/
/=======================================================\
|     ~~~~~~~~~~~~~~~ [ Main Menu ] ~~~~~~~~~~~~~~~     |
|-------------------------------------------------------|
|  0) [Log-Upload]   |       Klipper: Installed: 1      |
|                    |          Repo: Klipper3d/klipper |
|  1) [Install]      |                                  |
|  2) [Update]       |     Moonraker: Installed: 1      |
|  3) [Remove]       |                                  |
|  4) [Advanced]     |      Mainsail: Not installed!    |
|  5) [Backup]       |        Fluidd: Installed!        |
|                    | KlipperScreen: Installed!        |
|  6) [Settings]     |  Telegram Bot: Not installed!    |
|                    |                                  |
|  v4.0.0-13         |     Octoprint: Not installed!    |
|-------------------------------------------------------|
|                        Q) Quit                        |
\=======================================================/
####### Perform action: 


/=======================================================\
|     ~~~~~~~~~~~~~~~~~ [ KIAUH ] ~~~~~~~~~~~~~~~~~     |
|        Klipper Installation And Update Helper         |
|     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~     |
\=======================================================/
/=======================================================\
|     ~~~~~~~~~~~~~~ [ Update Menu ] ~~~~~~~~~~~~~~     |
|-------------------------------------------------------|
| a) [Update all]        |               |              |
|                        | Installed:    | Latest:      |
| Klipper & API:         |---------------|--------------|
|  1) [Klipper]          | v0.10.0-530   | v0.12.0-117  |
|  2) [Moonraker]        | v0.7.1-609    | v0.8.0-320   |
|                        |               |              |
| Klipper Webinterface:  |---------------|--------------|
|  3) [Mainsail]         |               | v2.10.0      |
|  4) [Fluidd]           | v1.19.0       | v1.28.1      |
|                        |               |              |
| Touchscreen GUI:       |---------------|--------------|
|  5) [KlipperScreen]    | v0.2.4-17     | v0.3.9-31    |
|                        |               |              |
| Other:                 |---------------|--------------|
|  6) [PrettyGCode]      |               |              |
|  7) [Telegram Bot]     |               |              |
|                        |------------------------------|
|  8) [System]           |  System upgrade available!   |
|-------------------------------------------------------|
|                       B) « Back                       |
\=======================================================/
####### Perform action: 


</pre>
</details>

---


Altération éffectuées

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

~~~
apt list --installed
~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>
root@mkspi:~# apt list --installed
Listing... Done
acl/oldoldstable,now 2.2.53-4 arm64 [installed,automatic]
adduser/oldoldstable,oldoldstable,now 3.118 all [installed]
adwaita-icon-theme/oldoldstable,oldoldstable,now 3.30.1-1 all [installed]
alsa-utils/oldoldstable,now 1.1.8-2 arm64 [installed]
anacron/oldoldstable,now 2.3-28 arm64 [installed]
apt-utils/oldoldstable,oldoldstable-updates,now 1.8.2.3 arm64 [installed]
apt/oldoldstable,oldoldstable-updates,now 1.8.2.3 arm64 [installed]
aptitude-common/oldoldstable,oldoldstable,now 0.8.11-7 all [installed,automatic]
aptitude/oldoldstable,now 0.8.11-7 arm64 [installed]
armbian-bsp-cli-mkspi/now 22.05.0-trunk arm64 [installed,local]
armbian-buster-desktop-xfce/buster,buster,buster,now 22.05.4 all [installed,upgradable to: 23.02.2]
armbian-config/buster,buster,buster,now 22.08.0-trunk.0038 all [installed,upgradable to: 23.02.2]
armbian-firmware/buster,buster,buster,now 22.08.0-trunk.0038 all [installed,upgradable to: 23.02.2]
armbian-zsh/buster,buster,buster,now 22.08.0-trunk.0038 all [installed,upgradable to: 23.02.2]
at-spi2-core/oldoldstable,now 2.30.0-7 arm64 [installed,automatic]
autoconf/oldoldstable,oldoldstable,now 2.69-11 all [installed,automatic]
automake/oldoldstable,oldoldstable,now 1:1.16.1-4 all [installed]
autotools-dev/oldoldstable,oldoldstable,now 20180224.1 all [installed,automatic]
avahi-autoipd/oldoldstable,now 0.7-4+deb10u1 arm64 [installed,upgradable to: 0.7-4+deb10u3]
avr-libc/oldoldstable,oldoldstable,now 1:2.0.0+Atmel3.6.1-2 all [installed]
avrdude/oldoldstable,now 6.3-20171130+svn1429-2 arm64 [installed]
base-files/now 10.3+deb10u12 arm64 [installed,upgradable to: 10.3+deb10u13]
base-passwd/oldoldstable,now 3.5.46 arm64 [installed]
bash-completion/oldoldstable,oldoldstable,now 1:2.8-6 all [installed]
bash/oldoldstable,now 5.0-4 arm64 [installed]
bc/oldoldstable,now 1.07.1-2+b1 arm64 [installed]
bind9-host/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
binutils-aarch64-linux-gnu/oldoldstable,now 2.31.1-16 arm64 [installed,automatic]
binutils-arm-none-eabi/oldoldstable,now 2.31.1-12+11 arm64 [installed]
binutils-avr/oldoldstable,now 2.26.20160125+Atmel3.6.1-4 arm64 [installed]
binutils-common/oldoldstable,now 2.31.1-16 arm64 [installed,automatic]
binutils/oldoldstable,now 2.31.1-16 arm64 [installed,automatic]
bison/oldoldstable,now 2:3.3.2.dfsg-1 arm64 [installed]
blueman/oldoldstable,oldoldstable,now 2.0.8-1+deb10u1 arm64 [installed]
bluez-cups/oldoldstable,now 5.50-1.2~deb10u2 arm64 [installed,upgradable to: 5.50-1.2~deb10u3]
bluez-obexd/oldoldstable,now 5.50-1.2~deb10u2 arm64 [installed,upgradable to: 5.50-1.2~deb10u3]
bluez-tools/oldoldstable,now 2.0~20170911.0.7cb788c-2 arm64 [installed]
bluez/oldoldstable,now 5.50-1.2~deb10u2 arm64 [installed,upgradable to: 5.50-1.2~deb10u3]
bridge-utils/oldoldstable,now 1.6-2 arm64 [installed]
brltty-x11/oldoldstable,now 5.6-10+deb10u1 arm64 [installed]
brltty/oldoldstable,now 5.6-10+deb10u1 arm64 [installed]
bsdmainutils/oldoldstable,now 11.1.2+b1 arm64 [installed,automatic]
bsdutils/oldoldstable,now 1:2.33.1-0.1 arm64 [installed]
btrfs-progs/oldoldstable,now 4.20.1-2 arm64 [installed]
bubblewrap/oldoldstable,now 0.3.1-4 arm64 [installed,automatic]
build-essential/oldoldstable,now 12.6 arm64 [installed]
bzip2/oldoldstable,now 1.0.6-9.2~deb10u1 arm64 [installed,upgradable to: 1.0.6-9.2~deb10u2]
ca-certificates/oldoldstable,oldoldstable,oldoldstable-updates,oldoldstable-updates,now 20200601~deb10u2 all [installed]
caffeine/oldoldstable,oldoldstable,now 2.9.4-2 all [installed]
cifs-utils/oldoldstable,oldoldstable,now 2:6.8-2+deb10u1 arm64 [installed]
cmake-data/oldoldstable,oldoldstable,now 3.13.4-1 all [installed,automatic]
cmake/oldoldstable,now 3.13.4-1 arm64 [installed]
console-setup-linux/oldoldstable,oldoldstable,now 1.193~deb10u1 all [installed]
console-setup/oldoldstable,oldoldstable,now 1.193~deb10u1 all [installed]
coreutils/oldoldstable,now 8.30-3 arm64 [installed]
cpio/oldoldstable,now 2.12+dfsg-9 arm64 [installed,upgradable to: 2.12+dfsg-9+deb10u1]
cpp-8/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
cpp/oldoldstable,now 4:8.3.0-1 arm64 [installed,automatic]
cpufrequtils/oldoldstable,now 008-1.1 arm64 [installed]
cracklib-runtime/oldoldstable,now 2.9.6-2 arm64 [installed]
cron/oldoldstable,now 3.0pl1-134+deb10u1 arm64 [installed]
cups-bsd/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
cups-client/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
cups-common/oldoldstable,oldoldstable,now 2.2.10-6+deb10u6 all [installed,upgradable to: 2.2.10-6+deb10u9]
cups-core-drivers/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
cups-daemon/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
cups-filters-core-drivers/oldoldstable,now 1.21.6-5 arm64 [installed,upgradable to: 1.21.6-5+deb10u1]
cups-filters/oldoldstable,now 1.21.6-5 arm64 [installed,upgradable to: 1.21.6-5+deb10u1]
cups-ipp-utils/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
cups-ppdc/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
cups-server-common/oldoldstable,oldoldstable,now 2.2.10-6+deb10u6 all [installed,upgradable to: 2.2.10-6+deb10u9]
cups/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
curl/oldoldstable,now 7.64.0-4+deb10u2 arm64 [installed,upgradable to: 7.64.0-4+deb10u6]
dash/oldoldstable,now 0.5.10.2-5 arm64 [installed]
dbus-x11/oldoldstable,now 1.12.20-0+deb10u1 arm64 [installed,upgradable to: 1.12.24-0+deb10u1]
dbus/oldoldstable,now 1.12.20-0+deb10u1 arm64 [installed,upgradable to: 1.12.24-0+deb10u1]
dconf-gsettings-backend/oldoldstable,now 0.30.1-2 arm64 [installed,automatic]
dconf-service/oldoldstable,now 0.30.1-2 arm64 [installed,automatic]
debconf-utils/oldoldstable,oldoldstable,now 1.5.71+deb10u1 all [installed]
debconf/oldoldstable,oldoldstable,now 1.5.71+deb10u1 all [installed]
debian-archive-keyring/oldoldstable,oldoldstable,now 2019.1+deb10u1 all [installed,upgradable to: 2019.1+deb10u2]
debianutils/oldoldstable,now 4.8.6.1 arm64 [installed]
desktop-file-utils/oldoldstable,now 0.23-4 arm64 [installed,automatic]
device-tree-compiler/oldoldstable,now 1.4.7-4 arm64 [installed]
dfu-util/oldoldstable,now 0.9-1 arm64 [installed]
dh-python/oldoldstable,oldoldstable,now 3.20190308 all [installed,automatic]
dhcpcd5/oldoldstable,now 7.1.0-2 arm64 [installed]
dialog/oldoldstable,now 1.3-20190211-1 arm64 [installed]
dictionaries-common/oldoldstable,oldoldstable,now 1.28.1 all [installed]
diffutils/oldoldstable,now 1:3.7-3 arm64 [installed]
dirmngr/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
distro-info-data/now 0.41+deb10u4 all [installed,upgradable to: 0.41+deb10u7]
dmsetup/oldoldstable,now 2:1.02.155-3 arm64 [installed]
dmz-cursor-theme/oldoldstable,oldoldstable,now 0.4.5 all [installed]
dnsutils/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
doc-base/oldoldstable,oldoldstable,now 0.10.8 all [installed]
dos2unix/oldoldstable,now 7.4.0-1 arm64 [installed]
dosfstools/oldoldstable,now 4.1-2 arm64 [installed]
dpkg-dev/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 1.19.8 all [installed,automatic]
dpkg/oldoldstable,oldoldstable,now 1.19.8 arm64 [installed]
e2fsprogs/oldoldstable,now 1.44.5-1+deb10u3 arm64 [installed]
emacsen-common/oldoldstable,oldoldstable,now 3.0.4 all [installed,automatic]
ethtool/oldoldstable,now 1:4.19-1 arm64 [installed]
evince-common/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 3.30.2-3+deb10u1 all [installed]
evince/oldoldstable,oldoldstable,now 3.30.2-3+deb10u1 arm64 [installed]
evtest/oldoldstable,now 1:1.33-2 arm64 [installed]
exo-utils/oldoldstable,oldoldstable,now 0.12.4-1+deb10u1 arm64 [installed,automatic]
expect/oldoldstable,now 5.45.4-2 arm64 [installed]
f2fs-tools/oldoldstable,now 1.11.0-1.1 arm64 [installed]
f3/oldoldstable,now 7.1-1 arm64 [installed]
fake-hwclock/oldoldstable,oldoldstable,now 0.11 all [installed]
fbset/oldoldstable,now 2.1-30 arm64 [installed]
fdisk/oldoldstable,now 2.33.1-0.1 arm64 [installed]
ffmpeg/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
figlet/oldoldstable,now 2.2.5-3 arm64 [installed]
file/oldoldstable,now 1:5.35-4+deb10u2 arm64 [installed,automatic]
findutils/oldoldstable,now 4.6.0+git+20190209-2 arm64 [installed]
flex/oldoldstable,now 2.6.4-6.2 arm64 [installed]
fontconfig-config/oldoldstable,oldoldstable,now 2.13.1-2 all [installed]
fontconfig/oldoldstable,now 2.13.1-2 arm64 [installed]
fonts-arphic-ukai/oldoldstable,oldoldstable,now 0.2.20080216.2-4 all [installed]
fonts-arphic-uming/oldoldstable,oldoldstable,now 0.2.20080216.2-10 all [installed]
fonts-dejavu-core/oldoldstable,oldoldstable,now 2.37-1 all [installed]
fonts-freefont-ttf/oldoldstable,oldoldstable,now 20120503-9 all [installed]
fonts-guru-extra/oldoldstable,oldoldstable,now 2.0-4 all [installed]
fonts-guru/oldoldstable,oldoldstable,now 2:1.2 all [installed]
fonts-kacst-one/oldoldstable,oldoldstable,now 5.0+svn11846-9 all [installed]
fonts-kacst/oldoldstable,oldoldstable,now 2.01+mry-14 all [installed]
fonts-liberation/oldoldstable,oldoldstable,now 1:1.07.4-9 all [installed]
fonts-lohit-guru/oldoldstable,oldoldstable,now 2.91.2-1 all [installed,automatic]
fonts-lyx/oldoldstable,oldoldstable,now 2.3.2-1 all [installed,automatic]
fonts-nanum/oldoldstable,oldoldstable,now 20180306-1 all [installed]
fonts-opensymbol/oldoldstable,oldoldstable,now 2:102.10+LibO6.1.5-3+deb10u7 all [installed,upgradable to: 2:102.10+LibO6.1.5-3+deb10u10]
fonts-stix/oldoldstable,oldoldstable,now 1.1.1-4 all [installed]
fonts-symbola/oldoldstable,oldoldstable,now 2.60-1 all [installed]
fonts-ubuntu-console/oldoldstable,oldoldstable,now 0.83-4 all [installed,automatic]
fonts-ubuntu-font-family-console/oldoldstable,oldoldstable,now 1:0.83-4 all [installed]
fonts-ubuntu/oldoldstable,oldoldstable,now 0.83-4 all [installed,automatic]
foomatic-db-compressed-ppds/oldoldstable,oldoldstable,now 20181217-2 all [installed]
fping/oldoldstable,now 4.2-1 arm64 [installed]
fuse/oldoldstable,now 2.9.9-1+deb10u1 arm64 [installed,automatic]
g++-8/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
g++/oldoldstable,now 4:8.3.0-1 arm64 [installed,automatic]
gcc-8-base/oldoldstable,now 8.3.0-6 arm64 [installed]
gcc-8/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
gcc-arm-none-eabi/oldoldstable,now 15:7-2018-q2-6 arm64 [installed]
gcc-avr/oldoldstable,now 1:5.4.0+Atmel3.6.1-2 arm64 [installed]
gcc/oldoldstable,now 4:8.3.0-1 arm64 [installed]
gdebi-core/oldoldstable,oldoldstable,now 0.9.5.7+nmu3 all [installed,automatic]
gdebi/oldoldstable,oldoldstable,now 0.9.5.7+nmu3 all [installed]
gdisk/oldoldstable,now 1.0.3-1.1 arm64 [installed,automatic]
ghostscript-x/oldoldstable,now 9.27~dfsg-2+deb10u5 arm64 [installed,upgradable to: 9.27~dfsg-2+deb10u9]
ghostscript/oldoldstable,now 9.27~dfsg-2+deb10u5 arm64 [installed,upgradable to: 9.27~dfsg-2+deb10u9]
gir1.2-appindicator3-0.1/oldoldstable,now 0.4.92-7 arm64 [installed,automatic]
gir1.2-atk-1.0/oldoldstable,now 2.30.0-2 arm64 [installed,automatic]
gir1.2-atspi-2.0/oldoldstable,now 2.30.0-7 arm64 [installed,automatic]
gir1.2-ayatanaappindicator3-0.1/oldoldstable,now 0.5.3-4 arm64 [installed,automatic]
gir1.2-freedesktop/oldoldstable,now 1.58.3-2 arm64 [installed,automatic]
gir1.2-gdkpixbuf-2.0/oldoldstable,now 2.38.1+dfsg-1 arm64 [installed,automatic]
gir1.2-glib-2.0/oldoldstable,now 1.58.3-2 arm64 [installed,automatic]
gir1.2-gtk-3.0/oldoldstable,now 3.24.5-1 arm64 [installed]
gir1.2-notify-0.7/oldoldstable,now 0.7.7-4 arm64 [installed,automatic]
gir1.2-packagekitglib-1.0/oldoldstable,now 1.1.12-5 arm64 [installed,automatic]
gir1.2-pango-1.0/oldoldstable,now 1.42.4-8~deb10u1 arm64 [installed,automatic]
gir1.2-polkit-1.0/oldoldstable,oldoldstable,now 0.105-25+deb10u1 arm64 [installed,automatic]
gir1.2-vte-2.91/oldoldstable,now 0.54.2-2 arm64 [installed,automatic]
gir1.2-wnck-3.0/oldoldstable,now 3.30.0-2 arm64 [installed,automatic]
git-man/oldoldstable,oldoldstable,now 1:2.20.1-2+deb10u3 all [installed,upgradable to: 1:2.20.1-2+deb10u8]
git/oldoldstable,now 1:2.20.1-2+deb10u3 arm64 [installed,upgradable to: 1:2.20.1-2+deb10u8]
glib-networking-common/oldoldstable,oldoldstable,now 2.58.0-2+deb10u2 all [installed,automatic]
glib-networking-services/oldoldstable,now 2.58.0-2+deb10u2 arm64 [installed,automatic]
glib-networking/oldoldstable,now 2.58.0-2+deb10u2 arm64 [installed,automatic]
gnome-desktop3-data/oldoldstable,oldoldstable,now 3.30.2.1-2 all [installed,automatic]
gnome-font-viewer/oldoldstable,now 3.30.0-2 arm64 [installed]
gnome-icon-theme/oldoldstable,oldoldstable,now 3.12.0-3 all [installed,automatic]
gnome-orca/now 3.30.1-1 all [installed,upgradable to: 3.30.1-2]
gnupg-l10n/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 all [installed]
gnupg-utils/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gnupg/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 all [installed]
gobject-introspection/oldoldstable,now 1.58.3-2 arm64 [installed,automatic]
gpg-agent/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gpg-wks-client/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gpg-wks-server/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gpg/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gpgconf/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gpgsm/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
gpgv/oldoldstable,oldoldstable,now 2.2.12-1+deb10u2 arm64 [installed]
grep/oldoldstable,now 3.3-1 arm64 [installed]
groff-base/oldoldstable,now 1.22.4-3+deb10u1 arm64 [installed,automatic]
gsettings-desktop-schemas/oldoldstable,oldoldstable,now 3.28.1-1 all [installed,automatic]
gstreamer1.0-packagekit/oldoldstable,now 1.1.12-5 arm64 [installed]
gstreamer1.0-plugins-base-apps/oldoldstable,now 1.14.4-2+deb10u1 arm64 [installed,upgradable to: 1.14.4-2+deb10u2]
gstreamer1.0-plugins-base/oldoldstable,now 1.14.4-2+deb10u1 arm64 [installed,upgradable to: 1.14.4-2+deb10u2]
gstreamer1.0-pulseaudio/oldoldstable,now 1.14.4-1+deb10u1 arm64 [installed,upgradable to: 1.14.4-1+deb10u3]
gstreamer1.0-tools/oldoldstable,now 1.14.4-1 arm64 [installed,automatic]
gtk-update-icon-cache/oldoldstable,now 3.24.5-1 arm64 [installed]
gtk2-engines-murrine/oldoldstable,now 0.98.2-2+deb10u1 arm64 [installed]
gtk2-engines-pixbuf/oldoldstable,now 2.24.32-3 arm64 [installed]
gtk2-engines-xfce/oldoldstable,now 3.2.0-4 arm64 [installed,automatic]
gtk2-engines/oldoldstable,now 1:2.20.2-5 arm64 [installed]
gvfs-backends/oldoldstable,now 1.38.1-5 arm64 [installed]
gvfs-common/oldoldstable,oldoldstable,now 1.38.1-5 all [installed,automatic]
gvfs-daemons/oldoldstable,now 1.38.1-5 arm64 [installed,automatic]
gvfs-libs/oldoldstable,now 1.38.1-5 arm64 [installed,automatic]
gvfs/oldoldstable,now 1.38.1-5 arm64 [installed,automatic]
gzip/oldoldstable,oldoldstable,now 1.9-3+deb10u1 arm64 [installed]
haveged/oldoldstable,now 1.9.1-7 arm64 [installed]
hdparm/oldoldstable,now 9.58+ds-1 arm64 [installed]
hicolor-icon-theme/oldoldstable,oldoldstable,now 0.17-2 all [installed]
hostapd/buster,now 3:2.9-102~armbian20.05.2+1 arm64 [installed]
hostname/oldoldstable,now 3.21 arm64 [installed]
hplip-data/oldoldstable,oldoldstable,now 3.18.12+dfsg0-2 all [installed,automatic]
hplip/oldoldstable,now 3.18.12+dfsg0-2 arm64 [installed]
html2text/oldoldstable,now 1.3.2a-24 arm64 [installed]
htop/now 3.1.0-0~armbian20.08.2+1 arm64 [installed,local]
hunspell-en-us/oldoldstable,oldoldstable,now 1:2018.04.16-1 all [installed]
i2c-tools/oldoldstable,now 4.1-1 arm64 [installed]
ibverbs-providers/oldoldstable,now 22.1-1 arm64 [installed,automatic]
icu-devtools/oldoldstable,now 63.1-6+deb10u3 arm64 [installed,automatic]
ifenslave/oldoldstable,oldoldstable,now 2.9 all [installed]
ifupdown/oldoldstable,now 0.8.35 arm64 [installed]
imagemagick-6-common/oldoldstable,oldoldstable,now 8:6.9.10.23+dfsg-2.1+deb10u1 all [installed,upgradable to: 8:6.9.10.23+dfsg-2.1+deb10u5]
imagemagick-6.q16/oldoldstable,now 8:6.9.10.23+dfsg-2.1+deb10u1 arm64 [installed,upgradable to: 8:6.9.10.23+dfsg-2.1+deb10u5]
imagemagick/oldoldstable,now 8:6.9.10.23+dfsg-2.1+deb10u1 arm64 [installed,upgradable to: 8:6.9.10.23+dfsg-2.1+deb10u5]
init-system-helpers/oldoldstable,oldoldstable,now 1.56+nmu1 all [installed]
init/oldoldstable,now 1.56+nmu1 arm64 [installed]
initramfs-tools-core/oldoldstable,oldoldstable,now 0.133+deb10u1 all [installed]
initramfs-tools/oldoldstable,oldoldstable,now 0.133+deb10u1 all [installed]
inputattach/oldoldstable,now 1:1.6.1-1 arm64 [installed]
iotop/oldoldstable,now 0.6-24-g733f3f8-1 arm64 [installed]
iozone3/oldoldstable,now 429-3+b1 arm64 [installed]
iperf3/oldoldstable,now 3.6-2 arm64 [installed,upgradable to: 3.6-2+deb10u1]
iproute2/oldoldstable,now 4.20.0-2+deb10u1 arm64 [installed]
iptables/oldoldstable,now 1.8.2-4 arm64 [installed]
iputils-arping/oldoldstable,now 3:20180629-2+deb10u2 arm64 [installed]
iputils-ping/oldoldstable,now 3:20180629-2+deb10u2 arm64 [installed]
isc-dhcp-client/oldoldstable,now 4.4.1-2+deb10u1 arm64 [installed,upgradable to: 4.4.1-2+deb10u3]
iso-codes/oldoldstable,oldoldstable,now 4.2-1 all [installed,automatic]
iw/oldoldstable,now 5.0.1-1 arm64 [installed]
jq/oldoldstable,now 1.5+dfsg-2+b1 arm64 [installed]
kbd/oldoldstable,now 2.0.4-4 arm64 [installed]
keyboard-configuration/oldoldstable,oldoldstable,now 1.193~deb10u1 all [installed]
keyutils/oldoldstable,now 1.6-6 arm64 [installed]
klibc-utils/oldoldstable,now 2.0.6-1+deb10u1 arm64 [installed]
kmod/oldoldstable,now 26-1 arm64 [installed]
laptop-detect/oldoldstable,oldoldstable,now 0.16 all [installed]
less/oldoldstable,now 487-0.1+b1 arm64 [installed]
libacl1/oldoldstable,now 2.2.53-4 arm64 [installed]
libao-common/oldoldstable,oldoldstable,now 1.2.2+20180113-1 all [installed,automatic]
libao4/oldoldstable,now 1.2.2+20180113-1 arm64 [installed,automatic]
libaom0/oldoldstable,now 1.0.0-3 arm64 [installed,upgradable to: 1.0.0-3+deb10u1]
libapparmor1/oldoldstable,now 2.13.2-10 arm64 [installed]
libappindicator3-1/oldoldstable,now 0.4.92-7 arm64 [installed,automatic]
libappstream4/oldoldstable,now 0.12.5-1 arm64 [installed,automatic]
libapt-inst2.0/oldoldstable,oldoldstable-updates,now 1.8.2.3 arm64 [installed]
libapt-pkg5.0/oldoldstable,oldoldstable-updates,now 1.8.2.3 arm64 [installed]
libarchive13/oldoldstable,now 3.3.3-4+deb10u1 arm64 [installed,upgradable to: 3.3.3-4+deb10u3]
libargon2-1/oldoldstable,now 0~20171227-0.2 arm64 [installed]
libasan5/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libasound2-data/oldoldstable,oldoldstable,now 1.1.8-1 all [installed,automatic]
libasound2-plugins/oldoldstable,now 1.1.8-1 arm64 [installed,automatic]
libasound2/oldoldstable,now 1.1.8-1 arm64 [installed,automatic]
libaspell15/oldoldstable,oldoldstable,now 0.60.7~20110707-6+deb10u1 arm64 [installed,automatic]
libass9/oldoldstable,now 1:0.14.0-2 arm64 [installed,automatic]
libassuan0/oldoldstable,now 2.5.2-1 arm64 [installed]
libasyncns0/oldoldstable,now 0.8-6 arm64 [installed,automatic]
libatasmart4/oldoldstable,now 0.19-5 arm64 [installed,automatic]
libatk-adaptor/oldoldstable,now 2.30.0-5 arm64 [installed]
libatk-bridge2.0-0/oldoldstable,now 2.30.0-5 arm64 [installed,automatic]
libatk1.0-0/oldoldstable,now 2.30.0-2 arm64 [installed]
libatk1.0-data/oldoldstable,oldoldstable,now 2.30.0-2 all [installed]
libatkmm-1.6-1v5/oldoldstable,now 2.28.0-2 arm64 [installed,automatic]
libatlas-base-dev/oldoldstable,now 3.10.3-8 arm64 [installed]
libatlas3-base/oldoldstable,now 3.10.3-8 arm64 [installed,automatic]
libatomic1/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libatspi2.0-0/oldoldstable,now 2.30.0-7 arm64 [installed,automatic]
libattr1/oldoldstable,now 1:2.4.48-4 arm64 [installed]
libaudio2/oldoldstable,now 1.9.4-6 arm64 [installed,automatic]
libaudit-common/oldoldstable,oldoldstable,now 1:2.8.4-3 all [installed]
libaudit1/oldoldstable,now 1:2.8.4-3 arm64 [installed]
libavahi-client3/oldoldstable,now 0.7-4+deb10u1 arm64 [installed,upgradable to: 0.7-4+deb10u3]
libavahi-common-data/oldoldstable,now 0.7-4+deb10u1 arm64 [installed,upgradable to: 0.7-4+deb10u3]
libavahi-common3/oldoldstable,now 0.7-4+deb10u1 arm64 [installed,upgradable to: 0.7-4+deb10u3]
libavahi-glib1/oldoldstable,now 0.7-4+deb10u1 arm64 [installed,upgradable to: 0.7-4+deb10u3]
libavc1394-0/oldoldstable,now 0.5.4-5 arm64 [installed,automatic]
libavcodec58/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libavdevice58/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libavfilter7/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libavformat58/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libavresample4/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libavutil56/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libayatana-appindicator3-1/oldoldstable,now 0.5.3-4 arm64 [installed,automatic]
libayatana-ido3-0.4-0/oldoldstable,now 0.4.4-1 arm64 [installed,automatic]
libayatana-indicator3-7/oldoldstable,now 0.6.2-3 arm64 [installed,automatic]
libbind9-161/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libbinutils/oldoldstable,now 2.31.1-16 arm64 [installed,automatic]
libbison-dev/oldoldstable,now 2:3.3.2.dfsg-1 arm64 [installed,automatic]
libblkid-dev/oldoldstable,now 2.33.1-0.1 arm64 [installed,automatic]
libblkid1/oldoldstable,now 2.33.1-0.1 arm64 [installed]
libblockdev-fs2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libblockdev-loop2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libblockdev-part-err2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libblockdev-part2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libblockdev-swap2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libblockdev-utils2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libblockdev2/oldoldstable,now 2.20-7+deb10u1 arm64 [installed,automatic]
libbluetooth3/oldoldstable,now 5.50-1.2~deb10u2 arm64 [installed,upgradable to: 5.50-1.2~deb10u3]
libbluray2/oldoldstable,now 1:1.1.0-1 arm64 [installed,upgradable to: 1:1.1.0-1+deb10u1]
libboost-all-dev/oldoldstable,now 1.67.0.1 arm64 [installed]
libboost-atomic-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-atomic1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-atomic1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-chrono-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-chrono1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-chrono1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-container-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-container1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-container1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-context-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-context1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-context1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-coroutine-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-coroutine1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-coroutine1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-date-time-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-date-time1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-date-time1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-exception-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-exception1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-fiber-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-fiber1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-fiber1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-filesystem-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-filesystem1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-filesystem1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-graph-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-graph-parallel-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-graph-parallel1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-graph-parallel1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-graph1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-graph1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-iostreams-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-iostreams1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-iostreams1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-locale-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-locale1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-locale1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-log-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-log1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-log1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-math-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-math1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-math1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-mpi-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-mpi-python-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-mpi-python1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-mpi-python1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-mpi1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-mpi1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-numpy-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-numpy1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-numpy1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-program-options-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-program-options1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-program-options1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-python-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-python1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-python1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-random-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-random1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-random1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-regex-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-regex1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-regex1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-serialization-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-serialization1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-serialization1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-signals-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-signals1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-signals1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-stacktrace-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-stacktrace1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-stacktrace1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-system-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-system1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-system1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-test-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-test1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-test1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-thread-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-thread1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-thread1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-timer-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-timer1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-timer1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-tools-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-type-erasure-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-type-erasure1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-type-erasure1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-wave-dev/oldoldstable,now 1.67.0.1 arm64 [installed,automatic]
libboost-wave1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost-wave1.67.0/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost1.67-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libboost1.67-tools-dev/oldoldstable,now 1.67.0-13+deb10u1 arm64 [installed,automatic]
libbrlapi0.6/oldoldstable,now 5.6-10+deb10u1 arm64 [installed,automatic]
libbs2b0/oldoldstable,now 3.1.0+dfsg-2.2 arm64 [installed,automatic]
libbsd0/oldoldstable,now 0.9.1-2+deb10u1 arm64 [installed]
libbz2-1.0/oldoldstable,now 1.0.6-9.2~deb10u1 arm64 [installed,upgradable to: 1.0.6-9.2~deb10u2]
libc-bin/oldoldstable,now 2.28-10+deb10u1 arm64 [installed,upgradable to: 2.28-10+deb10u2]
libc-dev-bin/oldoldstable,now 2.28-10+deb10u1 arm64 [installed,upgradable to: 2.28-10+deb10u2]
libc-l10n/oldoldstable,oldoldstable,now 2.28-10+deb10u1 all [installed,upgradable to: 2.28-10+deb10u2]
libc6-dev/oldoldstable,now 2.28-10+deb10u1 arm64 [installed,upgradable to: 2.28-10+deb10u2]
libc6/oldoldstable,now 2.28-10+deb10u1 arm64 [installed,upgradable to: 2.28-10+deb10u2]
libcaca0/oldoldstable,now 0.99.beta19-2.1 arm64 [installed,automatic]
libcairo-gobject2/oldoldstable,now 1.16.0-4+deb10u1 arm64 [installed,automatic]
libcairo-script-interpreter2/oldoldstable,now 1.16.0-4+deb10u1 arm64 [installed,automatic]
libcairo2-dev/oldoldstable,now 1.16.0-4+deb10u1 arm64 [installed]
libcairo2/oldoldstable,now 1.16.0-4+deb10u1 arm64 [installed]
libcairomm-1.0-1v5/oldoldstable,now 1.12.2-4 arm64 [installed,automatic]
libcanberra-gtk3-0/oldoldstable,now 0.30-7 arm64 [installed,automatic]
libcanberra0/oldoldstable,now 0.30-7 arm64 [installed,automatic]
libcap-ng0/oldoldstable,now 0.7.9-2 arm64 [installed]
libcap2-bin/oldoldstable,now 1:2.25-2 arm64 [installed]
libcap2/oldoldstable,now 1:2.25-2 arm64 [installed]
libcc1-0/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libcdio-cdda2/oldoldstable,now 10.2+0.94+2-4 arm64 [installed,automatic]
libcdio-paranoia2/oldoldstable,now 10.2+0.94+2-4 arm64 [installed,automatic]
libcdio18/oldoldstable,now 2.0.0-2 arm64 [installed,automatic]
libcdparanoia0/oldoldstable,now 3.10.2+debian-13 arm64 [installed,automatic]
libchromaprint1/oldoldstable,now 1.4.3-3 arm64 [installed,automatic]
libcodec2-0.8.1/oldoldstable,now 0.8.1-2 arm64 [installed,automatic]
libcolord2/oldoldstable,now 1.4.3-4 arm64 [installed,automatic]
libcom-err2/oldoldstable,now 1.44.5-1+deb10u3 arm64 [installed]
libcpufreq0/oldoldstable,now 008-1.1 arm64 [installed,automatic]
libcrack2/oldoldstable,now 2.9.6-2 arm64 [installed]
libcroco3/oldoldstable,now 0.6.12-3 arm64 [installed]
libcryptsetup12/oldoldstable,now 2:2.1.0-5+deb10u2 arm64 [installed]
libcups2/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
libcupsfilters1/oldoldstable,now 1.21.6-5 arm64 [installed,upgradable to: 1.21.6-5+deb10u1]
libcupsimage2/oldoldstable,now 2.2.10-6+deb10u6 arm64 [installed,upgradable to: 2.2.10-6+deb10u9]
libcurl3-gnutls/oldoldstable,now 7.64.0-4+deb10u2 arm64 [installed,upgradable to: 7.64.0-4+deb10u6]
libcurl4-openssl-dev/oldoldstable,now 7.64.0-4+deb10u2 arm64 [installed,upgradable to: 7.64.0-4+deb10u6]
libcurl4/oldoldstable,now 7.64.0-4+deb10u2 arm64 [installed,upgradable to: 7.64.0-4+deb10u6]
libcwidget3v5/oldoldstable,now 0.5.17-11 arm64 [installed,automatic]
libdaemon0/oldoldstable,now 0.14-7 arm64 [installed,automatic]
libdatrie1/oldoldstable,now 0.2.12-2 arm64 [installed]
libdb5.3/oldoldstable,now 5.3.28+dfsg1-0.5 arm64 [installed]
libdbus-1-3/oldoldstable,now 1.12.20-0+deb10u1 arm64 [installed,upgradable to: 1.12.24-0+deb10u1]
libdbus-1-dev/oldoldstable,now 1.12.20-0+deb10u1 arm64 [installed,upgradable to: 1.12.24-0+deb10u1]
libdbus-glib-1-2/oldoldstable,now 0.110-4 arm64 [installed,automatic]
libdbusmenu-glib4/oldoldstable,now 18.10.20180917~bzr490+repack1-1 arm64 [installed,automatic]
libdbusmenu-gtk3-4/oldoldstable,now 18.10.20180917~bzr490+repack1-1 arm64 [installed,automatic]
libdc1394-22/oldoldstable,now 2.2.5-1 arm64 [installed,automatic]
libdconf1/oldoldstable,now 0.30.1-2 arm64 [installed,automatic]
libde265-0/oldoldstable,now 1.0.3-1+b1 arm64 [installed,upgradable to: 1.0.11-0+deb10u4]
libdebconfclient0/oldoldstable,now 0.249 arm64 [installed]
libdevmapper1.02.1/oldoldstable,now 2:1.02.155-3 arm64 [installed]
libdigest-sha-perl/oldoldstable,now 6.02-1+b1 arm64 [installed]
libdjvulibre-text/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 3.5.27.1-10+deb10u1 all [installed,automatic]
libdjvulibre21/oldoldstable,oldoldstable,now 3.5.27.1-10+deb10u1 arm64 [installed,automatic]
libdns-export1104/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libdns1104/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libdotconf0/oldoldstable,now 1.3-0.3 arm64 [installed,automatic]
libdouble-conversion1/oldoldstable,now 3.1.0-3 arm64 [installed,automatic]
libdpkg-perl/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 1.19.8 all [installed,automatic]
libdrm-amdgpu1/oldoldstable,now 2.4.97-1 arm64 [installed,automatic]
libdrm-common/oldoldstable,oldoldstable,now 2.4.97-1 all [installed,automatic]
libdrm-etnaviv1/oldoldstable,now 2.4.97-1 arm64 [installed,automatic]
libdrm-nouveau2/oldoldstable,now 2.4.97-1 arm64 [installed,automatic]
libdrm-radeon1/oldoldstable,now 2.4.97-1 arm64 [installed,automatic]
libdrm2/oldoldstable,now 2.4.97-1 arm64 [installed,automatic]
libdw1/oldoldstable,now 0.176-1.1 arm64 [installed,upgradable to: 0.176-1.1+deb10u1]
libedit2/oldoldstable,now 3.1-20181209-1 arm64 [installed,automatic]
libegl-mesa0/oldoldstable,now 18.3.6-2+deb10u1 arm64 [installed,automatic]
libegl1-mesa/oldoldstable,now 18.3.6-2+deb10u1 arm64 [installed,automatic]
libegl1/oldoldstable,now 1.1.0-1 arm64 [installed,automatic]
libelf1/oldoldstable,now 0.176-1.1 arm64 [installed,upgradable to: 0.176-1.1+deb10u1]
libenchant1c2a/oldoldstable,now 1.6.0-11.1+b1 arm64 [installed,automatic]
libencode-locale-perl/oldoldstable,oldoldstable,now 1.05-1 all [installed,automatic]
libepoxy0/oldoldstable,now 1.5.3-0.1 arm64 [installed,automatic]
liberror-perl/oldoldstable,oldoldstable,now 0.17027-2 all [installed,automatic]
libestr0/oldoldstable,now 0.1.10-2.1 arm64 [installed]
libevdev2/oldoldstable,now 1.6.0+dfsg-1 arm64 [installed,automatic]
libevdocument3-4/oldoldstable,oldoldstable,now 3.30.2-3+deb10u1 arm64 [installed,automatic]
libevent-2.1-6/oldoldstable,now 2.1.8-stable-4 arm64 [installed,automatic]
libevent-core-2.1-6/oldoldstable,now 2.1.8-stable-4 arm64 [installed,automatic]
libevent-pthreads-2.1-6/oldoldstable,now 2.1.8-stable-4 arm64 [installed,automatic]
libevview3-3/oldoldstable,oldoldstable,now 3.30.2-3+deb10u1 arm64 [installed,automatic]
libexif12/oldoldstable,oldoldstable,now 0.6.21-5.1+deb10u5 arm64 [installed,automatic]
libexiv2-14/oldoldstable,now 0.25-4+deb10u2 arm64 [installed,upgradable to: 0.25-4+deb10u4]
libexo-1-0/oldoldstable,oldoldstable,now 0.12.4-1+deb10u1 arm64 [installed,automatic]
libexo-2-0/oldoldstable,oldoldstable,now 0.12.4-1+deb10u1 arm64 [installed,automatic]
libexo-common/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 0.12.4-1+deb10u1 all [installed,automatic]
libexo-helpers/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 0.12.4-1+deb10u1 all [installed,automatic]
libexpat1-dev/oldoldstable,now 2.2.6-2+deb10u4 arm64 [installed,upgradable to: 2.2.6-2+deb10u6]
libexpat1/oldoldstable,now 2.2.6-2+deb10u4 arm64 [installed,upgradable to: 2.2.6-2+deb10u6]
libext2fs2/oldoldstable,now 1.44.5-1+deb10u3 arm64 [installed]
libf2fs-format4/oldoldstable,now 1.11.0-1.1 arm64 [installed,automatic]
libf2fs5/oldoldstable,now 1.11.0-1.1 arm64 [installed,automatic]
libfakekey0/oldoldstable,now 0.1-10 arm64 [installed,automatic]
libfastjson4/oldoldstable,now 0.99.8-2 arm64 [installed,upgradable to: 0.99.8-2+deb10u1]
libfdisk1/oldoldstable,now 2.33.1-0.1 arm64 [installed]
libffi-dev/oldoldstable,now 3.2.1-9 arm64 [installed]
libffi6/oldoldstable,now 3.2.1-9 arm64 [installed]
libfftw3-double3/oldoldstable,now 3.3.8-2 arm64 [installed,automatic]
libfftw3-single3/oldoldstable,now 3.3.8-2 arm64 [installed,automatic]
libfile-listing-perl/oldoldstable,oldoldstable,now 6.04-1 all [installed,automatic]
libflac8/now 1.3.2-3+deb10u1 arm64 [installed,upgradable to: 1.3.2-3+deb10u3]
libflite1/oldoldstable,now 2.1-release-3 arm64 [installed,automatic]
libfont-afm-perl/oldoldstable,oldoldstable,now 1.20-2 all [installed]
libfontconfig1-dev/oldoldstable,now 2.13.1-2 arm64 [installed,automatic]
libfontconfig1/oldoldstable,now 2.13.1-2 arm64 [installed]
libfontembed1/oldoldstable,now 1.21.6-5 arm64 [installed,upgradable to: 1.21.6-5+deb10u1]
libfontenc1/oldoldstable,now 1:1.1.3-1+b2 arm64 [installed]
libfreetype6-dev/oldoldstable,now 2.9.1-3+deb10u2 arm64 [installed,upgradable to: 2.9.1-3+deb10u3]
libfreetype6/oldoldstable,now 2.9.1-3+deb10u2 arm64 [installed,upgradable to: 2.9.1-3+deb10u3]
libfribidi0/oldoldstable,now 1.0.5-3.1+deb10u1 arm64 [installed,upgradable to: 1.0.5-3.1+deb10u2]
libfstrm0/oldoldstable,now 0.4.0-1 arm64 [installed,automatic]
libftdi1/oldoldstable,now 0.20-4 arm64 [installed,automatic]
libfuse2/oldoldstable,now 2.9.9-1+deb10u1 arm64 [installed]
libgail-common/oldoldstable,now 2.24.32-3 arm64 [installed]
libgail18/oldoldstable,now 2.24.32-3 arm64 [installed,automatic]
libgarcon-1-0/oldoldstable,now 0.6.2-1 arm64 [installed,automatic]
libgarcon-common/oldoldstable,oldoldstable,now 0.6.2-1 all [installed,automatic]
libgbm1/oldoldstable,now 18.3.6-2+deb10u1 arm64 [installed,automatic]
libgcc-8-dev/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libgcc1/oldoldstable,now 1:8.3.0-6 arm64 [installed]
libgck-1-0/oldoldstable,now 3.28.1-1 arm64 [installed,automatic]
libgcr-base-3-1/oldoldstable,now 3.28.1-1 arm64 [installed,automatic]
libgcrypt20/oldoldstable,now 1.8.4-5+deb10u1 arm64 [installed]
libgd3/oldoldstable,now 2.2.5-5.2 arm64 [installed,automatic]
libgdata-common/oldoldstable,oldoldstable,now 0.17.9-3 all [installed,automatic]
libgdata22/oldoldstable,now 0.17.9-3 arm64 [installed,automatic]
libgdbm-compat4/oldoldstable,now 1.18.1-4 arm64 [installed,automatic]
libgdbm6/oldoldstable,now 1.18.1-4 arm64 [installed,automatic]
libgdk-pixbuf2.0-0/oldoldstable,now 2.38.1+dfsg-1 arm64 [installed]
libgdk-pixbuf2.0-common/oldoldstable,oldoldstable,now 2.38.1+dfsg-1 all [installed]
libgeoip1/oldoldstable,now 1.6.12-1 arm64 [installed,automatic]
libgfortran5/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libgirepository-1.0-1/oldoldstable,now 1.58.3-2 arm64 [installed,automatic]
libgirepository1.0-dev/oldoldstable,now 1.58.3-2 arm64 [installed]
libgl1-mesa-dri/oldoldstable,now 18.3.6-2+deb10u1 arm64 [installed]
libgl1/oldoldstable,now 1.1.0-1 arm64 [installed,automatic]
libglade2-0/oldoldstable,now 1:2.6.4-2+b1 arm64 [installed,automatic]
libglapi-mesa/oldoldstable,now 18.3.6-2+deb10u1 arm64 [installed,automatic]
libglew2.1/oldoldstable,now 2.1.0-4 arm64 [installed,automatic]
libglib2.0-0/oldoldstable,now 2.58.3-2+deb10u3 arm64 [installed,upgradable to: 2.58.3-2+deb10u5]
libglib2.0-bin/oldoldstable,now 2.58.3-2+deb10u3 arm64 [installed,upgradable to: 2.58.3-2+deb10u5]
libglib2.0-data/oldoldstable,oldoldstable,now 2.58.3-2+deb10u3 all [installed,upgradable to: 2.58.3-2+deb10u5]
libglib2.0-dev-bin/oldoldstable,now 2.58.3-2+deb10u3 arm64 [installed,upgradable to: 2.58.3-2+deb10u5]
libglib2.0-dev/oldoldstable,now 2.58.3-2+deb10u3 arm64 [installed,upgradable to: 2.58.3-2+deb10u5]
libglibmm-2.4-1v5/oldoldstable,now 2.58.0-2 arm64 [installed,automatic]
libglu1-mesa/oldoldstable,now 9.0.0-2.1+b3 arm64 [installed,automatic]
libglvnd0/oldoldstable,now 1.1.0-1 arm64 [installed,automatic]
libglx-mesa0/oldoldstable,now 18.3.6-2+deb10u1 arm64 [installed,automatic]
libglx0/oldoldstable,now 1.1.0-1 arm64 [installed,automatic]
libgme0/oldoldstable,now 0.6.2-1 arm64 [installed,automatic]
libgmp10/oldoldstable,now 2:6.1.2+dfsg-4+deb10u1 arm64 [installed]
libgnome-desktop-3-17/oldoldstable,now 3.30.2.1-2 arm64 [installed,automatic]
libgnutls30/now 3.6.7-4+deb10u7 arm64 [installed,upgradable to: 3.6.7-4+deb10u10]
libgoa-1.0-0b/oldoldstable,now 3.30.1-2 arm64 [installed,automatic]
libgoa-1.0-common/oldoldstable,oldoldstable,now 3.30.1-2 all [installed,automatic]
libgomp1/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libgpg-error0/oldoldstable,now 1.35-1 arm64 [installed]
libgphoto2-6/oldoldstable,now 2.5.22-3 arm64 [installed,automatic]
libgphoto2-port12/oldoldstable,now 2.5.22-3 arm64 [installed,automatic]
libgpiod2/oldoldstable,now 1.2-3 arm64 [installed,automatic]
libgpm2/oldoldstable,now 1.20.7-5 arm64 [installed,automatic]
libgraphite2-3/oldoldstable,now 1.3.13-7 arm64 [installed]
libgs9-common/oldoldstable,oldoldstable,now 9.27~dfsg-2+deb10u5 all [installed,upgradable to: 9.27~dfsg-2+deb10u9]
libgs9/oldoldstable,now 9.27~dfsg-2+deb10u5 arm64 [installed,upgradable to: 9.27~dfsg-2+deb10u9]
libgsettings-qt1/oldoldstable,now 0.1+17.10.20170824-9 arm64 [installed]
libgsm1/oldoldstable,now 1.0.18-2 arm64 [installed,automatic]
libgspell-1-1/oldoldstable,now 1.6.1-2 arm64 [installed,automatic]
libgspell-1-common/oldoldstable,oldoldstable,now 1.6.1-2 all [installed,automatic]
libgssapi-krb5-2/now 1.17-3+deb10u3 arm64 [installed,upgradable to: 1.17-3+deb10u5]
libgstreamer-plugins-base1.0-0/oldoldstable,now 1.14.4-2+deb10u1 arm64 [installed,upgradable to: 1.14.4-2+deb10u2]
libgstreamer1.0-0/oldoldstable,now 1.14.4-1 arm64 [installed,automatic]
libgtk-3-0/oldoldstable,now 3.24.5-1 arm64 [installed,automatic]
libgtk-3-common/oldoldstable,oldoldstable,now 3.24.5-1 all [installed,automatic]
libgtk2.0-0/oldoldstable,now 2.24.32-3 arm64 [installed]
libgtk2.0-bin/oldoldstable,now 2.24.32-3 arm64 [installed]
libgtk2.0-common/oldoldstable,oldoldstable,now 2.24.32-3 all [installed]
libgtkmm-2.4-1v5/oldoldstable,now 1:2.24.5-4 arm64 [installed,automatic]
libgtkmm-3.0-1v5/oldoldstable,now 3.24.0-2 arm64 [installed,automatic]
libgtksourceview-3.0-1/oldoldstable,now 3.24.9-2 arm64 [installed,automatic]
libgtksourceview-3.0-common/oldoldstable,oldoldstable,now 3.24.9-2 all [installed,automatic]
libgudev-1.0-0/oldoldstable,now 232-2 arm64 [installed,automatic]
libgxps2/oldoldstable,now 0.3.1-1 arm64 [installed,automatic]
libharfbuzz0b/oldoldstable,now 2.3.1-1 arm64 [installed]
libhavege1/oldoldstable,now 1.9.1-7 arm64 [installed]
libheif1/oldoldstable,now 1.3.2-2~deb10u1 arm64 [installed,automatic]
libhidapi-libusb0/oldoldstable,now 0.8.0~rc1+git20140818.d17db57+dfsg-2 arm64 [installed,automatic]
libhogweed4/oldoldstable,oldoldstable,now 3.4.1-1+deb10u1 arm64 [installed]
libhpmud0/oldoldstable,now 3.18.12+dfsg0-2 arm64 [installed,automatic]
libhtml-parser-perl/oldoldstable,now 3.72-3+b3 arm64 [installed,automatic]
libhtml-tagset-perl/oldoldstable,oldoldstable,now 3.20-3 all [installed,automatic]
libhtml-tree-perl/oldoldstable,oldoldstable,now 5.07-2 all [installed,automatic]
libhttp-cookies-perl/oldoldstable,oldoldstable,now 6.04-1 all [installed,automatic]
libhttp-date-perl/oldoldstable,oldoldstable,now 6.02-1 all [installed,automatic]
libhttp-message-perl/oldoldstable,oldoldstable,now 6.18-1 all [installed,automatic]
libhttp-negotiate-perl/oldoldstable,oldoldstable,now 6.01-1 all [installed,automatic]
libhunspell-1.7-0/oldoldstable,now 1.7.0-2 arm64 [installed,automatic]
libhwloc-dev/oldoldstable,now 1.11.12-3 arm64 [installed,automatic]
libhwloc-plugins/oldoldstable,now 1.11.12-3 arm64 [installed,automatic]
libhwloc5/oldoldstable,now 1.11.12-3 arm64 [installed,automatic]
libi2c0/oldoldstable,now 4.1-1 arm64 [installed,automatic]
libibverbs-dev/oldoldstable,now 22.1-1 arm64 [installed,automatic]
libibverbs1/oldoldstable,now 22.1-1 arm64 [installed,automatic]
libical3/oldoldstable,now 3.0.4-3 arm64 [installed,automatic]
libice-dev/oldoldstable,now 2:1.0.9-2 arm64 [installed,automatic]
libice6/oldoldstable,now 2:1.0.9-2 arm64 [installed,automatic]
libicu-dev/oldoldstable,now 63.1-6+deb10u3 arm64 [installed,automatic]
libicu63/oldoldstable,now 63.1-6+deb10u3 arm64 [installed]
libidn11/oldoldstable,now 1.33-2.2 arm64 [installed]
libidn2-0/oldoldstable,oldoldstable,now 2.0.5-1+deb10u1 arm64 [installed]
libiec61883-0/oldoldstable,now 1.2.0-3 arm64 [installed,automatic]
libieee1284-3/oldoldstable,now 0.2.11-13 arm64 [installed,automatic]
libijs-0.35/oldoldstable,now 0.35-14 arm64 [installed,automatic]
libimagequant0/oldoldstable,now 2.12.2-1.1 arm64 [installed,automatic]
libimobiledevice6/oldoldstable,now 1.2.1~git20181030.92c5462-2+deb10u1 arm64 [installed,automatic]
libindicator3-7/oldoldstable,now 0.5.0-4 arm64 [installed,automatic]
libinput-bin/oldoldstable,now 1.12.6-2+deb10u1 arm64 [installed,automatic]
libinput10/oldoldstable,now 1.12.6-2+deb10u1 arm64 [installed,automatic]
libio-html-perl/oldoldstable,oldoldstable,now 1.001-1 all [installed,automatic]
libio-socket-ssl-perl/oldoldstable,oldoldstable,now 2.060-3 all [installed,automatic]
libip4tc0/oldoldstable,now 1.8.2-4 arm64 [installed]
libip6tc0/oldoldstable,now 1.8.2-4 arm64 [installed,automatic]
libiperf0/oldoldstable,now 3.6-2 arm64 [installed,upgradable to: 3.6-2+deb10u1]
libiptc0/oldoldstable,now 1.8.2-4 arm64 [installed,automatic]
libirs161/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libisc-export1100/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libisc1100/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libisccc161/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libisccfg163/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
libisl19/oldoldstable,now 0.20-2 arm64 [installed,automatic]
libitm1/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libiw30/oldoldstable,now 30~pre9-13 arm64 [installed,automatic]
libjack-jackd2-0/oldoldstable,now 1.9.12~dfsg-2 arm64 [installed,automatic]
libjansson4/oldoldstable,now 2.12-1 arm64 [installed,automatic]
libjbig0/oldoldstable,now 2.1-3.1+b2 arm64 [installed]
libjbig2dec0/oldoldstable,now 0.16-1+deb10u1 arm64 [installed,automatic]
libjim0.77/oldoldstable,now 0.77+dfsg0-3 arm64 [installed,automatic]
libjpeg-dev/oldoldstable,oldoldstable,now 1:1.5.2-2+deb10u1 all [installed]
libjpeg62-turbo-dev/oldoldstable,now 1:1.5.2-2+deb10u1 arm64 [installed,automatic]
libjpeg62-turbo/oldoldstable,now 1:1.5.2-2+deb10u1 arm64 [installed]
libjq1/oldoldstable,now 1.5+dfsg-2+b1 arm64 [installed,automatic]
libjs-jquery-ui/oldoldstable,oldoldstable,now 1.12.1+dfsg-5 all [installed,upgradable to: 1.12.1+dfsg-5+deb10u1]
libjs-jquery/oldoldstable,oldoldstable,now 3.3.1~dfsg-3+deb10u1 all [installed,automatic]
libjson-c3/oldoldstable,oldoldstable,now 0.12.1+ds-2+deb10u1 arm64 [installed]
libjson-glib-1.0-0/oldoldstable,now 1.4.4-2 arm64 [installed,automatic]
libjson-glib-1.0-common/oldoldstable,oldoldstable,now 1.4.4-2 all [installed,automatic]
libjsoncpp1/oldoldstable,now 1.7.4-3 arm64 [installed,automatic]
libk5crypto3/now 1.17-3+deb10u3 arm64 [installed,upgradable to: 1.17-3+deb10u5]
libkeybinder-3.0-0/oldoldstable,now 0.3.2-1 arm64 [installed,automatic]
libkeyutils1/oldoldstable,now 1.6-6 arm64 [installed]
libklibc/oldoldstable,now 2.0.6-1+deb10u1 arm64 [installed]
libkmod2/oldoldstable,now 26-1 arm64 [installed]
libkpathsea6/oldoldstable,now 2018.20181218.49446-1 arm64 [installed,upgradable to: 2018.20181218.49446-1+deb10u2]
libkrb5-3/now 1.17-3+deb10u3 arm64 [installed,upgradable to: 1.17-3+deb10u5]
libkrb5support0/now 1.17-3+deb10u3 arm64 [installed,upgradable to: 1.17-3+deb10u5]
libksba8/oldoldstable,now 1.3.5-2 arm64 [installed,upgradable to: 1.3.5-2+deb10u2]
liblcms2-2/oldoldstable,now 2.9-3 arm64 [installed,automatic]
libldap-2.4-2/oldoldstable,oldoldstable,now 2.4.47+dfsg-3+deb10u7 arm64 [installed]
libldap-common/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 2.4.47+dfsg-3+deb10u7 all [installed]
libldb1/oldoldstable,oldoldstable,now 2:1.5.1+really1.4.6-3+deb10u1 arm64 [installed,automatic]
liblightdm-gobject-1-0/oldoldstable,now 1.26.0-4 arm64 [installed,automatic]
liblilv-0-0/oldoldstable,now 0.24.2~dfsg0-2 arm64 [installed,automatic]
libllvm7/oldoldstable,now 1:7.0.1-8+deb10u2 arm64 [installed,automatic]
liblmdb-dev/oldoldstable,now 0.9.22-1 arm64 [installed]
liblmdb0/oldoldstable,now 0.9.22-1 arm64 [installed,automatic]
liblocale-gettext-perl/oldoldstable,now 1.07-3+b4 arm64 [installed]
liblognorm5/oldoldstable,now 2.0.5-1 arm64 [installed]
liblouis-data/oldoldstable,oldoldstable,now 3.8.0-2 all [installed,automatic]
liblouis17/oldoldstable,now 3.8.0-2 arm64 [installed,automatic]
liblqr-1-0/oldoldstable,now 0.4.2-2.1 arm64 [installed,automatic]
liblsan0/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libltdl-dev/oldoldstable,now 2.4.6-9 arm64 [installed,automatic]
libltdl7/oldoldstable,now 2.4.6-9 arm64 [installed,automatic]
liblwp-mediatypes-perl/oldoldstable,oldoldstable,now 6.02-1 all [installed,automatic]
liblwp-protocol-https-perl/oldoldstable,oldoldstable,now 6.07-2 all [installed,automatic]
liblwres161/oldoldstable,now 1:9.11.5.P4+dfsg-5.1+deb10u7 arm64 [installed,upgradable to: 1:9.11.5.P4+dfsg-5.1+deb10u9]
liblz4-1/oldoldstable,oldoldstable,now 1.8.3-1+deb10u1 arm64 [installed]
liblzma5/oldoldstable,oldoldstable,now 5.2.4-1+deb10u1 arm64 [installed]
liblzo2-2/oldoldstable,now 2.10-0.1 arm64 [installed,automatic]
libmagic-mgc/oldoldstable,now 1:5.35-4+deb10u2 arm64 [installed,automatic]
libmagic1/oldoldstable,now 1:5.35-4+deb10u2 arm64 [installed,automatic]
libmagickcore-6.q16-6/oldoldstable,now 8:6.9.10.23+dfsg-2.1+deb10u1 arm64 [installed,upgradable to: 8:6.9.10.23+dfsg-2.1+deb10u5]
libmagickwand-6.q16-6/oldoldstable,now 8:6.9.10.23+dfsg-2.1+deb10u1 arm64 [installed,upgradable to: 8:6.9.10.23+dfsg-2.1+deb10u5]
libmariadb3/oldoldstable,now 1:10.3.34-0+deb10u1 arm64 [installed,upgradable to: 1:10.3.39-0+deb10u1]
libmnl0/oldoldstable,now 1.0.4-2 arm64 [installed]
libmount-dev/oldoldstable,now 2.33.1-0.1 arm64 [installed,automatic]
libmount1/oldoldstable,now 2.33.1-0.1 arm64 [installed]
libmp3lame0/oldoldstable,now 3.100-2+b1 arm64 [installed,automatic]
libmpc3/oldoldstable,now 1.1.0-1 arm64 [installed,automatic]
libmpdec2/oldoldstable,now 2.4.2-2 arm64 [installed,automatic]
libmpfr6/oldoldstable,now 4.0.2-1 arm64 [installed,automatic]
libmpg123-0/oldoldstable,now 1.25.10-2 arm64 [installed,automatic]
libmtdev1/oldoldstable,now 1.1.5-1+b1 arm64 [installed,automatic]
libmtp-common/oldoldstable,oldoldstable,now 1.1.16-2 all [installed,automatic]
libmtp9/oldoldstable,now 1.1.16-2 arm64 [installed,automatic]
libmysofa0/oldoldstable,now 0.6~dfsg0-3+deb10u1 arm64 [installed,automatic]
libnautilus-extension1a/oldoldstable,now 3.30.5-2 arm64 [installed,automatic]
libncurses-dev/oldoldstable,now 6.1+20181013-2+deb10u2 arm64 [installed,upgradable to: 6.1+20181013-2+deb10u4]
libncurses6/oldoldstable,now 6.1+20181013-2+deb10u2 arm64 [installed,upgradable to: 6.1+20181013-2+deb10u4]
libncursesw6/oldoldstable,now 6.1+20181013-2+deb10u2 arm64 [installed,upgradable to: 6.1+20181013-2+deb10u4]
libnet-http-perl/oldoldstable,oldoldstable,now 6.18-1 all [installed,automatic]
libnet-ssleay-perl/now 1.85-2+b1 arm64 [installed,upgradable to: 1.85-2+deb10u1]
libnetfilter-conntrack3/oldoldstable,now 1.0.7-1 arm64 [installed,automatic]
libnettle6/oldoldstable,oldoldstable,now 3.4.1-1+deb10u1 arm64 [installed]
libnewlib-arm-none-eabi/oldoldstable,oldoldstable,now 3.1.0.20181231-1 all [installed]
libnewlib-dev/oldoldstable,oldoldstable,now 3.1.0.20181231-1 all [installed,automatic]
libnewt0.52/oldoldstable,now 0.52.20-8 arm64 [installed]
libnfnetlink0/oldoldstable,now 1.0.1-3+b1 arm64 [installed,automatic]
libnfs12/oldoldstable,now 3.0.0-2 arm64 [installed,automatic]
libnftnl11/oldoldstable,now 1.1.2-2 arm64 [installed,automatic]
libnghttp2-14/oldoldstable,oldoldstable,now 1.36.0-2+deb10u1 arm64 [installed,automatic]
libnginx-mod-http-auth-pam/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-dav-ext/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-echo/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-geoip/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-image-filter/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-subs-filter/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-upstream-fair/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-http-xslt-filter/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-mail/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnginx-mod-stream/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
libnl-3-200/oldoldstable,now 3.4.0-1 arm64 [installed,automatic]
libnl-3-dev/oldoldstable,now 3.4.0-1 arm64 [installed]
libnl-genl-3-200/oldoldstable,now 3.4.0-1 arm64 [installed,automatic]
libnl-genl-3-dev/oldoldstable,now 3.4.0-1 arm64 [installed]
libnl-route-3-200/oldoldstable,now 3.4.0-1 arm64 [installed,automatic]
libnl-route-3-dev/oldoldstable,now 3.4.0-1 arm64 [installed,automatic]
libnorm1/oldoldstable,now 1.5.8+dfsg2-1 arm64 [installed,automatic]
libnotify-bin/oldoldstable,now 0.7.7-4 arm64 [installed]
libnotify4/oldoldstable,now 0.7.7-4 arm64 [installed,automatic]
libnpth0/oldoldstable,now 1.6-1 arm64 [installed]
libnspr4/oldoldstable,now 2:4.20-1 arm64 [installed,automatic]
libnss-myhostname/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
libnss3/oldoldstable,now 2:3.42.1-1+deb10u5 arm64 [installed,upgradable to: 2:3.42.1-1+deb10u6]
libntfs-3g883/oldoldstable,now 1:2017.3.23AR.3-3+deb10u2 arm64 [installed,upgradable to: 1:2017.3.23AR.3-3+deb10u3]
libnuma-dev/oldoldstable,now 2.0.12-1 arm64 [installed,automatic]
libnuma1/oldoldstable,now 2.0.12-1 arm64 [installed,automatic]
liboauth0/oldoldstable,now 1.0.3-3 arm64 [installed,automatic]
libogg0/oldoldstable,now 1.3.2-1+b1 arm64 [installed,automatic]
libonig5/oldoldstable,now 6.9.1-1 arm64 [installed,automatic]
libopenal-data/oldoldstable,oldoldstable,now 1:1.19.1-1 all [installed,automatic]
libopenal1/oldoldstable,now 1:1.19.1-1 arm64 [installed,automatic]
libopenjp2-7/oldoldstable,oldoldstable,now 2.3.0-2+deb10u2 arm64 [installed]
libopenmpi-dev/oldoldstable,now 3.1.3-11 arm64 [installed,automatic]
libopenmpi3/oldoldstable,now 3.1.3-11 arm64 [installed,automatic]
libopenmpt0/oldoldstable,oldoldstable,now 0.4.3-1+deb10u1 arm64 [installed,automatic]
libopts25/oldoldstable,now 1:5.18.12-4 arm64 [installed,auto-removable]
libopus0/oldoldstable,now 1.3-1 arm64 [installed,automatic]
liborc-0.4-0/oldoldstable,now 1:0.4.28-3.1 arm64 [installed,automatic]
libp11-kit0/oldoldstable,oldoldstable,now 0.23.15-2+deb10u1 arm64 [installed]
libpackagekit-glib2-18/oldoldstable,now 1.1.12-5 arm64 [installed,automatic]
libpam-gnome-keyring/oldoldstable,now 3.28.2-5 arm64 [installed]
libpam-modules-bin/oldoldstable,now 1.3.1-5 arm64 [installed]
libpam-modules/oldoldstable,now 1.3.1-5 arm64 [installed]
libpam-runtime/oldoldstable,oldoldstable,now 1.3.1-5 all [installed]
libpam-systemd/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
libpam0g/oldoldstable,now 1.3.1-5 arm64 [installed]
libpango-1.0-0/oldoldstable,now 1.42.4-8~deb10u1 arm64 [installed]
libpangocairo-1.0-0/oldoldstable,now 1.42.4-8~deb10u1 arm64 [installed]
libpangoft2-1.0-0/oldoldstable,now 1.42.4-8~deb10u1 arm64 [installed]
libpangomm-1.4-1v5/oldoldstable,now 2.42.0-2 arm64 [installed,automatic]
libpangoxft-1.0-0/oldoldstable,now 1.42.4-8~deb10u1 arm64 [installed,automatic]
libpaper1/oldoldstable,now 1.1.28 arm64 [installed,automatic]
libparted-fs-resize0/oldoldstable,now 3.2-25 arm64 [installed,automatic]
libparted2/oldoldstable,now 3.2-25 arm64 [installed,automatic]
libpcap0.8/oldoldstable,now 1.8.1-6+deb10u1 arm64 [installed,automatic]
libpci3/oldoldstable,now 1:3.5.2-1 arm64 [installed,automatic]
libpciaccess0/oldoldstable,now 0.14-1 arm64 [installed,automatic]
libpcre16-3/oldoldstable,now 2:8.39-12 arm64 [installed,automatic]
libpcre2-16-0/oldoldstable,now 10.32-5 arm64 [installed,upgradable to: 10.32-5+deb10u1]
libpcre2-8-0/oldoldstable,now 10.32-5 arm64 [installed,upgradable to: 10.32-5+deb10u1]
libpcre3-dev/oldoldstable,now 2:8.39-12 arm64 [installed,automatic]
libpcre32-3/oldoldstable,now 2:8.39-12 arm64 [installed,automatic]
libpcre3/oldoldstable,now 2:8.39-12 arm64 [installed]
libpcrecpp0v5/oldoldstable,now 2:8.39-12 arm64 [installed,automatic]
libpcsclite1/oldoldstable,now 1.8.24-1 arm64 [installed,automatic]
libperl5.28/oldoldstable,now 5.28.1-6+deb10u1 arm64 [installed,automatic]
libpgm-5.2-0/oldoldstable,now 5.2.122~dfsg-3 arm64 [installed,automatic]
libpipeline1/oldoldstable,now 1.5.1-2 arm64 [installed,automatic]
libpixman-1-0/oldoldstable,now 0.36.0-1 arm64 [installed,upgradable to: 0.36.0-1+deb10u1]
libpixman-1-dev/oldoldstable,now 0.36.0-1 arm64 [installed,upgradable to: 0.36.0-1+deb10u1]
libplist3/oldoldstable,now 2.0.1~git20190104.3f96731-1 arm64 [installed,automatic]
libpmix2/oldoldstable,now 3.1.2-3 arm64 [installed,automatic]
libpng-dev/oldoldstable,now 1.6.36-6 arm64 [installed,automatic]
libpng16-16/oldoldstable,now 1.6.36-6 arm64 [installed]
libpolkit-agent-1-0/oldoldstable,oldoldstable,now 0.105-25+deb10u1 arm64 [installed,automatic]
libpolkit-backend-1-0/oldoldstable,oldoldstable,now 0.105-25+deb10u1 arm64 [installed,automatic]
libpolkit-gobject-1-0/oldoldstable,oldoldstable,now 0.105-25+deb10u1 arm64 [installed,automatic]
libpoppler-glib8/oldoldstable,now 0.71.0-5 arm64 [installed,upgradable to: 0.71.0-5+deb10u2]
libpoppler82/oldoldstable,now 0.71.0-5 arm64 [installed,upgradable to: 0.71.0-5+deb10u2]
libpopt0/oldoldstable,now 1.16-12 arm64 [installed]
libpostproc55/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libproc-processtable-perl/oldoldstable,now 0.56-1 arm64 [installed]
libprocps7/oldoldstable,now 2:3.3.15-2 arm64 [installed,automatic]
libprotobuf-c1/oldoldstable,now 1.3.1-1+b1 arm64 [installed,automatic]
libproxy1-plugin-gsettings/oldoldstable,oldoldstable,now 0.4.15-5+deb10u1 arm64 [installed]
libproxy1-plugin-networkmanager/oldoldstable,oldoldstable,now 0.4.15-5+deb10u1 arm64 [installed]
libproxy1v5/oldoldstable,oldoldstable,now 0.4.15-5+deb10u1 arm64 [installed,automatic]
libpsl5/oldoldstable,now 0.20.2-2 arm64 [installed,automatic]
libpthread-stubs0-dev/oldoldstable,now 0.4-1 arm64 [installed,automatic]
libpulse-mainloop-glib0/oldoldstable,now 12.2-4+deb10u1 arm64 [installed,automatic]
libpulse0/oldoldstable,now 12.2-4+deb10u1 arm64 [installed,automatic]
libpulsedsp/oldoldstable,now 12.2-4+deb10u1 arm64 [installed,automatic]
libpython-dev/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
libpython-stdlib/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
libpython2-dev/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
libpython2-stdlib/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
libpython2.7-dev/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
libpython2.7-minimal/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
libpython2.7-stdlib/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
libpython2.7/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
libpython3-dev/oldoldstable,now 3.7.3-1 arm64 [installed,automatic]
libpython3-stdlib/oldoldstable,now 3.7.3-1 arm64 [installed,automatic]
libpython3.7-dev/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
libpython3.7-minimal/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
libpython3.7-stdlib/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
libpython3.7/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
libqpdf21/oldoldstable,now 8.4.0-2 arm64 [installed,upgradable to: 8.4.0-2+deb10u1]
libqrencode4/oldoldstable,now 4.0.2-1 arm64 [installed,automatic]
libqt5core5a/now 5.11.3+dfsg1-1+deb10u4 arm64 [installed,upgradable to: 5.11.3+dfsg1-1+deb10u5]
libqt5dbus5/now 5.11.3+dfsg1-1+deb10u4 arm64 [installed,upgradable to: 5.11.3+dfsg1-1+deb10u5]
libqt5gui5/now 5.11.3+dfsg1-1+deb10u4 arm64 [installed,upgradable to: 5.11.3+dfsg1-1+deb10u5]
libqt5network5/now 5.11.3+dfsg1-1+deb10u4 arm64 [installed,upgradable to: 5.11.3+dfsg1-1+deb10u5]
libqt5widgets5/now 5.11.3+dfsg1-1+deb10u4 arm64 [installed,upgradable to: 5.11.3+dfsg1-1+deb10u5]
libraw1394-11/oldoldstable,now 2.1.2-1+b1 arm64 [installed,automatic]
libreadline7/oldoldstable,now 7.0-5 arm64 [installed]
librest-0.7-0/oldoldstable,now 0.8.1-1 arm64 [installed,automatic]
librhash0/oldoldstable,now 1.3.8-1 arm64 [installed,automatic]
librsvg2-2/now 2.44.10-2.1 arm64 [installed,upgradable to: 2.44.10-2.1+deb10u3]
librsvg2-common/now 2.44.10-2.1 arm64 [installed,upgradable to: 2.44.10-2.1+deb10u3]
librtmp1/oldoldstable,now 2.4+20151223.gitfa8646d.1-2 arm64 [installed,automatic]
librubberband2/oldoldstable,now 1.8.1-7 arm64 [installed,automatic]
libsamplerate0/oldoldstable,now 0.1.9-2 arm64 [installed,automatic]
libsane-common/oldoldstable,oldoldstable,now 1.0.27-3.2 all [installed,automatic]
libsane-hpaio/oldoldstable,now 3.18.12+dfsg0-2 arm64 [installed,automatic]
libsane/oldoldstable,now 1.0.27-3.2 arm64 [installed,automatic]
libsasl2-2/oldoldstable,oldoldstable,now 2.1.27+dfsg-1+deb10u2 arm64 [installed]
libsasl2-modules-db/oldoldstable,oldoldstable,now 2.1.27+dfsg-1+deb10u2 arm64 [installed]
libsbc1/oldoldstable,now 1.4-1 arm64 [installed,automatic]
libsctp1/oldoldstable,now 1.0.18+dfsg-1 arm64 [installed,automatic]
libsdl2-2.0-0/oldoldstable,now 2.0.9+dfsg1-1 arm64 [installed,upgradable to: 2.0.9+dfsg1-1+deb10u1]
libseccomp2/oldoldstable,now 2.3.3-4 arm64 [installed]
libsecret-1-0/oldoldstable,now 0.18.7-1 arm64 [installed,automatic]
libsecret-common/oldoldstable,oldoldstable,now 0.18.7-1 all [installed,automatic]
libselinux1-dev/oldoldstable,now 2.8-1+b1 arm64 [installed,automatic]
libselinux1/oldoldstable,now 2.8-1+b1 arm64 [installed]
libsemanage-common/oldoldstable,oldoldstable,now 2.8-2 all [installed]
libsemanage1/oldoldstable,now 2.8-2 arm64 [installed]
libsensors-config/oldoldstable,oldoldstable,now 1:3.5.0-3 all [installed,automatic]
libsensors5/oldoldstable,now 1:3.5.0-3 arm64 [installed,automatic]
libsepol1-dev/oldoldstable,now 2.8-1 arm64 [installed,automatic]
libsepol1/oldoldstable,now 2.8-1 arm64 [installed]
libserd-0-0/oldoldstable,now 0.28.0~dfsg0-1 arm64 [installed,automatic]
libshine3/oldoldstable,now 3.1.1-2 arm64 [installed,automatic]
libsigc++-2.0-0v5/oldoldstable,now 2.10.1-2 arm64 [installed,automatic]
libsigsegv2/oldoldstable,now 2.12-2 arm64 [installed,automatic]
libslang2/oldoldstable,now 2.3.2-2 arm64 [installed]
libsm-dev/oldoldstable,now 2:1.2.3-1 arm64 [installed,automatic]
libsm6/oldoldstable,now 2:1.2.3-1 arm64 [installed,automatic]
libsmartcols1/oldoldstable,now 2.33.1-0.1 arm64 [installed]
libsmbclient/oldoldstable,now 2:4.9.5+dfsg-5+deb10u3 arm64 [installed,upgradable to: 2:4.9.5+dfsg-5+deb10u4]
libsnappy1v5/oldoldstable,now 1.1.7-1 arm64 [installed,automatic]
libsndfile1/oldoldstable,now 1.0.28-6+deb10u1 arm64 [installed,upgradable to: 1.0.28-6+deb10u2]
libsndio7.0/oldoldstable,now 1.5.0-3 arm64 [installed,automatic]
libsnmp-base/oldoldstable,oldoldstable,now 5.7.3+dfsg-5+deb10u2 all [installed,upgradable to: 5.7.3+dfsg-5+deb10u4]
libsnmp30/oldoldstable,now 5.7.3+dfsg-5+deb10u2 arm64 [installed,upgradable to: 5.7.3+dfsg-5+deb10u4]
libsodium-dev/oldoldstable,now 1.0.17-1 arm64 [installed]
libsodium23/oldoldstable,now 1.0.17-1 arm64 [installed,automatic]
libsord-0-0/oldoldstable,now 0.16.0~dfsg0-1+b1 arm64 [installed,automatic]
libsoup-gnome2.4-1/oldoldstable,now 2.64.2-2 arm64 [installed,automatic]
libsoup2.4-1/oldoldstable,now 2.64.2-2 arm64 [installed,automatic]
libsoxr0/oldoldstable,now 0.1.2-3 arm64 [installed,automatic]
libspectre1/oldoldstable,now 0.2.8-1 arm64 [installed,automatic]
libspeechd2/oldoldstable,now 0.9.0-5+deb10u1 arm64 [installed,automatic]
libspeex1/oldoldstable,now 1.2~rc1.2-1+b2 arm64 [installed,automatic]
libspeexdsp1/oldoldstable,now 1.2~rc1.2-1+b2 arm64 [installed,automatic]
libsqlite3-0/oldoldstable,now 3.27.2-3+deb10u1 arm64 [installed,upgradable to: 3.27.2-3+deb10u2]
libsratom-0-0/oldoldstable,now 0.6.0~dfsg0-1 arm64 [installed,automatic]
libss2/oldoldstable,now 1.44.5-1+deb10u3 arm64 [installed]
libssh-gcrypt-4/oldoldstable,now 0.8.7-1+deb10u1 arm64 [installed,upgradable to: 0.8.7-1+deb10u2]
libssh2-1/oldoldstable,now 1.8.0-2.1 arm64 [installed,upgradable to: 1.8.0-2.1+deb10u1]
libssl-dev/oldoldstable,now 1.1.1n-0+deb10u3 arm64 [installed,upgradable to: 1.1.1n-0+deb10u6]
libssl1.1/oldoldstable,now 1.1.1n-0+deb10u3 arm64 [installed,upgradable to: 1.1.1n-0+deb10u6]
libstartup-notification0/oldoldstable,now 0.12-6 arm64 [installed,automatic]
libstdc++-8-dev/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libstdc++6/oldoldstable,now 8.3.0-6 arm64 [installed]
libstemmer0d/oldoldstable,now 0+svn585-1+b2 arm64 [installed,automatic]
libswresample3/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libswscale5/oldoldstable,now 7:4.1.9-0+deb10u1 arm64 [installed,upgradable to: 7:4.1.11-0+deb10u1]
libsynctex2/oldoldstable,now 2018.20181218.49446-1 arm64 [installed,upgradable to: 2018.20181218.49446-1+deb10u2]
libsysfs2/oldoldstable,now 2.1.0+repack-5 arm64 [installed,automatic]
libsystemd0/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
libtalloc2/oldoldstable,now 2.1.14-2 arm64 [installed,automatic]
libtasn1-6/oldoldstable,now 4.13-3 arm64 [installed,upgradable to: 4.13-3+deb10u1]
libtcl8.6/oldoldstable,now 8.6.9+dfsg-2 arm64 [installed,automatic]
libtdb1/oldoldstable,now 1.3.16-2+b1 arm64 [installed,automatic]
libtevent0/oldoldstable,now 0.9.37-1 arm64 [installed,automatic]
libtext-iconv-perl/oldoldstable,now 1.7-5+b6 arm64 [installed,automatic]
libthai-data/oldoldstable,oldoldstable,now 0.1.28-2 all [installed]
libthai0/oldoldstable,now 0.1.28-2 arm64 [installed]
libtheora0/oldoldstable,now 1.1.1+dfsg.1-15 arm64 [installed,automatic]
libthunarx-3-0/oldoldstable,now 1.8.4-1 arm64 [installed,automatic]
libtiff5/oldoldstable,now 4.1.0+git191117-2~deb10u4 arm64 [installed,upgradable to: 4.1.0+git191117-2~deb10u8]
libtimedate-perl/oldoldstable,oldoldstable,now 2.3000-2+deb10u1 all [installed,automatic]
libtinfo6/oldoldstable,now 6.1+20181013-2+deb10u2 arm64 [installed,upgradable to: 6.1+20181013-2+deb10u4]
libtry-tiny-perl/oldoldstable,oldoldstable,now 0.30-1 all [installed,automatic]
libtsan0/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libtwolame0/oldoldstable,now 0.3.13-4 arm64 [installed,automatic]
libu2f-udev/oldoldstable,oldoldstable,now 1.1.9-1 all [installed]
libubsan1/oldoldstable,now 8.3.0-6 arm64 [installed,automatic]
libuchardet0/oldoldstable,now 0.0.6-3 arm64 [installed,automatic]
libudev1/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
libudisks2-0/oldoldstable,now 2.8.1-4 arm64 [installed,upgradable to: 2.8.1-4+deb10u2]
libunistring2/oldoldstable,now 0.9.10-1 arm64 [installed]
libunwind8/oldoldstable,now 1.2.1-10~deb10u1 arm64 [installed,automatic]
libupower-glib3/oldoldstable,now 0.99.10-1 arm64 [installed,automatic]
liburi-perl/oldoldstable,oldoldstable,now 1.76-1 all [installed,automatic]
libusb-0.1-4/oldoldstable,now 2:0.1.12-32 arm64 [installed,automatic]
libusb-1.0-0-dev/oldoldstable,now 2:1.0.22-2 arm64 [installed]
libusb-1.0-0/oldoldstable,now 2:1.0.22-2 arm64 [installed]
libusb-1.0-doc/oldoldstable,oldoldstable,now 2:1.0.22-2 all [installed]
libusb-dev/oldoldstable,now 2:0.1.12-32 arm64 [installed]
libusbmuxd4/oldoldstable,now 1.1.0~git20181007.07a493a-1 arm64 [installed,automatic]
libutempter0/oldoldstable,now 1.1.6-3 arm64 [installed,automatic]
libuuid-perl/oldoldstable,now 0.28-1 arm64 [installed,automatic]
libuuid1/oldoldstable,now 2.33.1-0.1 arm64 [installed]
libuv1/oldoldstable,oldoldstable,now 1.24.1-1+deb10u1 arm64 [installed,automatic]
libv4l-0/oldoldstable,now 1.16.3-3 arm64 [installed,automatic]
libv4l-dev/oldoldstable,now 1.16.3-3 arm64 [installed]
libv4l2rds0/oldoldstable,now 1.16.3-3 arm64 [installed,automatic]
libv4lconvert0/oldoldstable,now 1.16.3-3 arm64 [installed,automatic]
libva-drm2/oldoldstable,now 2.4.0-1 arm64 [installed,automatic]
libva-x11-2/oldoldstable,now 2.4.0-1 arm64 [installed,automatic]
libva2/oldoldstable,now 2.4.0-1 arm64 [installed,automatic]
libvdpau1/oldoldstable,now 1.1.1-10 arm64 [installed,automatic]
libvidstab1.1/oldoldstable,now 1.1.0-2 arm64 [installed,automatic]
libvisual-0.4-0/oldoldstable,now 0.4.0-15 arm64 [installed,automatic]
libvorbis0a/oldoldstable,now 1.3.6-2 arm64 [installed,automatic]
libvorbisenc2/oldoldstable,now 1.3.6-2 arm64 [installed,automatic]
libvorbisfile3/oldoldstable,now 1.3.6-2 arm64 [installed,automatic]
libvpx5/oldoldstable,now 1.7.0-3+deb10u1 arm64 [installed,upgradable to: 1.7.0-3+deb10u2]
libvte-2.91-0/oldoldstable,now 0.54.2-2 arm64 [installed,automatic]
libvte-2.91-common/oldoldstable,oldoldstable,now 0.54.2-2 all [installed,automatic]
libwacom-common/oldoldstable,oldoldstable,now 0.32-1 all [installed,automatic]
libwacom2/oldoldstable,now 0.32-1 arm64 [installed,automatic]
libwavpack1/oldoldstable,now 5.1.0-6+deb10u1 arm64 [installed,automatic]
libwayland-client0/oldoldstable,now 1.16.0-1 arm64 [installed,automatic]
libwayland-cursor0/oldoldstable,now 1.16.0-1 arm64 [installed,automatic]
libwayland-egl1/oldoldstable,now 1.16.0-1 arm64 [installed,automatic]
libwayland-server0/oldoldstable,now 1.16.0-1 arm64 [installed,automatic]
libwbclient0/oldoldstable,now 2:4.9.5+dfsg-5+deb10u3 arm64 [installed,upgradable to: 2:4.9.5+dfsg-5+deb10u4]
libwebp6/oldoldstable,now 0.6.1-2+deb10u1 arm64 [installed,upgradable to: 0.6.1-2+deb10u3]
libwebpdemux2/oldoldstable,now 0.6.1-2+deb10u1 arm64 [installed,upgradable to: 0.6.1-2+deb10u3]
libwebpmux3/oldoldstable,now 0.6.1-2+deb10u1 arm64 [installed,upgradable to: 0.6.1-2+deb10u3]
libwebrtc-audio-processing1/oldoldstable,now 0.3-1 arm64 [installed,automatic]
libwebsocketpp-dev/oldoldstable,now 0.8.1-1 arm64 [installed]
libwebsocketpp-doc/oldoldstable,oldoldstable,now 0.8.1-1 all [installed]
libwmf0.2-7-gtk/oldoldstable,now 0.2.8.4-14 arm64 [installed]
libwmf0.2-7/oldoldstable,now 0.2.8.4-14 arm64 [installed,automatic]
libwnck-3-0/oldoldstable,now 3.30.0-2 arm64 [installed,automatic]
libwnck-3-common/oldoldstable,oldoldstable,now 3.30.0-2 all [installed,automatic]
libwnck-common/oldoldstable,oldoldstable,now 2.30.7-6 all [installed,automatic]
libwnck22/oldoldstable,now 2.30.7-6 arm64 [installed,automatic]
libwrap0-dev/oldoldstable,now 7.6.q-28 arm64 [installed]
libwrap0/oldoldstable,now 7.6.q-28 arm64 [installed,automatic]
libwww-perl/oldoldstable,oldoldstable,now 6.36-2 all [installed,automatic]
libwww-robotrules-perl/oldoldstable,oldoldstable,now 6.02-1 all [installed,automatic]
libx11-6/oldoldstable,now 2:1.6.7-1+deb10u2 arm64 [installed,upgradable to: 2:1.6.7-1+deb10u3]
libx11-data/oldoldstable,oldoldstable,now 2:1.6.7-1+deb10u2 all [installed,upgradable to: 2:1.6.7-1+deb10u3]
libx11-dev/oldoldstable,now 2:1.6.7-1+deb10u2 arm64 [installed,upgradable to: 2:1.6.7-1+deb10u3]
libx11-xcb1/oldoldstable,now 2:1.6.7-1+deb10u2 arm64 [installed,upgradable to: 2:1.6.7-1+deb10u3]
libx264-155/oldoldstable,now 2:0.155.2917+git0a84d98-2 arm64 [installed,automatic]
libx265-165/oldoldstable,now 2.9-4 arm64 [installed,automatic]
libxapian30/oldoldstable,now 1.4.11-1 arm64 [installed,upgradable to: 1.4.11-1+deb10u1]
libxau-dev/oldoldstable,now 1:1.0.8-1+b2 arm64 [installed,automatic]
libxau6/oldoldstable,now 1:1.0.8-1+b2 arm64 [installed]
libxaw7/oldoldstable,now 2:1.0.13-1+b2 arm64 [installed,automatic]
libxcb-dri2-0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-dri3-0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-glx0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-icccm4/oldoldstable,now 0.4.1-1.1 arm64 [installed,automatic]
libxcb-image0/oldoldstable,now 0.4.0-1+b2 arm64 [installed,automatic]
libxcb-keysyms1/oldoldstable,now 0.4.0-1+b2 arm64 [installed,automatic]
libxcb-present0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-randr0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-render-util0/oldoldstable,now 0.3.9-1+b1 arm64 [installed,automatic]
libxcb-render0-dev/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-render0/oldoldstable,now 1.13.1-2 arm64 [installed]
libxcb-shape0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-shm0-dev/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-shm0/oldoldstable,now 1.13.1-2 arm64 [installed]
libxcb-sync1/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-util0/oldoldstable,now 0.3.8-3+b2 arm64 [installed,automatic]
libxcb-xfixes0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-xinerama0/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb-xkb1/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb1-dev/oldoldstable,now 1.13.1-2 arm64 [installed,automatic]
libxcb1/oldoldstable,now 1.13.1-2 arm64 [installed]
libxcomposite1/oldoldstable,now 1:0.4.4-2 arm64 [installed]
libxcursor1/oldoldstable,now 1:1.1.15-2 arm64 [installed]
libxdamage1/oldoldstable,now 1:1.1.4-3+b3 arm64 [installed]
libxdmcp-dev/oldoldstable,now 1:1.1.2-3 arm64 [installed,automatic]
libxdmcp6/oldoldstable,now 1:1.1.2-3 arm64 [installed]
libxdo3/oldoldstable,now 1:3.20160805.1-4 arm64 [installed,automatic]
libxext-dev/oldoldstable,now 2:1.3.3-1+b2 arm64 [installed,automatic]
libxext6/oldoldstable,now 2:1.3.3-1+b2 arm64 [installed]
libxfce4panel-2.0-4/oldoldstable,now 4.12.2-1 arm64 [installed,automatic]
libxfce4ui-1-0/oldoldstable,now 4.12.1-3 arm64 [installed,automatic]
libxfce4ui-2-0/oldoldstable,now 4.12.1-3 arm64 [installed,automatic]
libxfce4ui-common/oldoldstable,oldoldstable,now 4.12.1-3 all [installed,automatic]
libxfce4ui-utils/oldoldstable,now 4.12.1-3 arm64 [installed,automatic]
libxfce4util-common/oldoldstable,oldoldstable,now 4.12.1-3 all [installed,automatic]
libxfce4util7/oldoldstable,now 4.12.1-3 arm64 [installed,automatic]
libxfconf-0-2/oldoldstable,now 4.12.1-1 arm64 [installed,automatic]
libxfixes3/oldoldstable,now 1:5.0.3-1 arm64 [installed]
libxfont2/oldoldstable,now 1:2.0.3-1 arm64 [installed,automatic]
libxft2/oldoldstable,now 2.3.2-2 arm64 [installed,automatic]
libxi6/oldoldstable,now 2:1.7.9-1 arm64 [installed]
libxinerama1/oldoldstable,now 2:1.1.4-2 arm64 [installed]
libxkbcommon-x11-0/oldoldstable,now 0.8.2-1 arm64 [installed,automatic]
libxkbcommon0/oldoldstable,now 0.8.2-1 arm64 [installed,automatic]
libxkbfile1/oldoldstable,now 1:1.0.9-2+b11 arm64 [installed,automatic]
libxklavier16/oldoldstable,now 5.4-4 arm64 [installed,automatic]
libxml2/oldoldstable,now 2.9.4+dfsg1-7+deb10u4 arm64 [installed,upgradable to: 2.9.4+dfsg1-7+deb10u6]
libxmu6/oldoldstable,now 2:1.1.2-2+b3 arm64 [installed,automatic]
libxmuu1/oldoldstable,now 2:1.1.2-2+b3 arm64 [installed,automatic]
libxpm4/oldoldstable,now 1:3.5.12-1 arm64 [installed,upgradable to: 1:3.5.12-1+deb10u1]
libxrandr2/oldoldstable,now 2:1.5.1-1 arm64 [installed]
libxrender-dev/oldoldstable,now 1:0.9.10-1 arm64 [installed,automatic]
libxrender1/oldoldstable,now 1:0.9.10-1 arm64 [installed]
libxres1/oldoldstable,now 2:1.2.0-2 arm64 [installed,automatic]
libxshmfence1/oldoldstable,now 1.3-1 arm64 [installed,automatic]
libxslt1.1/oldoldstable,now 1.1.32-2.2~deb10u1 arm64 [installed,upgradable to: 1.1.32-2.2~deb10u2]
libxss1/oldoldstable,now 1:1.2.3-1 arm64 [installed,automatic]
libxt6/oldoldstable,now 1:1.1.5-1+b3 arm64 [installed,automatic]
libxtables12/oldoldstable,now 1.8.2-4 arm64 [installed]
libxtst6/oldoldstable,now 2:1.2.3-1 arm64 [installed,automatic]
libxv1/oldoldstable,now 2:1.0.11-1 arm64 [installed,automatic]
libxvidcore4/oldoldstable,now 2:1.3.5-1 arm64 [installed,automatic]
libxxf86dga1/oldoldstable,now 2:1.1.4-1+b3 arm64 [installed,automatic]
libxxf86vm1/oldoldstable,now 1:1.1.4-1+b2 arm64 [installed,automatic]
libyaml-0-2/oldoldstable,now 0.2.1-1 arm64 [installed,automatic]
libyaml-tiny-perl/oldoldstable,oldoldstable,now 1.73-1 all [installed,automatic]
libzmq5/oldoldstable,oldoldstable,now 4.3.1-4+deb10u2 arm64 [installed,automatic]
libzstd1/oldoldstable,oldoldstable,now 1.3.8+dfsg-3+deb10u2 arm64 [installed]
libzvbi-common/oldoldstable,oldoldstable,now 0.2.35-16 all [installed,automatic]
libzvbi0/oldoldstable,now 0.2.35-16 arm64 [installed,automatic]
lightdm/oldoldstable,now 1.26.0-4 arm64 [installed]
linux-base/oldoldstable,oldoldstable,now 4.6 all [installed]
linux-dtb-edge-rockchip64/now 22.05.0-trunk arm64 [installed,upgradable to: 23.02.2]
linux-image-edge-rockchip64/now 22.05.0-trunk arm64 [installed,upgradable to: 23.02.2]
linux-libc-dev/buster,now 22.05.3 arm64 [installed,upgradable to: 23.02.2]
linux-u-boot-mkspi-edge/now 22.05.0-trunk arm64 [installed,local]
locales/oldoldstable,oldoldstable,now 2.28-10+deb10u1 all [installed,upgradable to: 2.28-10+deb10u2]
login/oldoldstable,now 1:4.5-1.1 arm64 [installed]
logrotate/oldoldstable,now 3.14.0-4 arm64 [installed]
lsb-base/oldoldstable,oldoldstable,now 10.2019051400 all [installed]
lsb-release/oldoldstable,oldoldstable,now 10.2019051400 all [installed,automatic]
lsof/oldoldstable,now 4.91+dfsg-1 arm64 [installed]
lxtask/oldoldstable,now 0.1.9-1 arm64 [installed]
m4/oldoldstable,now 1.4.18-2 arm64 [installed,automatic]
make/oldoldstable,now 4.2.1-1.2 arm64 [installed,automatic]
makerbase-client/now 0.1.1 arm64 [installed,local]
man-db/oldoldstable,now 2.8.5-2 arm64 [installed,automatic]
mariadb-common/oldoldstable,oldoldstable,now 1:10.3.34-0+deb10u1 all [installed,upgradable to: 1:10.3.39-0+deb10u1]
matchbox-keyboard/oldoldstable,now 0.1+svn20080916-12 arm64 [installed]
mawk/oldoldstable,now 1.3.3-17+b3 arm64 [installed]
mc-data/oldoldstable,oldoldstable,now 3:4.8.22-1 all [installed,automatic]
mc/oldoldstable,now 3:4.8.22-1 arm64 [installed]
mesa-utils/oldoldstable,now 8.4.0-1+b1 arm64 [installed]
mime-support/oldoldstable,oldoldstable,now 3.62 all [installed,automatic]
mmc-utils/oldoldstable,now 0+git20180327.b4fe0c8c-1 arm64 [installed]
mount/oldoldstable,now 2.33.1-0.1 arm64 [installed]
mousepad/oldoldstable,now 0.4.1-2 arm64 [installed]
mousetweaks/oldoldstable,now 3.12.0-5 arm64 [installed]
mpi-default-bin/oldoldstable,now 1.13 arm64 [installed,automatic]
mpi-default-dev/oldoldstable,now 1.13 arm64 [installed,automatic]
mysql-common/oldoldstable,oldoldstable,now 5.8+1.0.5 all [installed,automatic]
nano/oldoldstable,now 3.2-3 arm64 [installed]
ncurses-base/oldoldstable,oldoldstable,now 6.1+20181013-2+deb10u2 all [installed,upgradable to: 6.1+20181013-2+deb10u4]
ncurses-bin/oldoldstable,now 6.1+20181013-2+deb10u2 arm64 [installed,upgradable to: 6.1+20181013-2+deb10u4]
ncurses-term/oldoldstable,oldoldstable,now 6.1+20181013-2+deb10u2 all [installed,upgradable to: 6.1+20181013-2+deb10u4]
net-tools/oldoldstable,now 1.60+git20180626.aebd88e-1 arm64 [installed]
netbase/oldoldstable,oldoldstable,now 5.6 all [installed]
netcat-openbsd/oldoldstable,now 1.195-2 arm64 [installed]
netplan.io/oldoldstable,now 0.95-2 arm64 [installed]
nginx-common/oldoldstable,oldoldstable,now 1.14.2-2+deb10u4 all [installed,upgradable to: 1.14.2-2+deb10u5]
nginx-full/oldoldstable,now 1.14.2-2+deb10u4 arm64 [installed,upgradable to: 1.14.2-2+deb10u5]
nginx/oldoldstable,oldoldstable,now 1.14.2-2+deb10u4 all [installed,upgradable to: 1.14.2-2+deb10u5]
nlohmann-json3-dev/oldoldstable,oldoldstable,now 3.5.0-0.1 all [installed]
nocache/oldoldstable,now 1.1-1 arm64 [installed]
ntfs-3g/oldoldstable,now 1:2017.3.23AR.3-3+deb10u2 arm64 [installed,upgradable to: 1:2017.3.23AR.3-3+deb10u3]
numix-gtk-theme/buster,buster,buster,now 2.6.7-6 all [installed]
numix-icon-theme-circle/oldoldstable,oldoldstable,now 19.02.07-1 all [installed,upgradable to: 19.12.27+202303050246~ubuntu20.04.1]
numix-icon-theme/oldoldstable,oldoldstable,now 0~20180717-1 all [installed]
ocl-icd-libopencl1/oldoldstable,now 2.2.12-2 arm64 [installed,automatic]
openmpi-bin/oldoldstable,now 3.1.3-11 arm64 [installed,automatic]
openmpi-common/oldoldstable,oldoldstable,now 3.1.3-11 all [installed,automatic]
openprinting-ppds/oldoldstable,oldoldstable,now 20181217-2 all [installed]
openssh-client/oldoldstable,now 1:7.9p1-10+deb10u2 arm64 [installed,upgradable to: 1:7.9p1-10+deb10u3]
openssh-server/oldoldstable,now 1:7.9p1-10+deb10u2 arm64 [installed,upgradable to: 1:7.9p1-10+deb10u3]
openssh-sftp-server/oldoldstable,now 1:7.9p1-10+deb10u2 arm64 [installed,upgradable to: 1:7.9p1-10+deb10u3]
openssl/oldoldstable,now 1.1.1n-0+deb10u3 arm64 [installed,upgradable to: 1.1.1n-0+deb10u6]
orca/now 3.30.1-1 all [installed,upgradable to: 3.30.1-2]
p7zip-full/oldoldstable,now 16.02+dfsg-6 arm64 [installed]
p7zip/oldoldstable,now 16.02+dfsg-6 arm64 [installed,automatic]
packagekit/oldoldstable,now 1.1.12-5 arm64 [installed]
pamix/oldoldstable,now 1.6~git20180112.ea4ab3b-3 arm64 [installed]
parted/oldoldstable,now 3.2-25 arm64 [installed]
passwd/oldoldstable,now 1:4.5-1.1 arm64 [installed]
pasystray/oldoldstable,now 0.7.1-1 arm64 [installed]
patch/oldoldstable,oldoldstable,now 2.7.6-3+deb10u1 arm64 [installed,automatic]
pavucontrol-qt/oldoldstable,now 0.14.1-1 arm64 [installed]
pavucontrol/oldoldstable,now 3.0-4 arm64 [installed]
pavumeter/oldoldstable,now 0.9.3-4+b3 arm64 [installed]
pciutils/oldoldstable,now 1:3.5.2-1 arm64 [installed]
perl-base/oldoldstable,now 5.28.1-6+deb10u1 arm64 [installed]
perl-modules-5.28/oldoldstable,oldoldstable,now 5.28.1-6+deb10u1 all [installed,automatic]
perl-openssl-defaults/oldoldstable,now 3 arm64 [installed,automatic]
perl/oldoldstable,now 5.28.1-6+deb10u1 arm64 [installed,automatic]
pinentry-curses/oldoldstable,now 1.1.0-2 arm64 [installed]
pkg-config/oldoldstable,now 0.29-6 arm64 [installed]
policykit-1-gnome/oldoldstable,now 0.105-7 arm64 [installed,automatic]
policykit-1/oldoldstable,oldoldstable,now 0.105-25+deb10u1 arm64 [installed]
poppler-data/oldoldstable,oldoldstable,now 0.4.9-2 all [installed,automatic]
poppler-utils/oldoldstable,now 0.71.0-5 arm64 [installed,upgradable to: 0.71.0-5+deb10u2]
ppp/oldoldstable,oldoldstable,now 2.4.7-2+4.1+deb10u1 arm64 [installed,automatic]
printer-driver-all/oldoldstable,oldoldstable,now 0.20170124 all [installed]
printer-driver-hpcups/oldoldstable,now 3.18.12+dfsg0-2 arm64 [installed,automatic]
procps/oldoldstable,now 2:3.3.15-2 arm64 [installed,automatic]
profile-sync-daemon/oldoldstable,oldoldstable,now 6.31-1 all [installed]
psmisc/oldoldstable,now 23.2-1+deb10u1 arm64 [installed]
pulseaudio-module-bluetooth/oldoldstable,now 12.2-4+deb10u1 arm64 [installed]
pulseaudio-utils/oldoldstable,now 12.2-4+deb10u1 arm64 [installed,automatic]
pulseaudio/oldoldstable,now 12.2-4+deb10u1 arm64 [installed,automatic]
pv/oldoldstable,now 1.6.6-1 arm64 [installed]
python-apt-common/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 1.8.4.3 all [installed,automatic]
python-dev/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
python-matplotlib-data/oldoldstable,oldoldstable,now 3.0.2-2 all [installed,automatic]
python-minimal/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
python-pip-whl/oldoldstable,oldoldstable,now 18.1-5 all [installed,automatic]
python-talloc/oldoldstable,now 2.1.14-2 arm64 [installed,automatic]
python2-dev/oldoldstable,now 2.7.16-1 arm64 [installed]
python2-minimal/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
python2.7-dev/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
python2.7-minimal/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
python2.7/oldoldstable,now 2.7.16-2+deb10u1 arm64 [installed,upgradable to: 2.7.16-2+deb10u3]
python2/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
python3-apt/oldoldstable,oldoldstable,now 1.8.4.3 arm64 [installed]
python3-brlapi/oldoldstable,now 5.6-10+deb10u1 arm64 [installed,automatic]
python3-cairo/oldoldstable,now 1.16.2-1+b1 arm64 [installed,automatic]
python3-certifi/oldoldstable,oldoldstable,now 2018.8.24-1 all [installed,automatic]
python3-chardet/oldoldstable,oldoldstable,now 3.0.4-3 all [installed,automatic]
python3-configobj/oldoldstable,oldoldstable,now 5.0.6-3 all [installed,automatic]
python3-cups/oldoldstable,now 1.9.73-2+b1 arm64 [installed,automatic]
python3-cupshelpers/oldoldstable,oldoldstable,now 1.5.11-4 all [installed,automatic]
python3-cycler/oldoldstable,oldoldstable,now 0.10.0-1 all [installed,automatic]
python3-dateutil/oldoldstable,oldoldstable,now 2.7.3-3 all [installed,automatic]
python3-dbus/oldoldstable,now 1.2.8-3 arm64 [installed,automatic]
python3-debian/oldoldstable,oldoldstable,now 0.1.35 all [installed,automatic]
python3-dev/oldoldstable,now 3.7.3-1 arm64 [installed]
python3-distro-info/oldoldstable,oldoldstable,now 0.21 all [installed,automatic]
python3-distutils/oldoldstable,oldoldstable,now 3.7.3-1 all [installed]
python3-ewmh/oldoldstable,oldoldstable,now 0.1.6-1 all [installed,automatic]
python3-gi-cairo/oldoldstable,now 3.30.4-1 arm64 [installed,automatic]
python3-gi/oldoldstable,now 3.30.4-1 arm64 [installed,automatic]
python3-idna/oldoldstable,oldoldstable,now 2.6-1 all [installed,automatic]
python3-kiwisolver/oldoldstable,now 1.0.1-2+b1 arm64 [installed,automatic]
python3-lib2to3/oldoldstable,oldoldstable,now 3.7.3-1 all [installed,automatic]
python3-libgpiod/oldoldstable,now 1.2-3 arm64 [installed]
python3-louis/oldoldstable,oldoldstable,now 3.8.0-2 all [installed,automatic]
python3-mako/oldoldstable,oldoldstable,now 1.0.7+ds1-1 all [installed,upgradable to: 1.0.7+ds1-1+deb10u1]
python3-markdown/oldoldstable,oldoldstable,now 3.0.1-3 all [installed,automatic]
python3-markupsafe/oldoldstable,now 1.1.0-1 arm64 [installed,automatic]
python3-matplotlib/oldoldstable,now 3.0.2-2 arm64 [installed]
python3-minimal/oldoldstable,now 3.7.3-1 arm64 [installed,automatic]
python3-netifaces/oldoldstable,now 0.10.4-1+b1 arm64 [installed,automatic]
python3-numpy/oldoldstable,now 1:1.16.2-1 arm64 [installed]
python3-pexpect/oldoldstable,oldoldstable,now 4.6.0-1 all [installed,automatic]
python3-pil/oldoldstable,oldoldstable,now 5.4.1-2+deb10u3 arm64 [installed,automatic]
python3-pip/oldoldstable,oldoldstable,now 18.1-5 all [installed]
python3-pkg-resources/oldoldstable,oldoldstable,now 40.8.0-1 all [installed,automatic]
python3-psutil/oldoldstable,now 5.5.1-1 arm64 [installed,automatic]
python3-ptyprocess/oldoldstable,oldoldstable,now 0.6.0-1 all [installed,automatic]
python3-pyatspi/oldoldstable,oldoldstable,now 2.30.0+dfsg-3 all [installed,automatic]
python3-pycurl/oldoldstable,now 7.43.0.2-0.1 arm64 [installed,automatic]
python3-pyparsing/oldoldstable,oldoldstable,now 2.2.0+dfsg1-2 all [installed,automatic]
python3-reportlab-accel/oldoldstable,now 3.5.13-1+deb10u1 arm64 [installed,upgradable to: 3.5.13-1+deb10u2]
python3-reportlab/oldoldstable,oldoldstable,now 3.5.13-1+deb10u1 all [installed,upgradable to: 3.5.13-1+deb10u2]
python3-requests/oldoldstable,oldoldstable,now 2.21.0-1 all [installed,upgradable to: 2.21.0-1+deb10u1]
python3-six/oldoldstable,oldoldstable,now 1.12.0-1 all [installed,automatic]
python3-software-properties/oldoldstable,oldoldstable,now 0.96.20.2-2 all [installed,automatic]
python3-speechd/oldoldstable,oldoldstable,now 0.9.0-5+deb10u1 all [installed,automatic]
python3-urllib3/oldoldstable,oldoldstable,now 1.24.1-1 all [installed,automatic]
python3-virtualenv/oldoldstable,oldoldstable,now 15.1.0+ds-2+deb10u1 all [installed]
python3-xdg/oldoldstable,oldoldstable,now 0.25-5 all [installed,automatic]
python3-xlib/oldoldstable,oldoldstable,now 0.23-2 all [installed,automatic]
python3-yaml/oldoldstable,now 3.13-2 arm64 [installed,automatic]
python3.7-dev/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
python3.7-minimal/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
python3.7/oldoldstable,now 3.7.3-2+deb10u3 arm64 [installed,upgradable to: 3.7.3-2+deb10u5]
python3/oldoldstable,now 3.7.3-1 arm64 [installed,automatic]
python/oldoldstable,now 2.7.16-1 arm64 [installed,automatic]
qrencode/oldoldstable,now 4.0.2-1 arm64 [installed]
readline-common/oldoldstable,oldoldstable,now 7.0-5 all [installed]
redshift/oldoldstable,now 1.12-2 arm64 [installed]
resolvconf/oldoldstable,oldoldstable,now 1.79 all [installed]
rfkill/oldoldstable,now 2.33.1-0.1 arm64 [installed]
rsync/oldoldstable,now 3.1.3-6 arm64 [installed]
rsyslog/oldoldstable,oldoldstable,now 8.1901.0-1+deb10u2 arm64 [installed]
samba-common/oldoldstable,oldoldstable,now 2:4.9.5+dfsg-5+deb10u3 all [installed,upgradable to: 2:4.9.5+dfsg-5+deb10u4]
samba-libs/oldoldstable,now 2:4.9.5+dfsg-5+deb10u3 arm64 [installed,upgradable to: 2:4.9.5+dfsg-5+deb10u4]
screen/oldoldstable,oldoldstable,now 4.6.2-3+deb10u1 arm64 [installed]
sed/oldoldstable,now 4.7-1 arm64 [installed]
sensible-utils/oldoldstable,oldoldstable,now 0.0.12 all [installed]
shared-mime-info/oldoldstable,now 1.10-1 arm64 [installed]
slick-greeter/oldoldstable,now 1.2.4-2 arm64 [installed]
smartmontools/oldoldstable,now 6.6-1 arm64 [installed]
smbclient/oldoldstable,now 2:4.9.5+dfsg-5+deb10u3 arm64 [installed,upgradable to: 2:4.9.5+dfsg-5+deb10u4]
software-properties-common/oldoldstable,oldoldstable,now 0.96.20.2-2 all [installed]
software-properties-gtk/oldoldstable,oldoldstable,now 0.96.20.2-2 all [installed]
sound-theme-freedesktop/oldoldstable,oldoldstable,now 0.8-2 all [installed,automatic]
speech-dispatcher-audio-plugins/oldoldstable,now 0.9.0-5+deb10u1 arm64 [installed,automatic]
speech-dispatcher/oldoldstable,now 0.9.0-5+deb10u1 arm64 [installed,automatic]
spice-vdagent/oldoldstable,now 0.18.0-1 arm64 [installed]
ssl-cert/oldoldstable,oldoldstable,now 1.0.39 all [installed,automatic]
stm32flash/oldoldstable,now 0.5-1+b1 arm64 [installed]
stress/oldoldstable,now 1.0.4-4 arm64 [installed]
sudo/oldoldstable,now 1.8.27-1+deb10u3 arm64 [installed,upgradable to: 1.8.27-1+deb10u5]
sunxi-tools/oldoldstable,now 1.4.2+git20181114.6d598a-3 arm64 [installed]
sysfsutils/oldoldstable,now 2.1.0+repack-5 arm64 [installed]
sysstat/oldoldstable,now 12.0.3-2 arm64 [installed,upgradable to: 12.0.3-2+deb10u2]
system-config-printer-common/oldoldstable,oldoldstable,now 1.5.11-4 all [installed,automatic]
system-config-printer/oldoldstable,oldoldstable,now 1.5.11-4 all [installed]
systemd-sysv/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
systemd/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
sysvinit-utils/oldoldstable,now 2.93-8 arm64 [installed]
tar/oldoldstable,now 1.30+dfsg-6 arm64 [installed]
tcl-expect/oldoldstable,now 5.45.4-2 arm64 [installed,automatic]
tcl8.6/oldoldstable,now 8.6.9+dfsg-2 arm64 [installed,automatic]
terminator/oldoldstable,oldoldstable,now 1.91-4 all [installed]
thunar-data/oldoldstable,oldoldstable,now 1.8.4-1 all [installed,automatic]
thunar-volman/oldoldstable,now 0.9.1-1 arm64 [installed]
thunar/oldoldstable,now 1.8.4-1 arm64 [installed,automatic]
tmux/oldoldstable,now 2.8-3 arm64 [installed,upgradable to: 2.8-3+deb10u1]
toilet-fonts/oldoldstable,oldoldstable,now 0.3-1.2 all [installed,automatic]
toilet/oldoldstable,now 0.3-1.2 arm64 [installed]
ttf-bitstream-vera/oldoldstable,oldoldstable,now 1.10-8 all [installed,automatic]
ttf-ubuntu-font-family/oldoldstable,oldoldstable,now 1:0.83-4 all [installed]
tzdata/now 2021a-0+deb10u5 all [installed,upgradable to: 2021a-0+deb10u11]
u-boot-tools/oldoldstable,now 2019.01+dfsg-7 arm64 [installed]
ucf/oldoldstable,oldoldstable,now 3.0038+nmu1 all [installed]
udev/oldoldstable,now 241-7~deb10u8 arm64 [installed,upgradable to: 241-7~deb10u10]
udisks2/oldoldstable,now 2.8.1-4 arm64 [installed,upgradable to: 2.8.1-4+deb10u2]
unattended-upgrades/oldoldstable,oldoldstable,now 1.11.2 all [installed]
unicode-data/oldoldstable,oldoldstable,now 12.1.0~pre1-2 all [installed]
unzip/oldoldstable,now 6.0-23+deb10u2 arm64 [installed,upgradable to: 6.0-23+deb10u3]
update-inetd/oldoldstable,oldoldstable,now 4.49 all [installed]
usb-modeswitch-data/oldoldstable,oldoldstable,now 20170806-2 all [installed]
usb-modeswitch/oldoldstable,now 2.5.2+repack0-2 arm64 [installed]
usb.ids/oldoldstable,oldoldstable,now 2019.07.27-0+deb10u1 all [installed,automatic]
usbutils/oldoldstable,now 1:010-3 arm64 [installed]
util-linux/oldoldstable,now 2.33.1-0.1 arm64 [installed]
uuid-dev/oldoldstable,now 2.33.1-0.1 arm64 [installed,automatic]
viewnior/oldoldstable,now 1.6-1+b1 arm64 [installed]
vim-common/oldoldstable,oldoldstable,now 2:8.1.0875-5+deb10u2 all [installed,upgradable to: 2:8.1.0875-5+deb10u6]
vim-runtime/oldoldstable,oldoldstable,now 2:8.1.0875-5+deb10u2 all [installed,upgradable to: 2:8.1.0875-5+deb10u6]
vim/oldoldstable,now 2:8.1.0875-5+deb10u2 arm64 [installed,upgradable to: 2:8.1.0875-5+deb10u6]
virtualenv/oldoldstable,oldoldstable,now 15.1.0+ds-2+deb10u1 all [installed]
vlan/oldoldstable,oldoldstable,now 2.0.5 all [installed]
wget/oldoldstable,now 1.20.1-1.1 arm64 [installed]
whiptail/oldoldstable,now 0.52.20-8 arm64 [installed]
wireguard-tools/buster,now 1.0.20200827-1~bpo10+1 arm64 [installed]
wireless-regdb/oldoldstable,oldoldstable,now 2016.06.10-1 all [installed,upgradable to: 2022.04.08-2~deb10u1]
wireless-tools/oldoldstable,now 30~pre9-13 arm64 [installed]
wpasupplicant/oldoldstable,oldoldstable,now 2:2.7+git20190128+0c1e29f-6+deb10u3 arm64 [installed]
x11-apps/oldoldstable,now 7.7+7 arm64 [installed]
x11-common/oldoldstable,oldoldstable,now 1:7.7+19 all [installed,automatic]
x11-utils/oldoldstable,now 7.7+4 arm64 [installed,automatic]
x11-xkb-utils/oldoldstable,now 7.7+4 arm64 [installed,automatic]
x11-xserver-utils/oldoldstable,now 7.7+8 arm64 [installed]
x11proto-core-dev/oldoldstable,oldoldstable,now 2018.4-4 all [installed,automatic]
x11proto-dev/oldoldstable,oldoldstable,now 2018.4-4 all [installed,automatic]
x11proto-xext-dev/oldoldstable,oldoldstable,now 2018.4-4 all [installed,automatic]
xarchiver/oldoldstable,now 1:0.5.4.14-1 arm64 [installed]
xauth/oldoldstable,now 1:1.0.10-1 arm64 [installed,automatic]
xbacklight/oldoldstable,now 1.2.1-1+b2 arm64 [installed]
xbitmaps/oldoldstable,oldoldstable,now 1.1.1-2 all [installed,automatic]
xcursor-themes/oldoldstable,oldoldstable,now 1.0.5-1 all [installed]
xdg-user-dirs-gtk/oldoldstable,now 0.10-3 arm64 [installed]
xdg-user-dirs/oldoldstable,now 0.17-2 arm64 [installed]
xdg-utils/oldoldstable,oldoldstable,now 1.1.3-1+deb10u1 all [installed,automatic]
xdotool/oldoldstable,now 1:3.20160805.1-4 arm64 [installed]
xfce4-appfinder/oldoldstable,now 4.12.0-2 arm64 [installed,automatic]
xfce4-notifyd/oldoldstable,now 0.4.3-1 arm64 [installed]
xfce4-panel/oldoldstable,now 4.12.2-1 arm64 [installed,automatic]
xfce4-pulseaudio-plugin/oldoldstable,now 0.4.1-1 arm64 [installed,automatic]
xfce4-screenshooter/oldoldstable,now 1.9.3-1 arm64 [installed]
xfce4-session/oldoldstable,now 4.12.1-6 arm64 [installed,automatic]
xfce4-settings/oldoldstable,now 4.12.4-1 arm64 [installed,automatic]
xfce4-terminal/oldoldstable,now 0.8.7.4-2 arm64 [installed]
xfce4/oldoldstable,oldoldstable,now 4.12.5 all [installed]
xfconf/oldoldstable,now 4.12.1-1 arm64 [installed,automatic]
xfdesktop4-data/oldoldstable,oldoldstable,now 4.12.4-2 all [installed,automatic]
xfdesktop4/oldoldstable,now 4.12.4-2 arm64 [installed,automatic]
xfonts-100dpi/oldoldstable,oldoldstable,now 1:1.0.4+nmu1 all [installed]
xfonts-75dpi/oldoldstable,oldoldstable,now 1:1.0.4+nmu1 all [installed]
xfonts-base/oldoldstable,oldoldstable,now 1:1.0.5 all [installed]
xfonts-encodings/oldoldstable,oldoldstable,now 1:1.0.4-2 all [installed]
xfonts-scalable/oldoldstable,oldoldstable,now 1:1.0.3-1.1 all [installed]
xfonts-utils/oldoldstable,now 1:7.7+6 arm64 [installed]
xfwm4/oldoldstable,now 4.12.5-1 arm64 [installed,automatic]
xinit/oldoldstable,now 1.4.0-1 arm64 [installed]
xinput/oldoldstable,now 1.6.2-1+b1 arm64 [installed]
xkb-data/oldoldstable,oldoldstable,now 2.26-2 all [installed]
xorg-docs-core/oldoldstable,oldoldstable,now 1:1.7.1-1.1 all [installed]
xorg-sgml-doctools/oldoldstable,oldoldstable,now 1:1.11-1 all [installed,automatic]
xscreensaver-data/oldoldstable,now 5.42+dfsg1-1 arm64 [installed,automatic]
xscreensaver/oldoldstable,now 5.42+dfsg1-1 arm64 [installed]
xserver-common/oldoldstable,oldoldstable,now 2:1.20.4-1+deb10u4 all [installed,upgradable to: 2:1.20.4-1+deb10u9]
xserver-xorg-core/oldoldstable,now 2:1.20.4-1+deb10u4 arm64 [installed,upgradable to: 2:1.20.4-1+deb10u9]
xserver-xorg-input-all/oldoldstable,now 1:7.7+19 arm64 [installed,automatic]
xserver-xorg-input-libinput/oldoldstable,now 0.28.2-2 arm64 [installed,automatic]
xserver-xorg-legacy/oldoldstable,now 2:1.20.4-1+deb10u4 arm64 [installed,upgradable to: 2:1.20.4-1+deb10u9]
xserver-xorg-video-fbdev/oldoldstable,now 1:0.5.0-1 arm64 [installed]
xserver-xorg/oldoldstable,now 1:7.7+19 arm64 [installed]
xterm/oldoldstable,now 344-1+deb10u2 arm64 [installed]
xtermcontrol/oldoldstable,now 3.3-2 arm64 [installed]
xtermset/oldoldstable,now 0.5.2-6+b1 arm64 [installed]
xtrans-dev/oldoldstable,oldoldstable,now 1.3.5-1 all [installed,automatic]
xwallpaper/oldoldstable,now 0.4.1-1 arm64 [installed]
xxd/oldoldstable,now 2:8.1.0875-5+deb10u2 arm64 [installed,upgradable to: 2:8.1.0875-5+deb10u6]
xz-utils/oldoldstable,oldoldstable,now 5.2.4-1+deb10u1 arm64 [installed,automatic]
zip/oldoldstable,now 3.0-11+b1 arm64 [installed]
zlib1g-dev/oldoldstable,now 1:1.2.11.dfsg-1+deb10u1 arm64 [installed,upgradable to: 1:1.2.11.dfsg-1+deb10u2]
zlib1g/oldoldstable,now 1:1.2.11.dfsg-1+deb10u1 arm64 [installed,upgradable to: 1:1.2.11.dfsg-1+deb10u2]
zsh-common/oldoldstable,oldoldstable,oldoldstable,oldoldstable,now 5.7.1-1+deb10u1 all [installed,automatic]
zsh/oldoldstable,oldoldstable,now 5.7.1-1+deb10u1 arm64 [installed,automatic]
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

~~~
<details>
 <summary>Résultat de la commande sur ma machine (Cliquez pour déplier!)</summary>
<pre>

</pre>
</details>

---
-->



