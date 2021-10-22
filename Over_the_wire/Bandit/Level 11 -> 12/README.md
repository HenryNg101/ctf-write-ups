# Level 11 -> 12
> The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

> Commands you may need to solve this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

When I read the challenge, I know that it's [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher). And if the rotation is 13, it's ROT13, a special case 
of Caesar cipher. Linux has no tool for this, but I just need to put the text inside "data.txt" into an online decoder, and I got it.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2011%20-%3E%2012/Images/0.png)
