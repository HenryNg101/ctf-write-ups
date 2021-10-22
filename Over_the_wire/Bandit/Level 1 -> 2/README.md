# Level 1 -> 2

> The password for the next level is stored in a file called - located in the home directory

> Commands you may need to solve this level: , cd, cat, file, du, find

In this level, I got a file in home directory, just like last level. But the file name is a special character, so I can't print out it normally, otherwise it's 
confusing for bash to process it, it will lead to errors. So, I need to add "./" before it ( "." represents current directory, "/" is used to seperate filename with
parent directory). Another way to deal with this is to put the filename to double quotes (""), so bash will identify it as a string, and in a string you can put 
special characters in there.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%201%20-%3E%202/Images/0.png)
