# Level 10 -> 11
> The password for the next level is stored in the file data.txt, which contains base64 encoded data

> Commands you may need to solve this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

So, I print out, and I got some encoded text. I quickly realised that this is base64 (this is [how](https://www.hannesholst.com/blog/how-to-identify-a-base64-encoded-string/) I knew it).
So Linux has a tool for it, which is **base64**, I just need to use it, with **-d** option to decode, instead of encode, and I got the pass.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2010%20-%3E%2011/Images/0.png)
