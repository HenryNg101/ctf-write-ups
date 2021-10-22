# Level 4 -> 5
> The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

> Commands you may need to solve this level: ls, cd, cat, file, du, find

So, in this one, I see that there are some files in "inhere" directory, when I **cat** them out, they give me some gibberish, it's quite annoying. So to filter
all readable characters, I use **strings** command (Combine with "./-file0*", to find all files start with "-file0", based on regex of bash).

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%204%20-%3E%205/Images/0.png)
