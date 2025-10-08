#  Data Manipulation

## 1. Translating Characters

### Solve
**Flag** `pwn.college{42epPjZK6-ETkg0YKjA87Mjkgk9.01MxEzNxwCMwEzNzEzW}`  

```bash
hacker@data~translating-characters:~$ /challenge/run
Your case-swapped flag:
PWN.COLLEGE{42EPpJzk6-etKG0ykJa87mJKGK9.01mXeZnXWcmWeZnZeZw}

hacker@data~translating-characters:~$ echo PWN.COLLEGE{42EPpJzk6-etKG0ykJa87mJKGK9.01mXeZnXWcmWeZnZeZw} | tr 'A-Za-z' 'a-zA-Z'
pwn.college{42epPjZK6-ETkg0YKjA87Mjkgk9.01MxEzNxwCMwEzNzEzW}
```
### New Learnings
tr command is used to modify the characters by changing the characters in the first argument to the characters in the second argument.  
Format:  
echo datatobemodified | tr arg1 arg2


## 2. Deleting Characters

### Solve
**Flag** `pwn.college{g-3Lp6T0PMeEzPECLS5xEOQpwZL.0FNxEzNxwCMwEzNzEzW}`  

```bash
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p^%w^%n^%.^%c^%o^%l^%l^e^%g^e^{^g^-%3L^%p^%6^T%0^%PM^%e^%E^z%P^E^C^L%S^%5^%x%E^%O^%Qp^%w^%Z^L^%.^0^F%N%x^E%z^N^x^%w%C^%M^%w%Ez^%Nz^E%z^%W^%}^%^%
hacker@data~deleting-characters:~$ echo p^%w^%n^%.^%c^%o^%l^%l^e^%g^e^{^g^-%hacker@data~deleting-characters:~$ echo p^%w^%n^%.^%c^%o^%l^%l^e^%g^e^{^g^-%3L^%p^%6^T%0^%PM^%e^%E^z%P^E^C^L%S^%5^%x%E^%O^%Qp^%w^%Z^L^%.^0^F%N%x^E%z^N^x^%w%C^%M^%w%Ez^%Nz^E%z^%W^%}^%^% | tr -d ^%
pwn.college{g-3Lp6T0PMeEzPECLS5xEOQpwZL.0FNxEzNxwCMwEzNzEzW}
hacker@data~deleting-characters:~$ pwn.college{g-3Lp6T0PMeEzPECLS5xEOQpwZL.0FNxEzNxwCMwEzNzEzW}
```

### New Learnings
'tr -d arg' is used to delete the characters given in the arg.

## 3. Deleting newlines

### Solve
**Flag** `pwn.college{YFBmFlh7IRfRV0rgQfsTUwFBHDH.0VNxEzNxwCMwEzNzEzW}`

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{YFBmFlh7IRfRV0rgQfsTUwFBHDH.0VNxEzNxwCMwEzNzEzW}
```

### New Learnings
"\n" is used for new line. This can be used with tr -d to delete new lines.
"\n" has to be put in double quotes to prevent the shell interpreter from interpreting it.

## 4. Extracting the first lines with head

### Solve
**Flag** `pwn.college{8o_TboOgzwGNf1AM57gpk0FLsF_.0lNxEzNxwCMwEzNzEzW}`

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{8o_TboOgzwGNf1AM57gpk0FLsF_.0lNxEzNxwCMwEzNzEzW}
```

### New Learnings
The head command is used to display the first few lines of its input (default is 10 lines). Using 'head -n num' displays num lines. 

## 5. Extracting specific section of text

