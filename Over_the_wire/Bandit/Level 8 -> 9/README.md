# Level 8 -> 9
> The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

> Commands you may need to solve this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

This level, it looks like previous level, but since I don't have the keyword to find, I can't use **grep**. I looked at all commands, and find out that, **uniq**
command with **-c** option would be perfect for the job, since uniq removes duplicate lines with **-c** option, it even counts the occurences. But after I did that,
I didn't get the expected result. I read the manual again, and I realised that **uniq** command only works with duplicated **adjacent** lines, so, that means that,
I have to put all duplicated lines together, so I use **sort** for the work, and redirect output of **sort** to **uniq** command with "|" ([I/O redirection](https://www.tutorialspoint.com/unix/unix-io-redirections.htm))

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%208%20-%3E%209/Images/1.png)
