# OBJECTIVE
Get the password in the file that has these properties:
- Human-readable
- Size: 1033 bytes
- Not executable

# SOLUTION
Similar to the previous level, we need to access the "inhere" directory. So, we can use the `cd` command to access the directory like this:
```bash
cd ./inhere
```

Then, use this command to show all files in the directory:
```bash
ls -al
```

![Terminal after the ls -al command (In "inhere" directory)](./images/ls_al_inhere.PNG) 

Even though we can `cat` all files like the previous level, IT WILL BE TIME-CONSUMING. Instead, since we have the specific properties, we can use the `find` command like this:
```bash
find -readable -size 1033c -not -executable
```

Command explanation:
- `-readable`: Find human-readable files
- `-size 1033c`: Find files that have the exact size (by default, this option searches using `b` (512-byte blocks), so we need to find by `c` (bytes)) 
- `-not -executable`: Find not executable files (put the option `-not` in front to invert the search condition)

After that, the terminal will output this following: 

![Terminal after the find command](./images/find.PNG)

We found that file `./maybehere07/.file2` is the only file that satisfies all of the above properties. Finally, we just need to `cat` this file to get the password. 

!["Level completed" screen](./images/objective.PNG)

# PASSWORD
```
pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
```
 