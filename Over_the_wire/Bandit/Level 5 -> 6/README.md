# Level 5 -> 6
> The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable

> Commands you may need to solve this level: ls, cd, cat, file, du, find

So, first thing I do, was to get into "inhere" directory, check and there are lots of files.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%205%20-%3E%206/Images/0.png)

Because there so many files like this, I can only try to find with **find** command, based on what the challenge gave me. And I got the password ("! -perm /+x" is
to find are not executable, so "!" is the **not** operator, it reverts the result of the expression after it, "+x" is the executable permission flag, you can read
more about file permission [here](https://www.tutorialspoint.com/unix/unix-file-permission.htm))

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%205%20-%3E%206/Images/1.png)
