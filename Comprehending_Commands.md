# Comprehending Commands

## 1. cat: not the pet, but the commmand!
To learn cat command.

### Solve
**Flag** `pwn.college{MdyOFbhzVYMTXja1Ng1S03lhMMf.QXxcTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{MdyOFbhzVYMTXja1Ng1S03lhMMf.QXxcTN0wCMwEzNzEzW}
```

### New Learnings
cat command is used for reading out files.

## 2. catting absolute paths

### Solve
**Flag** `pwn.college{4_Y_CVNwExd51vRemeSPaCu-YK0.QX5ETO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{4_Y_CVNwExd51vRemeSPaCu-YK0.QX5ETO0wCMwEzNzEzW}
```

## 3. more catting practice

### Solve 
**Flag** `pwn.college{s7NNNcB77_TFWGhkM3MzQW6ABSr.QXwITO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~more-catting-practice:~$ cat flag
cat: flag: No such file or directory
hacker@commands~more-catting-practice:~$ cd flag
You used 'cd'! In this level, I don't allow you to change the working directory
--- you MUST chase pass 'cat' the absolute path of where I put it on the
filesystem (which is /usr/share/vim/flag).
hacker@commands~more-catting-practice:~$ cat /usr/share/vim/flag
pwn.college{s7NNNcB77_TFWGhkM3MzQW6ABSr.QXwITO0wCMwEzNzEzW}
```

## 4. grepping for a n eedle in a haystack
To learn grep command

### Solve 
**Flag** `pwn.college{AyercwvsTw4eHGtESqPf88-X6d0.QX3EDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{AyercwvsTw4eHGtESqPf88-X6d0.QX3EDO0wCMwEzNzEzW}
```

### New Learnings
grep command is used to search for contents in larger files.
Format:  
grep SEARCH_STRING /path/to/file

## 5. comparing files
To learn diff command to compare 2 files.

### Solve 
**Flag**  ` pwn.college{E1Ro0CISaO99UFe16Ir3PaB2CVd.01MwMDOxwCMwEzNzEzW}`
To solve  
```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_and_real.txt /challenge/decoys_only.txt
12d11
< pwn.college{E1Ro0CISaO99UFe16Ir3PaB2CVd.01MwMDOxwCMwEzNzEzW}
```

### New Learnings
The diff command compares 2 files line by line and shows the difference.
Format: diff file1 file2
Output: <difference in 1st file >difference in second file

## 6. listing files
To learn ls command to list files.

### Solve 
**Flag** `pwn.college{MVDuZ4LRdIpjqBFbnRgY22LPq7i.QX4IDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~listing-files:~$ ls /challenge
6290-renamed-run-10563  DESCRIPTION.md
hacker@commands~listing-files:~$ cat /challenge/6290-renamed-run-10563
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:~$ cat /flag
cat: /flag: Permission denied
hacker@commands~listing-files:~$  /challenge/6290-renamed-run-10563
Yahaha, you found me! Here is your flag:
pwn.college{MVDuZ4LRdIpjqBFbnRgY22LPq7i.QX4IDO0wCMwEzNzEzW}
```

### New Learnings

The ls command is used for listing files.

## 7. touching files
Use touch command to create files.

### Solve 
**Flag** `pwn.college{cyxKRXGTgx777E_6Vayzr65Ey8V.QXwMDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{cyxKRXGTgx777E_6Vayzr65Ey8V.QXwMDO0wCMwEzNzEzW}
```

### New Learnings
The touch command is used to create a new blank file inside a directory.

## 8. removing files
To use rm command to remove files.

### Solve 
**Flag** `pwn.college{kqMHbSJGPJ8Av5hKiH5tXilFShR.QX2kDM1wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{kqMHbSJGPJ8Av5hKiH5tXilFShR.QX2kDM1wCMwEzNzEzW}
```

### New Learnings
The rm command is used to remove files.

## 9. moving files
To use mv command to move files.

### Solve 
**Flag** `pwn.college{AFPaq6Afy_FfXQvQ5cmQrQbWnw2.0VOxEzNxwCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{AFPaq6Afy_FfXQvQ5cmQrQbWnw2.0VOxEzNxwCMwEzNzEzW}
```

### New Learnings
The mv command is used to move files.
Format: mv file1 file2
The contents of file1 would move to file2

