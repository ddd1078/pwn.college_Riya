# Perceiving Permissions

## 1. Changing File Ownership

### Solve
**Flag** `pwn.college{QrzmRe4vQ4PPb0o2Ofz0W47pZ5U.QXxEjN0wCMwEzNzEzW}`
```bash
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 root root 60 Oct 11 04:20 /flag
hacker@permissions~changing-file-ownership:~$ cat /flag 2>/dev/null || echo "no read perms (expected)"
no read perms (expected)
hacker@permissions~changing-file-ownership:~$ chown hacker /flag || sudo chown hacker /flag
hacker@permissions~changing-file-ownership:~$ ls -l /flag
-r-------- 1 hacker root 60 Oct 11 04:20 /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{QrzmRe4vQ4PPb0o2Ofz0W47pZ5U.QXxEjN0wCMwEzNzEzW}
```

### New Learnings

## 2. Groups and Files

### Solve
**Flag** `pwn.college{UffZdyni-fLBEzuIml_MbunE6mC.QXxcjM1wCMwEzNzEzW}`

```bash
hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root root 60 Oct 11 04:25 /flag
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root hacker 60 Oct 11 04:25 /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{UffZdyni-fLBEzuIml_MbunE6mC.QXxcjM1wCMwEzNzEzW}
```

### New Learnings

## 3. Fun Wiht Group Names

### Solve
**Flag** `pwn.college{shPo4cF_8x10edKjQksJUQfWiNR.QXycjM1wCMwEzNzEzW}`

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp26339) groups=1000(grp26339)
hacker@permissions~fun-with-groups-names:~$ id -gn
grp26339
hacker@permissions~fun-with-groups-names:~$ chgrp "$(id -gn)" /flag
hacker@permissions~fun-with-groups-names:~$ ls -l /flag
-r--r----- 1 root grp26339 60 Oct 11 04:26 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{shPo4cF_8x10edKjQksJUQfWiNR.QXycjM1wCMwEzNzEzW}
```

### New Learnings

## 4. Changing Permissions

### Solve
**Flag** `pwn.college{ITwM1PqYcxEChXU2OJy1ufT1Tx4.QXzcjM1wCMwEzNzEzW}`

```bash
hacker@permissions~changing-permissions:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-------- 1 root root 60 Oct 11 04:28 /flag
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ ls -l /flag
-r-----r-- 1 root root 60 Oct 11 04:28 /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{ITwM1PqYcxEChXU2OJy1ufT1Tx4.QXzcjM1wCMwEzNzEzW}
```

### New Learnings

## 5. Executable Files

### Solve
**Flag** `pwn.college{EbWVYhpTIlSjNl6gVAtHiJ_wduJ.QXyEjN0wCMwEzNzEzW}`

```bash
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ chmod +x /challenge/run
hacker@permissions~executable-files:~$ ls -l /challenge/run
-r-xr-xr-x 1 hacker hacker 32 Jan 14  2025 /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{EbWVYhpTIlSjNl6gVAtHiJ_wduJ.QXyEjN0wCMwEzNzEzW}
```

### New Learnings

## 6. Permission Tweaking Practice

### Solve
**Flag** 

### New Learnings

## 7. Permissions Setting Practice

### Solve
**Flag** 

### New Learnings

## 8. The SUID Bit

### Solve
**Flag** `pwn.college{w6x0mxDmQc8ryO1QoHD9FLGYdeu.QXzEjN0wCMwEzNzEzW}`

```bash
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwxr-xr-x 1 root root 155 Jan 14  2025 /challenge/getroot
hacker@permissions~the-suid-bit:~$ file /challenge/getroot
/challenge/getroot: a /opt/pwn.college/bash script, ASCII text executable
hacker@permissions~the-suid-bit:~$ chmod +x /challenge/getroot
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwsr-xr-x 1 root root 155 Jan 14  2025 /challenge/getroot
hacker@permissions~the-suid-bit:~$ stat -c '%A %a %n' /challenge/getroot
-rwsr-xr-x 4755 /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{w6x0mxDmQc8ryO1QoHD9FLGYdeu.QXzEjN0wCMwEzNzEzW}
root@permissions~the-suid-bit:~# pwn.college{w6x0mxDmQc8ryO1QoHD9FLGYdeu.QXzEjN0wCMwEzNzEzW}
```


**Flag** 

### New Learnings
