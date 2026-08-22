# OBJECTIVE
In the "data.txt" file, get the password next to "millionth".

# SOLUTION
Use this command to show all files and directories in the current directory on the server:
```bash
ls -al
```

The terminal will return the following:

![Terminal after the ls -al command](./images/ls_al.PNG)

Now our task is to access the target file and get the password. However, if we use `cat data.txt`, our terminal will get flooded with text. To illustrate, this is a part of the file:

![Terminal if we only use cat command](./images/cat_wrong.PNG)

It is impossible to check every single line manually. So, we have to use a command similar to the `find` command, but searches within a file - `grep` command. Use the following command:
```bash
# NOTE: Don't forget to enclose the target word in double quotes ("")!!
cat data.txt | grep "millionth"
```

!["Level completed" screen](./images/objective.PNG)

**NOTE**: Since the `grep` command can read the file by itself, we can skip the `cat` command like this:
```bash
grep "millionth" data.txt
```

# PASSWORD
```
VR1ljMayciFxbnUokuQmJFw6QC9VKtub
```
 