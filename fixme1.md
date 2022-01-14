# picoCTF 2022: fixme1.py

**Category:** General Skills

**Points:** 25

**Description:** Fix the syntax error in this [Python script](https://artifacts.picoctf.net/c/42/fixme1.py) to print the flag.

## Introduction

This problem is based on Python as the script has a syntax error that we need to fix. Therefore, we need to to install [Python](https://www.python.org/downloads/) and edit the file in an IDE of our choice.

## Steps

After opening and running the file, it is apparent that there is a syntax error on the last line of the code:

```py
flag = str_xor(flag_enc, 'enkidu')
 print('That is correct! Here\'s your flag: ' + flag)
```

This is an unexpected indentation and the fix is quite simple:

```py
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)
```

After running the correct code, the output is:

`That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_e3881c95}`
