# Pondering Paths

## The Root
Invoke pwn program using its absolute path

### Solve
**Flag** `pwn.college{EnbJfLWePbUxdcQuPa7z3Vx663M.QX4cTO0wCMwEzNzEzW}`
to solve `/pwn`

### New Learnings
Absolute paths start with a / which means its starts at the root.

## Program and absolute paths
Using absolute path to invoke program with 2 directories

### Solve
**Flag** `pwn.college{UowZVMqkjpE7TOHbI3PQ1mLjb2g.QX1QTN0wCMwEzNzEzW}`
to solve ` /challenge/run`

## Position thy self
Learning to navigate directories using cd (change directory)

### Solve
**Flag** `pwn.college{ckyMMwT4_Me-vroeuiqO4LVD0nH.QX2QTN0wCMwEzNzEzW}`
to solve 
` cd /etc/apt/sources.list.d`
` /challenge/run`

### New Learnings
cd is a command to change directories

## Position elsewhere
Execute program from a specific path using cd.

### Solve
**Flag** `pwn.college{Mm_g4SXyV8cv90jivynxyA-y-_I.QX3QTN0wCMwEzNzEzW}`
to solve
` cd /var/lib/apt/lists`
`/challenge/run`

## Position yet elsewhere
Execute program from a specific path using cd.

### Solve
**Flag** `pwn.college{MoaL1S8tDnmAgrEP0eoIhXKGZ_a.QX4QTN0wCMwEzNzEzW}`
to solve
`cd  /home/hacker`
` cd /sys/kernel`
`/challenge/run`

## implicit relative paths, from /
Using a relative path to execute a program

### Solve
**Flag** `pwn.college{A4y0sTtfuKP4ixSSPHc6Vd7a0t7.QX5QTN0wCMwEzNzEzW}`
to solve
`cd /`
` challenge/run`

### New Learnings
A relative path is a path that does not start with the root that is /.
It is interpreted relative to the current working directory (cwd).

## explicit relative paths, from /

### Solve
**Flag** `pwn.college{4dTotZT0S59QpsH6OlCXkFl-eOJ.QXwUTN0wCMwEzNzEzW}`
to solve
`cd /`
`./challenge/run`

### New Learnings
'.' represents current directory.

## implicit relative path

### Solve
**Flag** `pwn.college{IHsbCRyTKgm_bFaYtEVeynhya9G.QXxUTN0wCMwEzNzEzW}`
to solve 
`cd /challenge`
`./run`

## home sweet home

### Solve
**Flag** `







