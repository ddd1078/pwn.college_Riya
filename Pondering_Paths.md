# Pondering Paths

## The Root
Invoke pwn program using its absolute path

### Solve
**Flag** `pwn.college{EnbJfLWePbUxdcQuPa7z3Vx663M.QX4cTO0wCMwEzNzEzW}`  
To solve  
```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{EnbJfLWePbUxdcQuPa7z3Vx663M.QX4cTO0wCMwEzNzEzW}
```

### New Learnings
Absolute paths start with a / which means its starts at the root.

## Program and absolute paths
Using absolute path to invoke program with 2 directories

### Solve
**Flag** `pwn.college{UowZVMqkjpE7TOHbI3PQ1mLjb2g.QX1QTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{UowZVMqkjpE7TOHbI3PQ1mLjb2g.QX1QTN0wCMwEzNzEzW}
```

## Position thy self
Learning to navigate directories using cd (change directory)

### Solve
**Flag** `pwn.college{ckyMMwT4_Me-vroeuiqO4LVD0nH.QX2QTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /etc/apt/sources.list.d directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /etc/apt/sources.list.d directory
bash: cd: too many arguments
hacker@paths~position-thy-self:~$  /etc/apt/sources.list.d directory
bash: /etc/apt/sources.list.d: Is a directory
hacker@paths~position-thy-self:~$ cd  /etc/apt/sources.list.d
hacker@paths~position-thy-self:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{ckyMMwT4_Me-vroeuiqO4LVD0nH.QX2QTN0wCMwEzNzEzW}
```

### New Learnings
cd is a command to change directories

## Position elsewhere
Execute program from a specific path using cd.

### Solve
**Flag** `pwn.college{Mm_g4SXyV8cv90jivynxyA-y-_I.QX3QTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var/lib/apt/lists directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd  /var/lib/apt/lists
hacker@paths~position-elsewhere:/var/lib/apt/lists$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Mm_g4SXyV8cv90jivynxyA-y-_I.QX3QTN0wCMwEzNzEzW}
```


## Position yet elsewhere
Execute program from a specific path using cd.

### Solve
**Flag** `pwn.college{MoaL1S8tDnmAgrEP0eoIhXKGZ_a.QX4QTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /sys/kernel directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ pwd
/home/hacker
hacker@paths~position-yet-elsewhere:~$ cd /sys/kernel
hacker@paths~position-yet-elsewhere:/sys/kernel$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{MoaL1S8tDnmAgrEP0eoIhXKGZ_a.QX4QTN0wCMwEzNzEzW}
```

## implicit relative paths, from /
Using a relative path to execute a program

### Solve
**Flag** `pwn.college{A4y0sTtfuKP4ixSSPHc6Vd7a0t7.QX5QTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{A4y0sTtfuKP4ixSSPHc6Vd7a0t7.QX5QTN0wCMwEzNzEzW}
```

### New Learnings
A relative path is a path that does not start with the root that is /.
It is interpreted relative to the current working directory (cwd).

## explicit relative paths, from /

### Solve
**Flag** `pwn.college{4dTotZT0S59QpsH6OlCXkFl-eOJ.QXwUTN0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{4dTotZT0S59QpsH6OlCXkFl-eOJ.QXwUTN0wCMwEzNzEzW}
```

### New Learnings
'.' represents current directory.

## implicit relative path

### Solve
**Flag** `pwn.college{IHsbCRyTKgm_bFaYtEVeynhya9G.QXxUTN0wCMwEzNzEzW}`  
to solve  
```hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
```

## home sweet home

### Solve
**Flag** `pwn.college{IqTRoEg8329Mr-MWEOicQStop6V.QXzMDO0wCMwEzNzEzW}`  
to solve  
```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/x
Writing the file to /home/hacker/x!
... and reading it back to you:
pwn.college{IqTRoEg8329Mr-MWEOicQStop6V.QXzMDO0wCMwEzNzEzW}
```

### New Learnings
The home directory is where users store most of their personal files.
cd will use home directory as the default destination.






