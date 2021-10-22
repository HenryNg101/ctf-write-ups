# Level 15 -> 16
> The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

> Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

> Commands you may need to solve this level: ssh, telnet, nc, openssl, s_client, nmap

Now, for this time, it's like the last level, but in this port, it uses ssl encryption. So to connect to it I have to use **openssl** with it's **s_client** service.
You will see all information of the server:

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2015%20-%3E%2016/Images/0.png)

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2015%20-%3E%2016/Images/1.png)

And the rest is quite easy to be done for now.
