

## Distros

- The distros share the same Linux kernel (core system)
- Open-source code allows for easy bug review and fast issue resolution
- The distros share the same access model. Clear distinction between regular users and root enhances security
- sudo grants temporary privileges, reducing accidental changes
<br>
<br>

<img width="728" height="480" alt="image" src="https://github.com/user-attachments/assets/bce1134c-6f4e-4244-8048-15a76f0453ec" />
<br>
- can have a play with difffernet distros to see what u prefer!

## Understanding the Linux filesystem
/ - forward lash to go into root 

- Directories contain sub directories
- Can be an ordinary file, a directory (folder), a device or a link (pointer to other file)
  
## Special filesystem directories
-  /etc - Configuration Files
-  /dev – Devices
-   tmp – Temporary Files
-   /mnt – Mount Directory 
➢ /mnt – Mount Directory (like a cdrom , hard drive, floppy disc etc)


## Commands

- /bin – User Binaries, binary executables eg  ps, ls, ping, grep, cp
- /sbin – System Binaries, eg iptables, reboot, fdisk, ifconfig
- /var – Variable Files. Content of the files that are expected to grow can be found under this directory eg ystem log files (/var/log);        packages and database files (/var/lib); emails (/var/mail); print queues (/var/spool); lock files (/var/lock); temp files needed across      reboots (/var/tmp)
- /boot – Boot Loader Files , uploading whatever we need
- /usr vs /home. /usr was where the home directories of the users were placed (that is to say, /usr/someone was then the directory now known    as /home/someone. So bascially on newer versions known as home!
- /opt – Optional add-on Applications
<br>
<br>

<img width="736" height="716" alt="image" src="https://github.com/user-attachments/assets/a955f8c9-d8b8-440e-a82c-babcf3349968" />

<br>

- Remember /dev controls devices such as hard drvies
- /mnt owuld be relevant when importing additional storgae devices (external media )
- Rememer Linux also is case sensentive


