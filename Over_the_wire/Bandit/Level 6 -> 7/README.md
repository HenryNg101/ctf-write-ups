# Level 6 -> 7
> The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

> Commands you may need to solve this level: ls, cd, cat, file, du, find, grep

So, in this level, we got the same problem, but the challenge said "somewhere on the server", it means that we have to go through the entire server, from root, so,
the destination is changed, from "." in "inhere" directory to "/", "/" means root when stand at the beginning. And I just need to apply appropriate options, and I 
got the file.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%206%20-%3E%207/Images/0.png)

This works well. However, since I'm not the root user, there are many files I can't access, so, to remove all errors, I need to put errors to somewhere else, but 
not to store those errors (not necessary).

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%206%20-%3E%207/Images/1.png)

So, 2 here stands for STDERR in Linux, and ">" is to [redirect](https://www.tutorialspoint.com/unix/unix-io-redirections.htm) those errors, and /dev/null is a null device file, it takes anything and never save them, read more 
about it [here](https://www.journaldev.com/35489/dev-null-in-linux).
