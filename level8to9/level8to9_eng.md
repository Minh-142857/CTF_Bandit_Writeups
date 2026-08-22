# OBJECTIVE
In the "data.txt" file, get the password that appears EXACTLY ONCE.

# SOLUTION
Use this command to show all files and directories in the current directory on the server:
```bash
ls -al
```

The terminal will return the following:

![Terminal after the ls -al command](./images/ls_al.PNG)

Similar to the previous level, if we use `cat data.txt`, the terminal will get flooded with text. Instead, we can use the `uniq` command to skip repeated lines. With this level, the `uniq` command looks like this:
```bash
uniq --unique data.txt # The "--unique" option outputs only non-repeated lines
```

However, it has a big problem. If we execute this command, the terminal will return the following:

![Terminal if we use the above command](./images/uniq_wrong.PNG)

Reason: The `uniq` command ONLY CHECKS ADJACENT LINES. As seen earlier in `data.txt`, lines appear in random order. 

To deal with this, we need to sort the lines (so that repeated lines become adjacent to each other, allowing the `uniq` command to skip them). We have to add the `sort` command (similar to `std::sort` in `C++`) before the `uniq` command like this:
```bash
sort data.txt | uniq --unique
```

!["Level completed" screen](./images/objective.PNG)

# PASSWORD
```
EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl
```
 