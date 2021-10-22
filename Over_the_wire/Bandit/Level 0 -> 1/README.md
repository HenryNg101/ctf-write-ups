# Level 0 and Level 0 -> 1
## Level 0
> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

> Commands you may need to solve this level: ssh

## Level 0 -> 1
> The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

> Commands you may need to solve this level: ls, cd, cat, file, du, find

So, I decided to write 2 chals at once because they are too short to write seperately. In these two levels, you got the credential to login to the machine, and then
read password for next level in a file to proceed. So, after I read the supplied docs, I found out that SSH is a secure shell connection, used to make secured, 
encrypted connection and provide services like remote cmd, login, etc. There are many options, but we only need to provide destination, which is [user@]hostname, and
port number (Not compulsory, but default port is 22, and we need to connect to 2220).
    
![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%200%20-%3E%201/Images/0.png)

After I login to the machine, the challenge tells me to find password in a file "readme" in hoem directory. And since I'm already in home directory ("~" in bash 
represent home directory), I just need to use **ls** command to list files to check, then use **cat** to print out the password.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%200%20-%3E%201/Images/1.png)
