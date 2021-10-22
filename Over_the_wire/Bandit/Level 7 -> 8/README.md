# Level 7 -> 8
> The password for the next level is stored in the file data.txt next to the word millionth

> Commands you may need to solve this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

So, I cat out that file in home directory, and I got too many lines of text, but then I realised the pattern of it, for each line, there's a keyword on the left
and password on the right, so I just need to find out the correct line, that's when **grep** comes to play. grep is like regular expression tool for Linux, it filter
text line by line, so it work perfect in this case.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%207%20-%3E%208/Images/0.png)
