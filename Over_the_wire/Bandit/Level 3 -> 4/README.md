# Level 3 -> 4
> The password for the next level is stored in a hidden file in the inhere directory.

> Commands you may need to solve this level: ls, cd, cat, file, du, find

So, in this one, I just need to go to "inhere" directory like the challenge said. I tried using **ls** but there's nothing. Later on, after I read the manual again,
I realised that **ls** normally doesn't count files with "." char at the beginning. So I just need to add **-a** option, and I found the file, print out and got the
pass.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%203%20-%3E%204/Images/0.png)
