# Level 29 -> 30
> There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29. Clone the repository and find the password for the next level.

> Commands you may need to solve this level: git

So, after I cloned, print out the content of README.md, it said this:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2029%20-%3E%2030/Images/0.png)

I had to Google about "Git production", and it tells me about Git branching workflow (Read more [here](https://medium.com/@patrickporto/4-branching-workflows-for-git-30d0aaee7bf)).
In Git, you can divide projects into branches. For example, when you work on your project, and you want to write a feature, but you are not confident with it, you
 can create a branch for testing purpose with **git branch**, then when everything works well, you can merge them with **git merge** later. And that's the idea for
 git workflows. So, in this case, the password is not in production branch, let's check if there's any other branch.

There's nothing here. But how about remote branches ?? They may not be shown here, but they are referenced in the git project (Read more [here](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)). 
So I checked again, with same command, but add **"-r"** option, and I got this (Or you can also do it with **git ls-remote**):

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2029%20-%3E%2030/Images/1.png)

Here we go. So, we got 4 references. But since we are already in master branch, we can remove the "HEAD" and "master" ones (HEAD is a pointer to current branch you're on, 
read more about it [here](https://git-scm.com/book/en/v2/Git-Internals-Git-References)). Let switch to those two branches with **git checkout [branch_name]** (branch_name 
can be normal one or with [remote_name] at the beginning to lead detach HEAD). And at **"dev"** (**"origin/dev"**) branch, in README file, you got the password.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2029%20-%3E%2030/Images/2.png)
