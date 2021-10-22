# Level 12 -> 13
> The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

> Commands you may need to solve this level: grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

So, let's open the file

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2012%20-%3E%2013/Images/0.png)

Hmm, it's a hexdump, which is, simply the display of memory of a file. So, I need to reverse the dump to find out more about it, which can be done by **xxd** command
with **-r** option.

From what the challenge said and I found out, this file is compressed many times, so the remaining task is to decompress it until it gives us the password. It's
just a repeated process. Check file type with **file** command, apply appropriate way to decompress them. For different types of compression, we need to apply
differently:
    
* gzip: rename file with .gz extension (if the file extension is not .gz), then use **gunzip [filename]**
* bzip2: **bunzip2 -d [filename]**
* POSIX tar archive: **tar -xf [filename]**

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2012%20-%3E%2013/Images/1.png)

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2012%20-%3E%2013/Images/2.png)
