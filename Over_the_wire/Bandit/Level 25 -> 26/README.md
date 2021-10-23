# Level 25 -> 26
> Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

> Commands you may need to solve this level: ssh, cat, more, vi, ls, id, pwd

After I login to the machine, it doesn't say anything, so, I just do what I normally do, I check home directory, and I got a private key file.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/0.png)

So, just like what I already did, I just connect to bandit26 with that key, and I got logged out. 

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/1.png)

After a while, I couldn't figure out, so I came to see some [hints](http://bresleveloper.blogspot.com/2018/05/overthewire-bandit-walkthrough-just.html).
And I go to check /etc/passwd file like I was told to do. And I found out that the shell for bandit26 is "/usr/bin/showtext", which I couldn't find any info about it
after some searches. 

Well, nevermind, the hint said that I need to use **vim** and **more** command, so I checked out **more** and did some test with it, I realised that,
when using more, it prints out content, same as **cat**, but if the content doesn't fit the page, the **more** command will still continue, instead of being ended
immediately like **cat**. This could be good, so I don't get kicked out immediately, and do some stuff.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/2.png)

Nice, so, I read more about **more** command, and I knows that, I can execute commands in **more** and also **vim** program. I tried executing some commands here.

![sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/3.png)

Doesn't work. Later on, I remebered that it was because the shell is not "/bin/bash", and this executable used for shell can only print out "bandit26" then do 
nothing, so, I try open vim ("v" command), since there's nothing else I can do with **more**. So I tried executing commands and it also didn't work.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/4.png)

So, now the problem is to set the shell to normal one. I used **:help** in vim, to see what I can do, and later on, **:help quickref** to find read all references,
and I found out that I can do it with **:set** command, with **shell** (or **sh**) option, so, **:set shell=/bin/bash** (or **set sh=/bin/bash**). Now, back to normal,
but this is what I got when try to print out the password:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/5.png)

I go and check the reference again, and about external command, I can also pop a shell, with **shell** command. So I just need to pop the shell and I got the password

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2025%20-%3E%2026/Images/6.png)
