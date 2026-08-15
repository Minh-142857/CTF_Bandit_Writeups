# OBJECTIVE
Log in to the game using the username bandit1, then get the password in the "-" file.

# SOLUTION
Log in to the game: Use ssh command with given information:
- Host: bandit.labs.overthewire.org
- Port: 2220 
- Username: bandit[level]
- Password: [Password of the previous level]

(**NOTE**: Since the instruction above applies to most levels, subsequent writeups will not repeat this step.)

Use this command to show all files on the server:
```bash
ls -al
```

After executing the command, the terminal will output the following:

![Terminal after the ls -al command](./ls_al.PNG)

Now we can get the password from the "-" file. However, if we use this command:
```bash
cat -
```
The system will understand that it needs to read input from the keyboard, instead of reading from the file. In that case, we need to press Ctrl + C to stop executing the command.

![Wrong command and how to stop it](./cat_wrong.PNG)

To get the password, we can use any of these 2 commands:
```bash
cat ./- #The system will interpret this as the file path
cat -- - #Signal the end of command options
```

!["Level completed" screen](./objective.PNG)

# PASSWORD
```
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```
 