# picoCTF 2022: Glitch Cat

**Category:** General Skills

**Points:** 30

**Description:** Our flag printing service has started glitching!

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
nc saturn.picoctf.net 55824
```

After connecting to the domain, we receive this fragmented output that vaguely resembles a flag:

```
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
```

It is apparent that this server is running python to display this output due to the `chr` function used in the output. To get the obfuscated characters, we can simply print them in Python:

```py
print(chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) +
      chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64))
```

This code outputs: `9c42a45d`

After putting all the parts together, the flag is:

`picoCTF{gl17ch_m3_n07_9c42a45d}`
