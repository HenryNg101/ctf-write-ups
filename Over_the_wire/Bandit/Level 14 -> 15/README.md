# Level 14 -> 15
> The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

> Commands you may need to solve this level: ssh, telnet, nc, openssl, s_client, nmap

So, for this level, it tells me to connect to localhost, but doesn't teel me that I need authentication to connect to it. So, ssh is not the option here. I checked
some other options, so only telnet and netcat are okay, since the server at that port doesn't use SSL (openssl s_client) 

(Haven't finish)
