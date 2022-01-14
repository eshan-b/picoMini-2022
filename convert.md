# picoCTF 2022: convertme.py

**Category:** General Skills

**Points:** 15

**Description:** Run the [Python script](https://artifacts.picoctf.net/c/34/convertme.py) and convert the given number from decimal to binary to get the flag.

## Introduction

This problem is based on Python as the script has a problem we need to solve. Therefore, we need to to install [Python](https://www.python.org/downloads/) and edit the file in an IDE of our choice.

## Approach #1: Solving the binary problem

After opening and running the file, it is apparent that there is a prompt to guess the correct binary representation of a randomly generated number to unlock the flag:

```latex
If 74 is in decimal base, what is it in binary base?
Answer:
```

To convert a number from decimal to binary, we can write a short python script instead of manually solving large digits:

```py
num = int(input())
print("{0:b}".format(int(num)))
```

## Approach #2: Hacking the script

After analyzing the code more carefully, we can see that a condition has to be met in order to get the flag:

```py
if ans_num == num:
  flag = str_xor(flag_enc, 'enkidu')
  print('That is correct! Here\'s your flag: ' + flag)
```

If we simply delete the try/except block along with the line that asks for input, and replace it with the inside of the if block, we can get the result without having to compute any binary number:

```py
print('If ' + str(num) + ' is in decimal base, what is it in binary base?')
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)
```

After running the correct code or inputting the correct data, our output is:

`That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_3e01a5f5}`
