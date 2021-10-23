# Level 30 -> 31
> There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo. The password for the user bandit30-git is the same as for the user bandit30. Clone the repository and find the password for the next level.

> Commands you may need to solve this level: git

So, in this challenge, there's nothing on README. There's no any other branch, even remote one. 

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2030%20-%3E%2031/Images/0.png)

So, I think that, how about references, since commits and blobs are not the only objects (references) that could be in a git project 
([Git objects](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects)). I check all references with **git show-ref** (Or **git for-each-ref** is more detailed). 
So I got another reference, which is a [git tag ](https://www.freecodecamp.org/news/git-tag-explained-how-to-add-remove/). Using **git show** again, I got the 
password for next level.
 
![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2030%20-%3E%2031/Images/1.png)

Note: You can also check tags with **git tag** command, check out the link for more detailed info.
