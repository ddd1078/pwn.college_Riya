# Untangling Users

## 1. Becoming root with su

### Solve
**Flag** `pwn.college{E0PAC0etrSumw9a0--6CKctTIjc.QX1UDN1wCMwEzNzEzW}`

```bash
hacker@users~becoming-root-with-su:~$ su
Password:
su: Authentication failure
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# ls
COLLEGE  Desktop  PWN  a  instructions  myflag  not-the-flag  pwn  the-flag
root@users~becoming-root-with-su:/home/hacker# cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{E0PAC0etrSumw9a0--6CKctTIjc.QX1UDN1wCMwEzNzEzW}
```

### New Learnings
The root means the system administrator who can administer the system. su (substitute user command) is used to become the root. It may be password protected.

## 2. Other users with su

### Solve
**Flag** `pwn.college{MPWPimgyAbyxk5XohVziOrK4M9s.QX2UDN1wCMwEzNzEzW}`

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ ls
COLLEGE  Desktop  PWN  a  instructions  myflag  not-the-flag  pwn  the-flag
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{MPWPimgyAbyxk5XohVziOrK4M9s.QX2UDN1wCMwEzNzEzW}
```

### New Learnings
'su' can by used to switch to other users too other than root by:  
su username

## 3. Cracking passwords

### Solve
**Flag** `pwn.college{AezemwpbpAkUdLI5nhU7xmwogcR.QX3UDN1wCMwEzNzEzW}`

```bash
hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$dYa3pLjDfWPM7o53$nOJVQLICBSsemefQrSeWKPSA//mDTPtUFnrJq8cqAdIzxEsg1gJguiPP3JLFoz08J2da0F2eBwCsLfvBgUWbM1:20374:0:99999:7:::
hacker@users~cracking-passwords:~$ su zardus
Password:
su: Authentication failure
hacker@users~cracking-passwords:~$ su zardus
Password:
su: Authentication failure
hacker@users~cracking-passwords:~$  cat /challenge/shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$dYa3pLjDfWPM7o53$nOJVQLICBSsemefQrSeWKPSA//mDTPtUFnrJq8cqAdIzxEsg1gJguiPP3JLFoz08J2da0F2eBwCsLfvBgUWbM1:20374:0:99999:7:::
hacker@users~cracking-passwords:~$ john --show /challenge/shadow-leak
hacker:NO PASSWORD:20357:0:99999:7:::

1 password hash cracked, 1 left
hacker@users~cracking-passwords:~$ john ./zardus.hash --show
?:aardvark

1 password hash cracked, 0 left
hacker@users~cracking-passwords:~$ su zardus
Password:
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{AezemwpbpAkUdLI5nhU7xmwogcR.QX3UDN1wCMwEzNzEzW}
```

### New Learnings
/etc/shadow is where all the passwords are stored and can be accessed by the root.

## 4.  Using sudo

### Solve
**Flag** 

### New Learnings
