# Level 20 -> 21
> There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

> NOTE: Try connecting to your own network daemon to see if it works as you think

> Commands you may need to solve this level: ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2020%20-%3E%2021/Images/0.png)

So, I got another executable with setuid bit. When I execute it, it said that it connects to a port in localhost using TCP, which means
that I can do it with either netcat or telnet. So I read the manual doc for both command, and I realised that you can build a basic client/server model with netcat (
telnet can't do this, sadly), by simply listen on a host with specific port one side, and the other side can connect to you on that port. So I tried open one connection
on my local machine with localhost:

On server side: 

    nc -l localhost -p 1234 (-l to listen, -p is needed in this one)
   
On client side:
    
    nc localhost 1234

So, when I send a message on client to server, it receives the exact same thing that it sent, and same thing also happens with server when send back to client. So
it's clear now. I open my connection with bandit, I split my terminal into 2 panes with tmux (Just for convienience, and also easier to observe) with Ctrl-b + " to
split, Ctrl + ; to move between panes. And I got the password after I send from my listener.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2020%20-%3E%2021/Images/1.png)
