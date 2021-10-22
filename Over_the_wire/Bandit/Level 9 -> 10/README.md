# Level 9 -> 10
> The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

> Commands you may need to solve this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

So, I opened the "data.txt" file, and there are so much gibberish, so I just need to **strings** it, then look for lines that has several '=' characters. And I got
some lines:
    
    ========== the*2i"4
    ========== password
    Z)========== is
    &========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%209%20-%3E%2010/Images/0.png)

So, that's the password. One small tip for finding it faster is to redirect output and **grep** it with "=" character, so the command is:
    
    strings data.txt | grep =
