# Level 14 -> 15
> The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

> Commands you may need to solve this level: ssh, telnet, nc, openssl, s_client, nmap

So, for this level, it tells me to connect to localhost, but doesn't teel me that I need authentication to connect to it. So, ssh is not the option here. I checked
some other options, so only telnet and netcat are okay, since the server at that port doesn't use SSL (openssl s_client). To connect to it, we simply need to netcat 
or telnet to that port in localhost, and that's how it's done

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2014%20-%3E%2015/Images/0.png)

Note: One more interesting thing, but quite obvious that I just realised that, to connect to that port on localhost, you can do it for any bandit user (since the 
host is the same, bandit.labs.overthewire.org)
