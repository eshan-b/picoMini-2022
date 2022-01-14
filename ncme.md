# picoCTF 2022: ncme

**Category:** General Skills

**Points:** 10

**Description:** Connect to a remote computer using `nc` and get the flag.

## Introduction

This problem is based on netcat—"a computer networking utility for reading from and writing to network connections using TCP or UDP" ([netcat - Wikipedia](https://en.wikipedia.org/wiki/Netcat)).

To install it on Debian/Ubuntu based system, enter this into the terminal:

```batch
sudo apt-get install netcat
```

For Fedora/RedHat/CentOS systems, enter this:

```batch
yum install nc
```

## Steps

To connect to the given domain we can use this command in the terminal:

```batch
nc saturn.picoctf.net 56469
```

After connecting to the domain, the flag is simply outputted:

`picoCTF{}`
