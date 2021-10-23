# Level 26 -> 27
> Good job getting a shell! Now hurry and grab the password for bandit27!

> Commands you may need to solve this level: ls

So, after get the shell from the last level, I just check to see if there's any file in home directory. And I found another ELF executable with suid permission.
I ran it, it's the same with level 19 -> 20, and it run as bandit27. All I had to do was to print out the password (/etc/bandit_pass/bandit27), and I'm done.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2026%20-%3E%2027/Images/0.png)
