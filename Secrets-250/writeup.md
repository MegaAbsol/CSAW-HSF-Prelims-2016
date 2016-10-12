Secrets - 250
======

Category: File & Disk Forensics
------
Problem Statement:
Looks like our murderer is also a fan of effortless file synchronization. Can you tell me what tool they used so I can hide my secrets too?

https://s3.amazonaws.com/hsf2016/NTUSER.DAT.copy0

Challenge by Tina Ferati

------

Writeup
------

In this challenge, we are given an unusual file. Running `file` on it states that it is a windows NT registry file.

To solve this problem, we can use a registry viewer and look at the relevant installed programs. Alternatively, we can simply run `strings` on it and search for common file syncing programs.

After some research on the installed programs, we discover that the "murderer" used `Dropbox`, which is the flag.
