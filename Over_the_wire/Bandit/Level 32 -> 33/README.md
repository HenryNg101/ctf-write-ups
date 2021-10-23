# Level 32 -> 33
> After all this git stuff its time for another escape. Good luck!

> Commands you may need to solve this level: sh, man

So, I login, and it welcomes me with an uppershell. I typed some command and I get:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2032%20-%3E%2033/Images/0.png)

I go to other bandit user and check "/etc/passwd" file, and this is what I got:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2032%20-%3E%2033/Images/1.png)

So, the shell is changed again, just like level 25 -> 26, but in this one, the shell is different, so I have to think it the other way. I checked the sh command, 
which spawns a bash shell. After I read a lot, did lots of searches, I found out that **$0** represent the name of the shell, which is "/bin/bash". So we just need 
to use it, and we get the normal shell. After check my user, I realised that I become user bandit33 by being able to get this shell (I'm not sure about this). So I 
just print out the password, and it's done.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2032%20-%3E%2033/Images/2.png)
