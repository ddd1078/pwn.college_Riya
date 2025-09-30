# Shell Variables
## 1. Printing Variables

### Solve

**flag** `pwn.college{Yia0J_VzEN_qt48guWIjmWSb_OC.QX3UTN0wCMwEzNzEzW}`  
To solve  
`hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{Yia0J_VzEN_qt48guWIjmWSb_OC.QX3UTN0wCMwEzNzEzW}`

### New Learnings
Variables can be printed with echo by prehending the variable name with $.

## 2. Setting Variables

### Solve
**flag** `pwn.college{A0AyA5Xi6wLutwIreINiFjKgE_Q.QX5UTN0wCMwEzNzEzW}`  
To solve  
`hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{A0AyA5Xi6wLutwIreINiFjKgE_Q.QX5UTN0wCMwEzNzEzW}`

### New Learnings
To write values to variables:  
VAR=value  
Do this without any spaces in the middle or $.

## 3. Multi-word Variables

### Solve
**flag** `pwn.college{gTaMzsIXCoxykDB3Ak-5p3XqyFi.QXwYTN0wCMwEzNzEzW}`  
To solve  
`hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{gTaMzsIXCoxykDB3Ak-5p3XqyFi.QXwYTN0wCMwEzNzEzW}`

### New Learnings
If there are spaces in the variable assignment put the variable assignment in "" so that the shell does not interpret the text after space as a command.

## 4. Exporting Variables

### Solve
**flag** `pwn.college{0pT9Q23fAD2uGspyts7UUWl4iA1.QXyYTN0wCMwEzNzEzW}`  
To solve  
`hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{0pT9Q23fAD2uGspyts7UUWl4iA1.QXyYTN0wCMwEzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!`

### New Learnings
By default, variables set in a shell session are local to that shell process and the other commands would not inherit them. To use the same variables in other commands, we can export variables:  
export var  

## 5. Printing Exported Variables

### Solve
**flag** `pwn.college{k9r51o1y2MDhgzohqmy5yHUPldz.QX4UTN0wCMwEzNzEzW}`  
To solve  
`hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=98117893e803d00d3853d22b606f33a63a12cc22c4a38295bea6fd82c8ab3596
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{k9r51o1y2MDhgzohqmy5yHUPldz.QX4UTN0wCMwEzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env`

### New Learnings
The env command prints out every exported variable in the shell.

## 6. Storing Command Output

### Solve
**flag** `pwn.college{oGwQfClUhMRBeUrV-udTl5AgHVV.QX1cDN1wCMwEzNzEzW}`  
To solve  
`hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{oGwQfClUhMRBeUrV-udTl5AgHVV.QX1cDN1wCMwEzNzEzW}`

### New Learnings
Command substitution helps to store the output of some command into a variable. Format:  
VAR=$(command)  
echo $VAR

## 7. Reading Output

### Solve
**flag** `pwn.college{8oPrj_wgSVmYtDXibf04vNgklvW.QX4cTN0wCMwEzNzEzW}`
To solve  
`hacker@variables~reading-input:~$ echo PWN=COLLEGE
PWN=COLLEGE
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8oPrj_wgSVmYtDXibf04vNgklvW.QX4cTN0wCMwEzNzEzW}`

### New Learnings
The read command lets the user store input into a variable directly.

## 8. Reading Files

### Solve
**flag** `pwn.college{sSgulQNa2HiIsdinbL-nXGlsK10.QXwIDO0wCMwEzNzEzW}`  
To solve  
`hacker@variables~reading-files:~$ read PWN </challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{sSgulQNa2HiIsdinbL-nXGlsK10.QXwIDO0wCMwEzNzEzW}`
