# Digesting Documentation

## 1. Learning From Documentation
Learning documentation.

### Solve
**Flag** `pwn.college{IJ14RfTP_Dzjt4UL1ZA9RuVs9Dc.QX0ITO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.colllege{IJ14RfTP_Dzjt4UL1ZA9RuVs9Dc.QX0ITO0wCMwEzNzEzW}
```

## 2. Learning Complex Usage
Learning complex usage of documentation.

### Solve
**FLag** `pwn.college{ABaRm7wszEdPYBJ0nWiIQ5ULWOi.QX1ITO0wCMwEzNzEzW}`
to solve  
```bash
hacker@man~learning-complex-usage:~$ cd /
hacker@man~learning-complex-usage:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{ABaRm7wszEdPYBJ0nWiIQ5ULWOi.QX1ITO0wCMwEzNzEzW}
```

## 3. Reading Manuals
Learning to use man command.

### Solve
**FLag** ` pwn.college{sKuvSKAunzlNaBBnQ4A26QKeVs-.QX0EDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --suvunz 426
Correct usage! Your flag: pwn.college{sKuvSKAunzlNaBBnQ4A26QKeVs-.QX0EDO0wCMwEzNzEzW}
```

### New Learnings
The man command will display the manual of the argument passed.
The manual comprises of the name, synopsis, description, see also etc.


## 4. Searching Manuals

### Solve
**FLag** `pwn.college{UhjDJr8Vn8RQwN-jdlaU51TaNpE.QX1EDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge  --zhunsuu
Initializing...
Correct usage! Your flag: pwn.college{UhjDJr8Vn8RQwN-jdlaU51TaNpE.QX1EDO0wCMwEzNzEzW}
```

### New Learnings
Manuals can be searched using / and searched backward using ? within the manual.
'n'gives next result whereas 'N'gives previous result.

## 5. Searching For Manuals

### Solve
**FLag** `pwn.college{AcpEleqrRM8iWtLo8I-bMciiln_.QX2EDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
cpleqritob (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man cpleqritob
hacker@man~searching-for-manuals:~$ /challenge/challenge --cpleqr 882
Correct usage! Your flag: pwn.college{AcpEleqrRM8iWtLo8I-bMciiln_.QX2EDO0wCMwEzNzEzW}
```
### New Learnings
'man -k argument' searches the manual database for that argument and is used to find hidden man pages.

## 6. Helpful Programs
Learning to use --help.

### Solve
**FLag** `pwn.college{Y9Jvot7tRNmOSzkehdKbq0VEZl0.QX3IDO0wCMwEzNzEzW}`  
To solve  
```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]
optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to
                        give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge --print-value
The secret value is: 970
hacker@man~helpful-programs:~$ /challenge/challenge -g 970
Correct usage! Your flag: pwn.college{Y9Jvot7tRNmOSzkehdKbq0VEZl0.QX3IDO0wCMwEzNzEzW}
```

### New Learnings
Some programs do not have a man page but --help can be used sometimes to know how to run them.

## 7. Help for Builtins

### Solve
**FLag** `pwn.college{Ir2MjJb0NBe5KggCPwZ4U-eUb5i.QX0ETO0wCMwEzNzEzW}`  
To solve  
```bash
hacker@man~help-for-builtins:~$ help
GNU bash, version 5.2.37(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.
A star (*) next to a name means that the command is disabled.
 job_spec [&]                          history [-c] [-d offset] [n] or hi>
 (( expression ))                      if COMMANDS; then COMMANDS; [ elif>
 . filename [arguments]                jobs [-lnprs] [jobspec ...] or job>
 :                                     kill [-s sigspec | -n signum | -si>
 [ arg... ]                            let arg [arg ...]
 [[ expression ]]                      local [option] name[=value] ...
 alias [-p] [name[=value] ... ]        logout [n]
 bg [job_spec ...]                     mapfile [-d delim] [-n count] [-O >
 bind [-lpsvPSVX] [-m keymap] [-f fi>  popd [-n] [+N | -N]
 break [n]                             printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]     pushd [-n] [+N | -N | dir]
 caller [expr]                         pwd [-LP]
 case WORD in [PATTERN [| PATTERN]..>  read [-ers] [-a array] [-d delim] >
 cd [-L|[-P [-e]] [-@]] [dir]          readarray [-d delim] [-n count] [->
 challenge [--fortune] [--version] [>  readonly [-aAf] [name[=value] ...]>
 command [-pVv] command [arg ...]      return [n]
 compgen [-abcdefgjksuv] [-o option]>  select NAME [in WORDS ... ;] do CO>
 complete [-abcdefgjksuv] [-pr] [-DE>  set [-abefhkmnptuvxBCEHPT] [-o opt>
 compopt [-o|+o option] [-DEI] [name>  shift [n]
 continue [n]                          shopt [-pqsu] [-o] [optname ...]
 coproc [NAME] command [redirections>  source filename [arguments]
 declare [-aAfFgiIlnrtux] [name[=val>  suspend [-f]
 dirs [-clpv] [+N] [-N]                test [expr]
 disown [-h] [-ar] [jobspec ... | pi>  time [-p] pipeline
 echo [-neE] [arg ...]                 times
 enable [-a] [-dnps] [-f filename] [>  trap [-lp] [[arg] signal_spec ...]
 eval [arg ...]                        true
 exec [-cl] [-a name] [command [argu>  type [-afptP] name [name ...]
 exit [n]                              typeset [-aAfFgiIlnrtux] name[=val>
 export [-fn] [name[=value] ...] or >  ulimit [-SHabcdefiklmnpqrstuvxPRT]>
 false                                 umask [-p] [-S] [mode]
 fc [-e ename] [-lnr] [first] [last]>  unalias [-a] name [name ...]
 fg [job_spec]                         unset [-f] [-v] [-n] [name ...]
 for NAME [in WORDS ... ] ; do COMMA>  until COMMANDS; do COMMANDS-2; do>
 for (( exp1; exp2; exp3 )); do COMM>  variables - Names and meanings of >
 function name { COMMANDS ; } or nam>  wait [-fn] [-p var] [id ...]
 getopts optstring name [arg ...]      while COMMANDS; do COMMANDS-2; do>
 hash [-lr] [-p pathname] [-dt] [nam>  { COMMANDS ; }
 help [-dms] [pattern ...]
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct
    You must be sure to provide the right value to --secret. That value
    is "Ir2MjJb0".
hacker@man~help-for-builtins:~$ challenge --secret Ir2MjJb0
Correct! Here is your flag!
pwn.college{Ir2MjJb0NBe5KggCPwZ4U-eUb5i.QX0ETO0wCMwEzNzEzW}
```

### New Learnings
Builtins are programs that are built into the shelfs itself instead of having a manual. Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. The command help can be used to get a list of shell builtins.