## 10. hidden files
To find the hidden flag using -a after ls to see the file.

### Solve 
**Flag** `pwn.college{cAcxI2wxMPR1QXC_DW53_zyq02g.QXwUDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~hidden-files:~$ ls -a /
.                      bin        etc    lib64   nix   run   tmp
..                     boot       home   libx32  opt   sbin  usr
.dockerenv             challenge  lib    media   proc  srv   var
.flag-116851949825709  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:~$ cat /.flag-116851949825709
pwn.college{cAcxI2wxMPR1QXC_DW53_zyq02g.QXwUDO0wCMwEzNzEzW}
```

### New Learnings
The ls command does not list files that start with .a by default. These files are hidden.
Use ls -a to show them.

## 11. An Epic Filesystem Quest

### Solve 
**Flag** `pwn.college{00C3weLnoUnPwqogTGn-InPePPB.QX5IDO0wCMwEzNzEzW}`  
to solve 
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
GIST  challenge  flag  lib32   media  opt   run   sys  var
bin   dev        home  lib64   mnt    proc  sbin  tmp
boot  etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat /GIST
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/TeX/Script`

`The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ ls -a  /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/TeX/Script
.  ..  .INSIGHT  Regular
hacker@commands~an-epic-filesystem-quest:/$ cat  /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/TeX/Script/.INSIGHT
Great sleuthing!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Asana-Math/Size6/Regular`

`Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Asana-Math/Size6/Regular
Main.js  README-TRAPPED
hacker@commands~an-epic-filesystem-quest:/$ cat README-TRAPPED
cat: README-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/javascript/mathjax/unpacked/jax/output/HTML-CSS/fonts/Asana-Math/Size6/Regular/README-TRAPPED
Lucky listing!
The next clue is in: /usr/share/systemtap/tapset`

`The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/systemtap/tapset
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ ls /usr/share/systemtap/tapset
DOSSIER  libruby2.7-x86_64-linux-gnu.stp
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ cat /usr/share/systemtap/tapset/DOSSIER
Great sleuthing!
The next clue is in: /usr/share/locale/na/LC_MESSAGES
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ ls  /usr/share/locale/na/LC_MESSAGES
CLUE  iso_3166-1.mo  iso_3166.mo
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ cat CLUE
cat: CLUE: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ cat  /usr/share/locale/na/LC_MESSAGES/CLUE
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/sage/coding/guruswami_sudan/__pycache__`

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ ls -a  /usr/lib/python3/dist-packages/sage/coding/guruswami_sudan/__py
cache__
.          __init__.cpython-38.pyc       utils.cpython-38.pyc
..         gs_decoder.cpython-38.pyc
.DISPATCH  interpolation.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ cat /usr/lib/python3/dist-packages/sage/coding/guruswami_sudan/__pycache__/.DISPATCH
Yahaha, you found me!
The next clue is in: /usr/share/emacs/26.3/etc/images/ezimage`

