# Level 23 -> 24
> A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

> NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

> NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

> Commands you may need to solve this level: cron, crontab, crontab(5) (use “man 5 crontab” to access this)

Same as last 2 levels, I open the cron script, check the script I got and this is it:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2023%20-%3E%2024/Images/0.png)

So, from what I understand, it goes to directory "/var/spool/bandit24",for every files, even files with "." at the beginning (yeah "*" doesn't include file with "."
at the beginning), except "." and ".." files, they are current and parent directories, it checks if the owner of the file is bandit23 (current user), if yes, it executes
that file, and then delete it.

From what I understand about /var/spool ([Link](https://refspecs.linuxfoundation.org/FHS_3.0/fhs/ch05s14.html)), /var/spool/bandit24 contains work to be done by 
user bandit24, so it has the right as bandit 24. So, I can read password in here. With that in mind, I just write a simple script.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2023%20-%3E%2024/Images/1.png)

After waiting for a minute (cron execute it every minute), I go check and see the script gone, which means that it was executed and deleted, I just need to go and
print the password in file that I stored it.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2023%20-%3E%2024/Images/2.png)
