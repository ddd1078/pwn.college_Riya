# Chaining Commands

## 1. Chaining with Semicolons

### Solve
**Flag** `pwn.college{Qaun68M0133ro0IGpWmpHTmZAbG.QX1UDO0wCMwEzNzEzW}`

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{Qaun68M0133ro0IGpWmpHTmZAbG.QX1UDO0wCMwEzNzEzW}
```

## 2. Building on Success

### Solve
**Flag** `pwn.college{kncWxebYCj3t2wnuHYAxmQ8ifIM.0lM0MDOxwCMwEzNzEzW}`

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{kncWxebYCj3t2wnuHYAxmQ8ifIM.0lM0MDOxwCMwEzNzEzW}
```
## 3. Handling Failure
### Solve
**Flag** ` pwn.college{Qf4VTesYulFAPvAYV2CfCtCdg-c.01M0MDOxwCMwEzNzEzW}`

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{Qf4VTesYulFAPvAYV2CfCtCdg-c.01M0MDOxwCMwEzNzEzW}
```

## 4. Your First Shell Script

### Solve
**Flag** `pwn.college{UL_usCiPxVmJkoNd2odE6Y1t-nn.QXxcDO0wCMwEzNzEzW}`

```bash
hacker@chaining~your-first-shell-script:~$ cat > x.sh <<'EOF'
> /challenge/pwn
> /challenge/college
> EOF
hacker@chaining~your-first-shell-script:~$ cat x.sh
/challenge/pwn
/challenge/college
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{UL_usCiPxVmJkoNd2odE6Y1t-nn.QXxcDO0wCMwEzNzEzW}
```

## 5. Redirecting Script Output

### Solve
**Flag** `pwn.college{4s6ceaRWg8qGl4Zfq3_O5caeV1W.QX4ETO0wCMwEzNzEzW}`

```bash
hacker@chaining~redirecting-script-output:~$ cat > x.sh <<'EOF'
> /challenge/pwn
> /challenge/college
> EOF
hacker@chaining~redirecting-script-output:~$ cat x.sh
/challenge/pwn
/challenge/college
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{4s6ceaRWg8qGl4Zfq3_O5caeV1W.QX4ETO0wCMwEzNzEzW}
```

## 6. Executable shell scripts

### Solve
**Flag** `pwn.college{UxOPyaoYcnudnjhZNvfZjbGS0hp.QX0cjM1wCMwEzNzEzW}`

```bash
hacker@chaining~executable-shell-scripts:~$ cat > x.sh <<'EOF'
> script -q -c "/challenge/solve" /dev/null <<'INPUT'
> PWN
> COLLEGE
> INPUT
> EOF
hacker@chaining~executable-shell-scripts:~$ chmod +x x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
PWN
COLLEGE
Congratulations on your shell script execution! Your flag:
pwn.college{UxOPyaoYcnudnjhZNvfZjbGS0hp.QX0cjM1wCMwEzNzEzW}
```

## 7. Understanding Shebangs

### Solve
**Flag** ` pwn.college{EbxoYI8Yva8UBsOurxcl8TIEmEU.0VOzMDOxwCMwEzNzEzW}`

```bash
hacker@chaining~understanding-shebangs:~$ printf '%s\n' '#!/bin/bash' 'echo "hack the planet"' > /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ sed -n '1p' /home/hacker/solve.sh
#!/bin/bash
#!/bin/bash
hacker@chaining~understanding-shebangs:~$ cat -v /home/hacker/solve.sh      
#!/bin/bash
#!/bin/bash
echo "hack the planet"
hacker@chaining~understanding-shebangs:~$ /home/hacker/solve.sh
hack the planet
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{EbxoYI8Yva8UBsOurxcl8TIEmEU.0VOzMDOxwCMwEzNzEzW}
```

## 8. Scripting with arguments

### Solve
**Flag** `pwn.college{QKVsum9qM9NLzKhA7Xyl5Jzh_Su.0VNzMDOxwCMwEzNzEzW}`

```bash
hacker@chaining~scripting-with-arguments:~$ printf '%s\n' '#!/bin/bash' 'printf "%s %s\n" "$2" "$1"' > /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{QKVsum9qM9NLzKhA7Xyl5Jzh_Su.0VNzMDOxwCMwEzNzEzW}
```

## 9. Scripting with conditionals

### Solve
**Flag** `pwn.college{ohoG3qNGiRNiufMbFrHTUGl1LQK.0lNzMDOxwCMwEzNzEzW}`

```bash
hacker@chaining~scripting-with-conditionals:~$ printf '%s\n' '#!/bin/bash' 'if [ "$1" = "pwn" ]; then echo "college"; fi' > /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{ohoG3qNGiRNiufMbFrHTUGl1LQK.0lNzMDOxwCMwEzNzEzW}
```

## 10. Scripting with default cases

### Solve
**Flag** `pwn.college{oz5XKf1Wx1cKloyyTPQwcz9d1J9.01NzMDOxwCMwEzNzEzW}`

```bash
hacker@chaining~scripting-with-default-cases:~$ printf '%s\n' '#!/bin/bash' 'if [ "$1" = "pwn" ]; then echo "college"; else echo "nope"; fi' > /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{oz5XKf1Wx1cKloyyTPQwcz9d1J9.01NzMDOxwCMwEzNzEzW}
```

## 11. Scripting with multiple conditions

### Solve
**Flag** `pwn.college{8lTzoiQ_BrMXmrGGFRwYtUNets3.0FOzMDOxwCMwEzNzEzW}`

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ printf '%s\n' '#!/bin/bash' 'if [ "$1" = "hack" ]; then' '  echo "the planet"' 'elif [ "$1" = "pwn" ]; then' '  echo "college"' 'elif [ "$1" = "learn" ]; then' '  echo "linux"' 'else' '  echo "unknown"' 'fi' > /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{8lTzoiQ_BrMXmrGGFRwYtUNets3.0FOzMDOxwCMwEzNzEzW}
```

## 12. Reading shell scripts

### Solve
**Flag** `pwn.college{ACejPNy9MkI_EMlU2Ng8YcsIR6P.0lMwgDOxwCMwEzNzEzW}`

```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ printf 'hack the PLANET\n' | /challenge/run
CORRECT! Your flag:
pwn.college{ACejPNy9MkI_EMlU2Ng8YcsIR6P.0lMwgDOxwCMwEzNzEzW}
```
