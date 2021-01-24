# OverTheWire: Bandit
#### This is going to be my solution and brief explaination of how I did I played Bandit Wargame on OverTheWire. Here is the [link](https://overthewire.org/wargames/bandit/) to this wargame. There are also other wargames in OverTheWire, don't forget to check it out.

# **1. Level 0 -> 1:**
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%200%20-%20Level%201/Screenshot_2021-01-24_17_16_34.png)
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%200%20-%20Level%201/Screenshot_2021-01-24_17_22_05.png)
- Use command: ssh bandit0@bandit.labs.overthewire.org –p 2220. Then open "readme" file with command "cat": "cat readme"(you can check to see what file is in the machine with "ls" command), you got the password: **boJ9jbbUNNfktd78OOpsqOltutMc3MY1**
- Explaination: "ssh" command is to open a SSH connection to a remote server, and to open, you must specify address in the form: [hostname]@[server], then other options (read in manual doc), in this case, the port we want to connect to, which is 2220.
- From now on, to connect to next level’s machines, use the same command, the only difference is just the hostname, which is “bandit” + (the level). For example, “bandit0”, “bandit1”.

# **2. Level 1 -> 2:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%201%20-%20Level%202/Screenshot_2021-01-24_17_57_38.png)
-	So, like I did before, I check files, and I saw only a file with the name “-“, which is a special character, so can’t be opened in the same way, you have to open it with command “cat ./-“, and it has the password for the next level: **CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9**
-	Explaination: “./” represent for current working directory, so, when added “./”, it's the same,  before the file with special character, you can open it. To learn more about open files with special characters, check this out: [link](https://tldp.org/LDP/abs/html/special-chars.html).

# **3. Level 2 -> 3:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%202%20-%20Level%203/Screenshot_2021-01-24_18_00_25.png)
-	Same way with previous level, the only problem is, the file contain spaces, and spaces in terminal are used to separate parameters passed to the command, but we only want 1 parameter, which is the file name, in this case. So, to deal with file with spaces, use backslash before the space. Example: “cat hello\ friend” for “hello friend” file.
-	A little tip for this, if you don’t want to type too much, use “Tab” key to autocomplete file name for you.
-	Command: “cat spaces\ in\ this\ filename”, and you receive the password, which is: **UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK**

# **4. Level 3 -> 4:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%203%20-%20Level%204/Screenshot_2021-01-24_18_02_14.png)
-	After you got the “inhere” directory, and check file with “ls” command, you don’t get anything, because, the default “ls” command ignore files starting with “.” character, so, to do this, apply “-a” option to list all files, include files starting with “.” character, you got “.hidden” file, open file, we got the password, which is: **pIwrPrtPN36QITSp3EQaw936yaFoFgAB**

# **5. Level 4 -> 5:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%204%20-%20Level%205/Screenshot_2021-01-24_18_05_12.png)
-	After you got the “inhere” directory, and check file with “ls” command, you see that there are several files, and we got the hint, which is, human-readable file, however, when I checked, I don't get anything, so I used "strings ./*"(the star chracter represents for all files in directory) command, to filter only readable characters, and I got the password, which is: **koReBOKuIDDepwhWk7jZC0RTdopnAYKh**

# **6. Level 5 -> 6:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%205%20-%20Level%206/Screenshot_2021-01-24_18_10_22.png)
-	After login to the machine, and go to the “inhere” directory, we got lots of directories, so, if we try to open all of files, that’s gonna take very long time. But we have been given some criteria, so we will use “find” command with those criteria, we will use this command in this case “find –size 1033c –readable –not –executable”, and you got the password: **DXjZPULLxYr17uwoI01bNLQbtFemEgo7**
-	If you don’t get the criteria in this command, “-size 1033c” is for filtering the files with that size, 1033 bytes (c is for byte). “-not –executable” is for filtering files that are not executable, “-not” is the NOT operator, go before an expression, so, in this case, this will find the files that are not executable instead. 

# **7. Level 6 -> 7:** (Incomplete)\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%206%20-%20Level%207/Screenshot_2021-01-24_18_13_03.png)
-	Just like the last level, but different argument because we got different infos about the file, so the command is: “find / -user bandit7 –group bandit6 –size 33c”. The difference here, when compared to last one, is the first “/” character, this represent for the “root” directory, which contains all of files in the system, because in this level, there are some directories and files are hidden, so we need to access root directory to find all possible files.
-	However, when run command, there are lots of files that you can’t access, because you don’t have permission to access them, but there is one result, and that's the result for this level, which is: **HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs**

# **8. Level 7->8:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%207%20-%20Level%208/Screenshot_2021-01-24_18_16_07.png)
-	Use the “grep millionth data.txt” command, to find the line has that word, then you get the password: **cvX2JJa4CFALtqS87jk27qwqGhBM9plV**
- Explaination: grep is the command used for finding pattern in the given data, so we have been given that the password in the same line with the word "millionth", so we just need to use that command. You can read more about regular expression and grep [here](https://www.geeksforgeeks.org/regular-expression-grep/)

# **9. Level 8->9:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%208%20-%20Level%209/Screenshot_2021-01-24_18_27_45.png)
-	Use the command “sort data.txt | uniq –c”, you will see the number of occurrences of a line, and the content of that line, choose the one that only appear once, that’s the password: **UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR**
- Explaination: "uniq" command is used to omit **repeated** and **adjacent** lines, and "-c" option is to count the occurences of repeated and adjacent line of a line. So, we have to sort the data first, to put all of repeated lines together, otherwise, it won't be counted. To make it efficiently, I used ["pipping"](https://ryanstutorials.net/linuxtutorial/piping.php) to take the sorted data as the input for the "uniq" command.

# **10. Level 9->10:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%209%20-%20Level%2010/Screenshot_2021-01-24_18_32_14.png)
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%209%20-%20Level%2010/Screenshot_2021-01-24_18_32_43.png)
-	After I opened the file, I see lots of scrap, so I used the command “strings data.txt” to filter readable strings, and I follow lines that are preceded by severals "=" characters (the hint we have been given), and I see the password: **truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk**

# **11. Level 10->11:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%2010%20-%20Level%2011/Screenshot_2021-01-24_18_39_24.png)
- I opened the file, and I got a text longer than usual password, but I realised that the data only contain normal characters and followed by "=", so I think that this is [Base64](https://en.wikipedia.org/wiki/Base64) encoding, so, I decoded it using command "base64 –d data.txt", and got the password: **IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR**

# **12. Level 11->12:**\
![Solution](https://github.com/quochung2k2/ctf-write-ups/blob/main/Over_the_wire/Bandit/images/Level%2011%20-%20Level%2012/Screenshot_2021-01-24_18_44_51.png)
- I read the hint for this level is, all characters have been rotated by 13 positions, so this is [ROT13](https://en.wikipedia.org/wiki/ROT13) encoding. There is no command for this, at least from what I know, but there are many online decoders, decode it and you got the password: **5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu**

13. **Level 12->13:**
14. **Level 13->14:**
15. **Level 14->15:**
16. **Level 15->16:**
17. **Level 16->17:**
18. **Level 17->18:**
19. **Level 18->19:**
20. **Level 19->20:**
21. **Level 20->21:**
22. **Level 21->22:**
23. **Level 22->23:**
24. **Level 23->24:**
25. **Level 24->25:**
26. **Level 25->26:**
27. **Level 26->27:**
28. **Level 27->28:**
29. **Level 28->29:**
30. **Level 29->30:**
31. **Level 30->31:**
32. **Level 31->32:**
33. **Level 32->33:**
