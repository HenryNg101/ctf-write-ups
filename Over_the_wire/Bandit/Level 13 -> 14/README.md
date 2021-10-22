# Level 13 -> 14
> The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

> Commands you may need to solve this level: ssh, telnet, nc, openssl, s_client, nmap

So, this level gives me a SSH private key to connect to bandit14. I tried to learn more about SSH, and I realised there are more than one way for authentication
with SSH (Read more [here](https://www.golinuxcloud.com/openssh-authentication-methods-sshd-config/)). For this one, it's public key authentication. After read this
[guide](https://serverpilot.io/docs/how-to-use-ssh-public-key-authentication/) about SSH public key authentication, I know that to use this method, I just need add
**-i** option, using the provided key, and I got it. I tried connect to bandit14@bandit.labs.overthewire.org but it doesn't work, but when I read the challenge, it
mentions **localhost**, so I use localhost instead of bandit.labs.overthewire.org, and I got to next level. You can proceed to next level from here, or print out password 
for bandit14 (/etc/bandit_pass/bandit14), and now you can connect from outside.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2013%20-%3E%2014/Images/0.png)
