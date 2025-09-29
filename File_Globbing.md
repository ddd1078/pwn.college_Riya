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

### New Learnings
'*' is a glob which acts as a wildcard which matches argument. If no arguments are matched then the shell leaves the glob unchanged.

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

### New Learnings
'?' is a glob which acts as a single charactered wildcard.

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

### New Learnings
[] is a wildcard for some subset of potential characters, specified within the brackets. 

## 4. Matching paths with []

### Solve
**Flag** `pwn.college{MIuHO92RHZQnl3q_xKzby3F0h_q.QX0IDO0wCMwEzNzEzW}`  
To solve  
`hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{MIuHO92RHZQnl3q_xKzby3F0h_q.QX0IDO0wCMwEzNzEzW}`

### New Learnings
Globbing can also be used on a path basis instead of just files.

## 5. Multiple globs

### Solve
**Flag** `pwn.college{szxZjozfsWXifegEFz0dV3PSw5I.0lM3kjNxwCMwEzNzEzW}`  
To solve  
`hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{szxZjozfsWXifegEFz0dV3PSw5I.0lM3kjNxwCMwEzNzEzW}`

### New Learnings
Multiple * globs can be used to match files.

## 6. Mixing globs

### Solve
**Flag** `pwn.college{0BxUtB4JWMrM7ibP4ngSvVuvb40.QX1IDO0wCMwEzNzEzW}`  
To solve  
`hacker@globbing~mixing-globs:~$  cd /challenge/files
/challenge/run [cep]*
You got it! Here is your flag!
pwn.college{0BxUtB4JWMrM7ibP4ngSvVuvb40.QX1IDO0wCMwEzNzEzW}`

### New Learnings
* cannot be used at the start.

## 7. Exclusionary globbing

### Solve
**Flag** `pwn.college{YUCSy3Y14oMCTBrPpSbDX2bRyVt.QX2IDO0wCMwEzNzEzW}`  
To solve  
` cd /challenge/files
/challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{YUCSy3Y14oMCTBrPpSbDX2bRyVt.QX2IDO0wCMwEzNzEzW}`

### New Learnings
In the glob [], if the first character is ! or ^ then the glob inverts. It matches characters that are not there is the bracket [].

## 8. Tab completion

### Solve
**Flag** `pwn.college{847pJJAC_1no9rReZcxtxOKJlCE.0FN0EzNxwCMwEzNzEzW}`  
To solve  
`hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{847pJJAC_1no9rReZcxtxOKJlCE.0FN0EzNxwCMwEzNzEzW}`

### New Learnings
Tab is a safer way to predict characters that the glob * which may lead to unintended files.

## 9. Multiple options for tab completion

### Solve
**Flag** `pwn.college{sE7A-UqBs1BmfRQ5mNHpaje9GSo.0lN0EzNxwCMwEzNzEzW}`  
To solve  
`hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwncollege-family      pwncollege-flyswatter
pwn-college            pwncollege-flag        pwncollege-hacking
pwn-the-planet         pwncollege-flamingo
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{sE7A-UqBs1BmfRQ5mNHpaje9GSo.0lN0EzNxwCMwEzNzEzW}`

### New Learnings
Pressing tab twice gives options if there are multiple files starting with same letters.

## 10. Tab completion on commands

### Solve
**Flag** `pwn.college{sDN9r4Jxp62r5iypG-K9dArW_Zb.0VN0EzNxwCMwEzNzEzW}`  
To solve  
`hacker@globbing~tab-completion-on-commands:~$ pwn
pwn               pwndbg            pwntools-gdb
pwncollege-10797  pwnstrip
hacker@globbing~tab-completion-on-commands:~$ pwncollege-10797
Correct! Here is your flag:
pwn.college{sDN9r4Jxp62r5iypG-K9dArW_Zb.0VN0EzNxwCMwEzNzEzW}`

### New Learnings
Tab can be used for commands as well as files.

