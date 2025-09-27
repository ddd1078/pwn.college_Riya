# File Globbing

## 1. Matching wih *

### Solve
**Flag** `pwn.college{ocT4fBZCYISWhaUqD0U85rSt5Gg.QXxIDO0wCMwEzNzEzW}`
To solve
`This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ ls /
This challenge resets your working directory to /home/hacker unless you change
directory properly...
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{ocT4fBZCYISWhaUqD0U85rSt5Gg.QXxIDO0wCMwEzNzEzW}`

## 2. Matching with ?

### Solve
**Flag** `pwn.college{UwsB1vczoH7KlU37ukrM6U5-63Q.QXyIDO0wCMwEzNzEzW}`
To solve
`This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{UwsB1vczoH7KlU37ukrM6U5-63Q.QXyIDO0wCMwEzNzEzW}`

## 3. Matching wih []

### Solve
**Flag** `pwn.college{Mv2ZP3I0BBK0Y-MOmL-bOTQ5Qux.QXzIDO0wCMwEzNzEzW}`
To solve
`hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ echo file_[absh]
file_a file_b file_h file_s
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{Mv2ZP3I0BBK0Y-MOmL-bOTQ5Qux.QXzIDO0wCMwEzNzEzW}`

## 4. Matching paths with []

### Solve
**Flag** `pwn.college{MIuHO92RHZQnl3q_xKzby3F0h_q.QX0IDO0wCMwEzNzEzW}`
To solve
`hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{MIuHO92RHZQnl3q_xKzby3F0h_q.QX0IDO0wCMwEzNzEzW}`

## 5. Multiple globs

### Solve
**Flag**

## 6. Mixing globs

### Solve
**Flag**

## 7. Exclusionary globbing

### Solve
**Flag**

## 8. Tab completion

### Solve
**Flag**

## 9. Multiple options for tab completion

### Solve
**Flag**

## 10. Tab completion on commands

### Solve
**Flag**
