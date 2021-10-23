# Level 24 -> 25
> A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

So, for this one, the challenge said that, we have to bruteforce every possible numbers and send it to get the password. I create a file, called "brute", then for each
line in "brute", I put password of current level next to a 4-digit number that the programs goes through.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2024%20-%3E%2025/Images/0.png)

Some small notes about the script:
* {0..9} is to iterate through 0 to 9 in bash for loop
* [password] $i$j$k$n works, because string concatenation in Bash only needs to reference the variable, you don't have to use "+" expression. (If put string in "",
you must change $var to ${var})

After I do that, I just need to feed the input to netcat connection, and then take the output of the netcat to a file. Then, I filter the result, and got the pass.

![Sol](https://github.com/HenryNg101/ctf-write-ups/blob/main/Over_the_wire/Bandit/Level%2024%20-%3E%2025/Images/1.png)
