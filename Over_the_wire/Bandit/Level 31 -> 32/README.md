# Level 31 -> 32
> There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31. Clone the repository and find the password for the next level.

> Commands you may need to solve this level: git

This level is quite easy. When I opened README file:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2031%20-%3E%2032/Images/0.png)

So, I just need to create file that has the same name. Then use **git branch** check to make sure my current branch is "master", and **git remote** to check that the 
remote git's name is "origin". Then, before I can commit, I need to add file in with **git add**, then commit, and push. This is how you contribute something to a git project. 
Of course I can't actually push to the remote, but it sends back to me the message which contains the password.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2031%20-%3E%2032/Images/1.png)
