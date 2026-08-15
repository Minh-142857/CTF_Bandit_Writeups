# OBJECTIVE
Log in to the game using the username bandit2, then get the password in the "--spaces in this filename--" file.

# SOLUTION
Use this command to show all files on the server:
```bash
ls -al
```

After executing the command, the terminal will output the following:

![Terminal after the ls -al command](./ls_al.PNG)

We can get the password from the "--spaces in this filename--" file. However, similar to the previous level, we can't use this command:
```bash
cat --spaces in this filename--
```

Since the filename contains spaces and starts with "--", the terminal will treat each part as an option, and return this:

![Wrong command 1](./cat_wrong_1.PNG)

To make the system interpret this as a single filename, we need to enclose it in double quotes (""). But if we execute this:
```bash
cat "--spaces in this filename--"
```

The terminal will output the following error:

![Wrong command 2](./cat_wrong_2.PNG)

Root cause: Even though we enclosed the filename in double quotes, it still starts with "--", which makes the system interpret it as an option, and output the error shown above. To fix this, we can use the same trick as in the previous level, and the terminal will output the password: 

!["Level completed" screen](./objective.PNG)

# PASSWORD
```
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
```
 