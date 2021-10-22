# Level 16 -> 17
> The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

> Commands you may need to solve this level: ssh, telnet, nc, openssl, s_client, nmap

So, the challlenge is the same as the last one, except that I don't know whic port to connect, the range is huge, 31000 -> 32000. To find out which port, I use a
very famous network scanning tool, called **nmap**, which is used a lot in networking and cybersecurity (web security, pentesting, etc).  

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2016%20-%3E%2017/Images/0.png)

(-sV to print the service/version info, -p to specify what port(s) to scan)

So, as we can see, we got 2 ports use ssl. So, let's connect to the first one, port 31518.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2016%20-%3E%2017/Images/1.png)

Doesn't seem like it. Now, the rest must be it.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2016%20-%3E%2017/Images/2.png)

Nice !! So, here I got a ssh private key, same as what we did in level 13 -> 14. So I just need to create a file, put that key in, and use it to connect 
to next bandit user on localhost. (I forgot to do it at the beginning, but you have to restrict access to other people with chmod, so the key is secured enough to
be accepted by server).

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2016%20-%3E%2017/Images/3.png)

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2016%20-%3E%2017/Images/4.png)

Note: For access restriction and permission, I already mentioned it in level 5 -> 6.