### Solve
**Flag** `pwn.college{8JP9WuV8qUpfddvtJyub_Fv7nYu.01NxEzNxwCMwEzNzEzW}`

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr  -d "\n"
pwn.college{8JP9WuV8qUpfddvtJyub_Fv7nYu.01NxEzNxwCMwEzNzEzW}
```

### New Learnings
The cut command is used to extact specific columns of data.  
Format:  
cut -d " " -f column_to_be_cut_number

## 6. Sorting data

### Solve
**Flag** `pwn.college{0MT9Z6nz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwCMwEzNzEzW}`
I sorted it reverse alphabetically so that the first flag would be the correct one.  

```bash
hacker@data~sorting-data:~$ sort -r /challenge/flags.txt
pwn.college{0MT9Z6nz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwCMwEzNzEzW}
pwn.college{0MT9Z6nz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwCMwDzNzEzW}
pwn.college{0MT9Z6nz6hgsGn-i7GN6lzEg9Te.0FM0MDNxwCMwEzNzEzW}
pwn.college{0MT9Z6nz6hgsGn-i7GN6lzEg9Te.0FM0LCOxwCMwEzNzEzW}
pwn.college{0MT9Z6nz6hgsGn-i7GN6lzEg8Te.0FM0MDOxwCMwEzNzEzW}
pwn.college{0MT9Z6nz6hgsGn-i7GN6lzDg9Te.0FM0MDOxwBLvEzNyEzW}
pwn.college{0MT9Z6nz6hgsGn-i7GN6kzEg9Te.0FM0MDOxwCMwEzNzEzW}
pwn.college{0MT9Z6nz6hgsGn-h7GN6lzEg9Te.0EM0MCOwwCMwEyNzEzW}
pwn.college{0MT9Z6nz5hgsGn-i7GN6lzEg9Te.0FM0LDOxwCMvEyNzEzW}
pwn.college{0MT9Z5mz6hgrGn-i7GN6lzEf9Te.0FM0MDOxwCMwDzNzEzW}
pwn.college{0MT8Z6nz6hfsGn-i7GM6lzEg9Te.0FM0LDOxwCMwDzMzEzW}
pwn.college{0MS9Z6nz6hgrGn-i7GN6lzDf8Se.0FL0LDNxwCLwEzNyEzW}
pwn.college{0MS9Z6ny5hfsGn-i7GN6lzEf9Se.0FM0LCOxwBMwDzNzEzV}
pwn.college{0MS9Z5nz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwBMwEzNzEzW}
pwn.college{0LT9Z6nz6gfrFn-i7GN6kyEg9Te.0FM0MDOxwCMwEzMyEzW}
pwn.college{0LT9Y6ny5hfsFn-i7GM5lzDf9Td.0FL0MDNxvCMvEzNzDyW}
pwn.collegd{0MT9Z6nz6hgsGn-i6GM6kzEg9Se.0FM0MDOxvCMwEzMzDzW}
pwn.collegd{0MT8Z6nz6hgsGn-i7GN6lzEf8Te.0FM0MDOxwCMwDyNzEzV}
pwn.collegd{0LT8Z6my6ggrFm-i6GN6lyEg8Sd.0EM0MCOxwCMwEzMyEyW}
pwn.collefe{0MT9Y6ny6hfsGn-i6GN6kzEf8Te.0EM0MDOxwCMvEzNzDyW}
pwn.collefe{0LT9Z6mz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwCLwDzNzEzW}
pwn.colldge{0MT9Z6nz6hgsGn-i7GN6lzEg8Te.0FM0MCOwwCMwDzNzEzW}
pwn.colldge{0MT9Z6nz6hgsGn-i7GN6lzEf9Te.0FM0LDOxwCMwEzNzEzW}
pwn.colkege{0MT9Z6nz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwCMwEzNzEzW}
pwn.colkege{0MT9Z6mz6gfsFn-i7GN6kzEf9Te.0FL0LDNxwBMvDzMyDyW}
pwn.coklege{0MT9Z5nz6hgsGn-h6GN6lyDg9Te.0FM0MDOxwCMwEzNyEzW}
pwn.coklege{0LT9Z6nz6hfsGm-i6GM6lzDg9Te.0FM0MCOxwCMwEyNzDzW}
pwn.cnllege{0MT8Z6nz6hgsGn-i7GN6lzEg9Te.0FM0MDOxwCMwEzNzEzW}
pwn.cnllegd{0MT9Z6nz6hgsFn-i7GN6lzEg9Te.0FM0MDOxwCMwEzMzEyW}
pwn.cnlldge{0MT9Y6nz6hgsGn-i7GN6lzDg9Te.0FM0MDOxwCMvEzNzEzW}
pwn.cnlldfe{0MS8Z5nz6ggsGm-i7GN6lyEg8Te.0FM0LDOwwCMwEyMzEyV}
pwn.cnlkdge{0MT9Z6my6hgsGm-h7GN5lzEg9Td.0EM0LDNxvBMwEzNzDzW}
pwn.cnlkdgd{0LS8Z5nz6hgsGn-h6FM5lzDg9Td.0FL0MDNxwCMvDzNyEyV}
pwn.cnlkdfe{0MT9Z6nz6hgrFm-h7GN5kyEg8Td.0EM0MDOxvCLwDzMzDzW}
pwn.bollegd{0MT8Z6mz6hfsGn-i6GM5kzEf9Te.0EM0MDOxvBMwDyMzDzV}
pwn.bollegd{0LT9Z6nz6hgsGn-i7GN6lzEg9Td.0FM0MDOxwCMwDzNzEzW}
pwn.bollegd{0LS9Z6ny6hgrFm-i6GN6lyDf9Te.0FM0MDNxvCLvEzMyEyW}
pwn.bollefe{0LT9Z6nz6hgsGn-i7FM5lzEg9Te.0FM0MDOxwBMwDzMzEzV}
pwn.boklegd{0MT9Z6ny5hgsGn-h7GN5lzDg9Td.0EL0MDNxwCMwEyNyDzW}
pwn.boklegd{0LT9Z5my6hfrFn-i6GN6lzDg9Se.0FL0MCOxvCMwEzNzDyV}
pwn.bokldge{0MT9Z5nz6gfrGn-i6FN6lzEg9Te.0EL0MDNxwBMwEyMyEzV}
pwn.bnlkege{0LT9Y6nz6hgsFn-i7FM6kyEg8Td.0FM0MDNxwCMwEyNyDzW}
pwm.college{0MT9Z6nz5hfrGn-i7GN5lzEf9Td.0FL0MDOxwCMvEzNzEyW}
pwm.cokldge{0MS9Y6nz6ggsGn-i7FN6lzEg9Te.0FM0MDOxwCMwEyMyEzW}
pwm.cnllege{0MT9Y5nz6hgrGn-i6GM5kzEf9Te.0FL0MCOwwCMvDzNzEzV}
pwm.cnllege{0MS9Z6nz6hgsGn-h7GN6lzEg9Te.0EL0MCNwwBMwEzNzDzW}
pwm.cnllege{0LT8Z6mz5hfsGn-h6GN5kzEg9Te.0EM0LDOwwCMwDyNzEzW}
pwm.cnllegd{0MT9Y5mz6hfrGn-i7GM5lyEf9Td.0FM0MDOxwCMwEzMyDzV}
pwm.cnllegd{0LT9Y6ny6ggrFn-i7GN6lyEf8Td.0FM0LDOwwCLwEzNyEzW}
pwm.cnllefe{0MT9Z6nz6ggsFn-h6GN5lyEg9Td.0FM0MDOxwCMvEyNyEzW}
pwm.cnllefe{0LT8Z6ny5hfsGn-i7GN5lzEg9Te.0FM0LDOxwCMwDzNzEzW}
pwm.cnlldge{0MT9Z6mz6hfsFn-i6GN5kyEg9Sd.0FM0MDOxwBLwEzNzEzW}
pwm.cnlkdfe{0LS9Y6my5ggsGn-h6GN5lzEg9Te.0EM0LDOxvCMwDzMzEzW}
pwm.bollege{0MT9Z6nz5hfrFn-i6GM5kzDf8Se.0FM0MDNxwCLvEzNyEzV}
pwm.bollege{0MT8Y6nz6hgsGn-h7GN6lzDg9Te.0FM0LDNxwCMwEzNzDzW}
pwm.bollege{0LS9Y6nz6hgrFn-h7GM5lzEg9Te.0FL0LDOxwCLwEyNyEzW}
pwm.bollegd{0MS9Z6ny5hgrFn-i6GN5lzEg9Se.0FM0MCOwwCLvDzNzDyW}
pwm.bokkdge{0MS9Y5nz6ggrGm-h7FN6lzEg9Te.0EM0MDOxvBMvEzNzEzW}
pwm.bnllege{0MT9Z6nz6hgsGm-i7FN6lzEf8Te.0EM0MDOxwBMwDzNzEzV}
pvn.college{0MT8Z6nz6hgsGn-i7GN6kzEg9Te.0FM0MCOwwCMwEyNzEyW}
pvn.college{0MT8Z6nz6hgsGn-i7GN5lzEg9Te.0FM0MDOxvCMwEzNzEzW}
pvn.colldgd{0LT9Y6mz5hgsFn-i6GN6kzEg9Sd.0EM0MDOxwCMwEyNzEyV}
pvn.colkdge{0MS8Z5nz5hgsGn-i7GN6lzDg8Te.0FM0MCOwvBLvEzNzEzV}
pvn.cokldgd{0MT9Z6nz6hgsGn-i7GM5kyEf9Se.0EM0MCOxvCMwEzNzEzV}
pvn.cokldfe{0MT9Z6nz5hgrGn-i7GN5kzEg9Te.0FM0MCNwwCLvEzNzDyV}
pvn.cokkdge{0MT9Y6mz5hfrGn-i7GN6lzEg9Te.0FL0MDOwwCMwEyNyEyW}
pvn.cnllege{0MS9Z5ny6hgsGm-h7GM6lyDg9Sd.0FM0MDOwwCMvEzNyDyW}
pvn.cnllegd{0LS8Z6nz6ggsGn-i6FN6lzEg9Te.0EM0MCOxwCMwEzNzEzW}
pvn.cnllefe{0LS8Z6my6hgsGn-i6GM6lzDf8Td.0FM0LCOxwCLwEzNyEzW}
pvn.cnlkegd{0MT9Y6nz6hfsFm-i6GN6lzEg9Te.0FM0MDOxvBMvEzMyDzW}
pvn.cnlkdfd{0MT9Z6nz6gfsGn-h7FM6lzEg8Se.0FM0LDOwvBMvEzNzEyW}
pvn.cnkldge{0MS8Z5ny5ggsGn-h7GM5kyDg8Te.0EM0LDOxwCMwEyNzEzW}
pvn.cnkldge{0LT9Z6nz6hgrGn-i7GN6lyEg9Te.0EM0LDOxwCMwEzNyEzV}
pvn.cnkldgd{0LS9Z5mz6hgsGm-i6GN6lzDf9Td.0FM0MDOxwCMvEyNyDzW}
pvn.bollege{0MT9Z6nz5hgrGn-h7GN6lzEg9Te.0FM0MDOxwCMvEzNzEzW}
pvn.boklege{0MT8Z5nz6hgsGn-i7FN6lyEg9Te.0FM0MDOxvCMvEyNzEzW}
pvn.bokkege{0MT8Y5ny6hgsFn-i6GN5lyEg9Se.0FL0LDNxwCMvDyNzEyW}
pvm.cnlkefe{0LT9Y6ny5ggrFn-i7GN6lzEg9Te.0EM0MDNxvCMvEyMzEyW}
pvm.bolldge{0MT8Y6my5ggsGn-h7GM6kzEf8Te.0FM0MCOxwCMvEyNzDzW}
pvm.boklege{0MT8Y5nz6hgrGm-i7FN6kzEf9Te.0FM0MDNxwBMwEzNzEyW}
own.collegd{0MS9Z6nz6hgsFn-h6FM6lzEg9Te.0EM0MDOwwBLvDzMzEzW}
own.collefe{0MT9Z6nz6hgrGn-i6GN6lyEg9Te.0FM0MDOwwBLwEzNzDzW}
own.collefe{0MS8Z5nz6hfrGn-h6FN5kyEg8Se.0FM0MCNwvCMwDzMzEyV}
own.colldge{0MT9Y6ny5hgsGm-i7GM5lyEg9Te.0FM0MDNxwBLwEzMzEyV}
own.coklege{0MT9Z6nz5hgsGn-i7GN6lzEg9Te.0FM0MCOxwCMwEzNzDzW}
own.cnllege{0MT9Z6ny6hgsGn-i7GN6lzEg8Te.0EM0MCOxwCMwEzNzEzW}
own.cnlkege{0LT9Y6nz6hfsGm-h7FN6lyDf9Td.0FM0MDNxwBLvEzNyEzW}
own.cnklege{0MS9Y5nz6ggsFn-h7GN5lzEf9Sd.0FM0LDOxwCLwEyMzEyV}
own.cnkkegd{0LT9Y5nz6hgsGn-i7GN5lyDf9Te.0FM0MDNxvCLvDyNyEzW}
own.bollefe{0MT8Z5ny6hfsGn-h6FN5lzEf9Sd.0FL0MCOxwBLvEzMyEzW}
own.bokkdge{0MS8Z5ny6hgrGn-h7GN5lyEf9Td.0EL0LCOxwCLwEyNzEzW}
own.bnlldfd{0MS9Z6nz6hfsGn-i6GN5lzDf9Te.0EM0LCOxvCLwEzMyEyW}
own.bnkkege{0MT9Y6ny5ggrGn-h7GN6lzEf8Te.0EM0LCOxwCMwEzNyEzV}
owm.college{0MT8Z6nz6hfrFm-i7GM6kzEg8Te.0FM0LDOxwBMwEzNyEzW}
owm.bollegd{0MT9Z6nz6hgsGn-i7GN6kzEg9Te.0FM0MDOxwBMvEzNzEzV}
owm.bolldfe{0LS9Y6mz5hfrGn-h7FM6lzEg8Td.0FM0LDNxvCMwEzNzDyW}
ovn.collefe{0MT9Z5nz6hgsGn-h7GN6lyEg9Te.0FL0LDNxvCLvEzNzEyW}
ovn.colkefe{0MT9Z5nz5hgrFm-h7FM6lyDg9Se.0EM0MDOxwBMwEzMzDyW}
ovn.cnllefe{0MT9Y6nz6hgsGn-i7GN6lzEg9Td.0FM0MCOxwCMwEzNzEyW}
ovn.bolkegd{0LS9Y6mz6hgsGm-h7FN6lzEg8Se.0EM0LDOxvBLwEzNzEzV}
ovm.bnlkdfe{0MS8Z6nz5ggsGm-i6FM6lyEg9Te.0FL0LDOwvCMwDzNzEzV}
```

### New Learnings
The sort command helps to sort the files to orgnaize data.  
Arguments that can be used after sort:  
-r: reverse order (Z to A)  
-n: numeric sort (for numbers)   
-u: unique lines only (remove duplicates)  
-R: random order
