# OBJECTIVE
Log in to the game using the username bandit3, then get the password in the hidden file in the "inhere" directory.

# SOLUTION
Use this command to show all files and directories in the current directory on the server:
```bash
ls -al
```

After executing the command, the terminal will output the following:

![Terminal after the ls -al command](./images/ls_al.PNG)

Then, we can use this command to access the target directory:
```bash
cd ./inhere
```

![Terminal after the cd command](./images/cd.PNG)

Reuse the first command to show all files in the directory:

![Terminal after the ls -al command (In "inhere" directory)](./images/ls_al_inhere.PNG) 

After that, we can see a file named "...Hiding-From-You". Execute the following command to get the password:
```bash
cat ...Hiding-From-You
```

!["Level completed" screen](./images/objective.PNG)

# PASSWORD
```
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
```
 