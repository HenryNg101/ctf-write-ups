# Level 22 -> 23
> A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

> NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

> Commands you may need to solve this level: cron, crontab, crontab(5) (use “man 5 crontab” to access this)

So, for this one, I just follow like last level. I go and print out "cronjob_bandit23" file, then print the script that it executes every minute

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2022%20-%3E%2023/Images/0.png)

(Actually I just tried to print all scripts that I can print, you can ignore the above script, it was for current level, not the next one)

So, to understand quickly, I write the same script, only replace "$(whoami)" with bandit23 (Well, next level's user).

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2022%20-%3E%2023/Images/1.png)

Nice !! Gotcha. Now, let's go and print it out, and I got the password.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2022%20-%3E%2023/Images/2.png)
