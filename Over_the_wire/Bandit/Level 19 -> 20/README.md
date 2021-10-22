# Level 19 -> 20
> To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

So, in this level, I just got an executable, with special permission, setuid (you can read for more special permissions [here](https://www.thegeekdiary.com/linux-interview-questions-special-permissions-suid-sgid-and-sticky-bit/)).
I tried executing the ELF executable, and it also said that. When I tried using command **whoami** with it (**./bandit20-do whoami**), to find out which user I get when use the file, I found
out that it's bandit20, which is the next level. So, I only need to go the password folder, and print out my password, which is the next level user's pass.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2019%20-%3E%2020/Images/0.png)
