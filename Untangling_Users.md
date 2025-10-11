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

## 3. Cracking passwords

### Solve
**Flag** 

### New Learnings

## 4.  Using sudo

### Solve
**Flag** 

### New Learnings