`The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/systemtap/tapset$ cd  /usr/share/emacs/26.3/etc/images/ezimage
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/etc/images/ezimage$ ls  /usr/share/emacs/26.3/etc/images/ezimage
README         checkmark.pbm  doc.pbm    page-minus.pbm  tag-type.pbm
WHISPER        checkmark.xpm  doc.xpm    page-minus.xpm  tag-type.xpm
bits.pbm       dir-minus.pbm  info.pbm   page-plus.pbm   tag-v.pbm
bits.xpm       dir-minus.xpm  info.xpm   page-plus.xpm   tag-v.xpm
bitsbang.pbm   dir-plus.pbm   key.pbm    page.pbm        tag.pbm
bitsbang.xpm   dir-plus.xpm   key.xpm    page.xpm        tag.xpm
box-minus.pbm  dir.pbm        label.pbm  tag-gt.pbm      unlock.pbm
box-minus.xpm  dir.xpm        label.xpm  tag-gt.xpm      unlock.xpm
box-plus.pbm   doc-minus.pbm  lock.pbm   tag-minus.pbm
box-plus.xpm   doc-minus.xpm  lock.xpm   tag-minus.xpm
box.pbm        doc-plus.pbm   mail.pbm   tag-plus.pbm
box.xpm        doc-plus.xpm   mail.xpm   tag-plus.xpm
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/etc/images/ezimage$ cat  /usr/share/emacs/26.3/etc/images/ezimage/WHISPER
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/misc/mic/cosm

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/etc/images/ezimage$ cd  /opt/linux/linux-5.4/drivers/misc/mic/cosm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/misc/mic/cosm$ ls  /opt/linux/linux-5.4/drivers/misc/mic/cosm
EVIDENCE  cosm_debugfs.c  cosm_main.h         cosm_sysfs.c
Makefile  cosm_main.c     cosm_scif_server.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/misc/mic/cosm$ cat  /opt/linux/linux-5.4/drivers/misc/mic/cosm/EVIDENCE
Yahaha, you found me!
The next clue is in: /usr/share/emacs/26.3/lisp/url
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/misc/mic/cosm$ ls /usr/share/emacs/26.3/lisp/url
TIP             url-expand.elc    url-irc.elc      url-privacy.elc
url-about.elc   url-file.elc      url-ldap.elc     url-proxy.elc
url-auth.elc    url-ftp.elc       url-mailto.elc   url-queue.elc
url-cache.elc   url-future.elc    url-methods.elc  url-tramp.elc
url-cid.elc     url-gw.elc        url-misc.elc     url-util.elc
url-cookie.elc  url-handlers.elc  url-news.elc     url-vars.elc
url-dav.elc     url-history.elc   url-nfs.elc      url.elc
url-dired.elc   url-http.elc      url-ns.elc
url-domsuf.elc  url-imap.elc      url-parse.elc
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/misc/mic/cosm$ cat /usr/share/emacs/26.3/lisp/url/TIP
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{00C3weLnoUnPwqogTGn-InPePPB.QX5IDO0wCMwEzNzEzW}
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/misc/mic/cosm$ /usr/share/emacs/26.3/lisp/url/usr/share/emacs/26.3/lisp/url/usr/share/emacs/26.3/lisp/url/usr/share/emacs/26.3/lisp/url
```

## 12. making directories
Using mkdir command to make a directory and add a file to it using touch command.

### Solve 
**Flag** `pwn.college{kGXEz2qnQXOqyyovrikwkg79MbL.QXxMDO0wCMwEzNzEzW}`  
to solve
```bash
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{kGXEz2qnQXOqyyovrikwkg79MbL.QXxMDO0wCMwEzNzEzW}
hacker@commands~making-directories:/tmp/pwn$ pwn.college{kGXEz2qnQXOqyyovrikwkg79MbL.QXxMDO0wCMwEzNzEzW}
```

### New Learnings
The mkdir command is used to make a new directory.

## 13. finding files
Using the command find to find a file.

### Solve 
**Flag** `pwn.college{sFd0ZD7WDPtpBpaRkozrah_WfUS.QXyMDO0wCMwEzNzEzW}`  

To solve:
```bash
hacker@commands~finding-files:~$ find  / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/emacs/26.3/etc/images/icons/hicolor/32x32/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ /usr/local/lib/python3.8/dist-packages/pwnlib/flag^C
hacker@commands~finding-files:~$ cat /usr/share/emacs/26.3/etc/images/icons/hicolor/32x32/flag
pwn.college{sFd0ZD7WDPtpBpaRkozrah_WfUS.QXyMDO0wCMwEzNzEzW}
```

### New Learnings
The find command is used to find files.
Format: find argument.
The argument can be a location or name using '-name filename'. If no argument is specified then find matches every file. 
To search the whole file system: 'find / -name filename;

## 14. linking files

### Solve 
**Flag** `pwn.college{szXCJOrimeCxho4aIeUUCQIHe76.QX5ETN1wCMwEzNzEzW}`  
to solve  
```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
ln: failed to create symbolic link '/home/hacker/not-the-flag': File exists
hacker@commands~linking-files:~$ rm -f ~/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ls -l /home/hacker/not-the-flag
lrwxrwxrwx 1 hacker hacker 5 Sep 29 12:40 /home/hacker/not-the-flag -> /flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{szXCJOrimeCxho4aIeUUCQIHe76.QX5ETN1wCMwEzNzEzW}
```


### New Learnings
Symbolic links or soft links are a special type of file that references another file.
Format: ln -s file-to-be-linked file
