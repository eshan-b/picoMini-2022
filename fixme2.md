# picoCTF 2022: fixme2.py

**Category:** General Skills

**Points:** 25

**Description:** Fix the syntax error in this [Python script](https://artifacts.picoctf.net/c/71/fixme2.py) to print the flag.

## Introduction

This problem is based on Python as the script has a syntax error that we need to fix. Therefore, we need to to install [Python](https://www.python.org/downloads/) and edit the file in an IDE of our choice.

## Steps

After opening and running the file, it is apparent that there is a syntax error in the if/else code block:

```py
if flag = "":
    print('String XOR encountered a problem, quitting.')
```

Currently, we are declaring the flag as an empty string. In the if statement, we want to compare whether the flag is an empty string. To do this, we can replace the assignment operator (`=`) with a  comparison operator (`==`):

```py
if flag == "":
    print('String XOR encountered a problem, quitting.')
```

After running the correct code, the output is:

`That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_3ebe57c1}`


