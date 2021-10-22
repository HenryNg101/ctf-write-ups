# Level 17 -> 18
> There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

> NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

> Commands you may need to solve this level: cat, grep, ls, diff

So, looks like an easy level. I have known all commands here, what they are for (definitely not for compare files). So, it must be diff. I just need to put 2 files
together, compare, and try 2 password (Just to found out that, the order of the difference line follows by the order of input file).

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2017%20-%3E%2018/Images/0.png)
