# Lets Warm Up

## Challenge
> If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Hint
> Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

## Solution
You can use Python to convert this hex number to the equivalent ASCII character:
```python
print(chr(int(0x70)))
```
Or using [this](https://www.rapidtables.com/code/text/ascii-table.html) table to search for the character you want to find, and you got the result.

## Flag
**picoCTF{p}**
