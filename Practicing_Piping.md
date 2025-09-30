# Practicing Piping

## 1. Redirecting Output

### Solve
**flag** `pwn.college{AcGyPnyIR9Y4ZsM__LKhbbaTjIe.QX0YTN0wCMwEzNzEzW}`  
To solve  
`hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{AcGyPnyIR9Y4ZsM__LKhbbaTjIe.QX0YTN0wCMwEzNzEzW}`

### New Learnings
'>' is used to redirect the output of the command to a particular file.  
Format: command argument > file

## 2. Redirecting more output

### Solve
**flag** ` pwn.college{8kcmboE_9jhCmTa0CDAlXH8H6zq.QX1YTN0wCMwEzNzEzW}`  
To solve  
`hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag
[HYPE] ONWARDS TO GREATNESS!
[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.
[TEST] You should have redirected my stdout to a file called myflag. Checking...
[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{8kcmboE_9jhCmTa0CDAlXH8H6zq.QX1YTN0wCMwEzNzEzW}`

## 3. Appending output

### Solve
**flag** `pwn.college{YC7zRelEJiZbKiKoWXZ7vdSH5Cv.QX3ATO0wCMwEzNzEzW}`
To solve  
`hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag
[HYPE] ONWARDS TO GREATNESS!
[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!
[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...
[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.
[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat myflag
[FLAG] Here is your flag:
[FLAG] pwn.college{8kcmboE_9jhCmTa0CDAlXH8H6zq.QX1YTN0wCMwEzNzEzW}
hacker@piping~appending-output:~$ cat the-flag
pwn.college{YC7zRelEJiZbKiKoWXZ7vdSH5Cv.QX3ATO0wCMwEzNzEzW}
If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!`

### New Learnings
Use >> (not >) to append command output so you don't overwrite earlier results.

## 4. Redirecting errors

### Solve
**flag** `

### New Learnings


## 5. Redirecting input

### Solve
**flag**

## 6. Grepping stored results

### Solve
**flag**

## 7. Grepping live output

### Solve
**flag**

## 8. Grepping errors

### Solve
**flag**

## 9. Filtering with grep -v

### Solve
**flag** `pwn.college{gEYfnhiuhtmNwMAhYnz7dbYSGfR.0FOxEzNxwCMwEzNzEzW}`  
To solve  
`hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{gEYfnhiuhtmNwMAhYnz7dbYSGfR.0FOxEzNxwCMwEzNzEzW}`

## 10. Duplicating piped data with tee

### Solve
**flag**

## 11. Process substitution for input

### Solve
**flag** `pwn.college{MgVg_dLrnbHKPSYx-UiXgKCdSyq.0lNwMDOxwCMwEzNzEzW}`  
To solve  
`hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
8a9
 pwn.college{MgVg_dLrnbHKPSYx-UiXgKCdSyq.0lNwMDOxwCMwEzNzEzW}`

## 12. Writing to multiple programs

### Solve
**flag** `pwn.college{Yxwu-SFXjSNIqEMt4jE7lalPJhV.QXwgDN1wCMwEzNzEzW}`  
To solve  
`hacker@piping~writing-to-multiple-programs:~$  /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
220167461297324903
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{Yxwu-SFXjSNIqEMt4jE7lalPJhV.QXwgDN1wCMwEzNzEzW}`

## 13. Split-piping stderr and stdout

### Solve
**flag** `pwn.college{ks7aoSWQfv3SnaSa5A_mgZrM0VM.QXxQDM2wCMwEzNzEzW}`  
To solve  
`hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{ks7aoSWQfv3SnaSa5A_mgZrM0VM.QXxQDM2wCMwEzNzEzW}` 

### New Learnings


## 14. Named pipes

### Solve
**flag**
