wut r they doin, Joe? - 300
======

Category: Memory Forensics & Malware Analysis
------
Problem Statement:
Joe's computer has like been acting kind of funny  lately. He knows you do that stuff with the computers sometimes, so he uhh brought it to you. 

Let's see if you can help him out. Can you find the full path of the "r.exe" file that the attacker put on Joe's computer?

https://s3.amazonaws.com/hsf2016/WinXPSP3x86.mem.7z

Challenge by Jamie Levy

------

Writeup
------

In this problem, we are given a rather large 7z file, which seems to be a memory dump of a windows machine.

After extracting it, we open the .mem file in a hex editor and search for `/r.exe`, which is what the problem asks for. Unfortunately, this does not yield any significant results.

However, since the file system is windows, we realize that windows in fact uses a backslash instead of a forward slash to delimit directories. After searching for `\r.exe`, we get the flag: `c:\windows\system32\1076\r.exe`
