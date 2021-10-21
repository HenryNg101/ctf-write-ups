# Level 21 -> 22
> A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

> Commands you may need to solve this level: cron, crontab, crontab(5) (use “man 5 crontab” to access this)

So, this time, it's about cron jobs. Cron is a good scheduler, it's very useful for system administrator to automate tasks so that they don't have to keep up to do them. 
(You can learn more about [cron](https://opensource.com/article/17/11/how-use-cron-linux) and [set up cron](https://phoenixnap.com/kb/set-up-cron-job-linux) here)
I follow to the /etc/cron.d directory, which contains cron jobs files that cron reads to execute (Read [here](https://unix.stackexchange.com/questions/458713/how-are-files-under-etc-cron-d-used)).

And I found some cron jobs files here, the difference between them are the name, for different users, so I think bandit22 is the one I need, because I need password
 for that level(actually it is, after I did some checks). That command in the file, it means that every minute it executes the script /usr/bin/cronjob_bandit22.sh 
 and put errors and result into /dev/null, so that it won't notify user about changes (Otherwise it's too easy). I just need to print out the script, found out that it
 put bandit22 password into a file, I print the content of that file out, and I got the password.
 
 ![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2021%20-%3E%2022/Images/0.png)
