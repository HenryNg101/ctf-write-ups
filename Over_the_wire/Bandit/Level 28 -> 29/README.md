# Level 28 -> 29
> There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28. Clone the repository and find the password for the next level.

> Commands you may need to solve this level: git

Okay, let's continue. Do the same as last level. And I got the README.md file like this:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2028%20-%3E%2029/Images/0.png)

Well, seems like the content of the file has been changed. So, let's check all commits. A git commit is used when you changed something in project, you have to commit 
the change to the project using **"git commit"**, then to put it to the remote project on Github, you have to use **"git push [remote_name] [branch_name]"**. So, to list 
all commit logs in the history, we use **git log**:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2028%20-%3E%2029/Images/1.png)

After I see some commits here, I want to check what exactly did they do, so I used **git show [object_hash]** (git show is used to show contents of some types of git 
objects, check it out on man page to know more). So I can see that there was a line got deleted to replace with "XX...XX", and that's the password for next level.
