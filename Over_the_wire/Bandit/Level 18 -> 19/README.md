# Level 18 -> 19
> The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

> Commands you may need to solve this level: ssh, ls, cat

So, in this level, I understand that the .bashrc file, which is executed when I log in, is configured to kick me out every time I try to login (Read more about
.bashrc [here](https://www.journaldev.com/41479/bashrc-file-in-linux)). So, this level suggest me only 3 commands, and since I understand the purpose of **ls** and
**cat** is too simple, and can't change anything here, I read the ssh manual again, and I realised that, after the **user@hostname** part, there's a **command** part,
and it said that "If command is specified, it is executed on the remote host instead of a login shell.". So, I can execute one command and get out without actually
get into the machine. So, I just need to execute command right there, and I got the password, without triggering the .bashrc script.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2018%20-%3E%2019/Images/0.png)
