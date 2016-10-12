Secret Meeting - 250
======

Category: Steganography & Image Forensics
------
Problem Statement:
My super secret friend wanted to meet up somewhere in Brooklyn, but all she sent me were these raw bytes. Can you help me figure out where I'm supposed to meet her?

71 a4 13 67 65 6f 3a 34   30 2e 36 39 34 34 2c 37
33 2e 39 38 36 36 00 ec   11 ec 11 ec 11 ec 11 ec
11 ec 

------

Writeup
------
In this problem, we are given a large number of hex bytes, and we are supposed to find some sort of location.

By translating the hex digits into ASCII, we get `geo:40.6944,73.9866` along with some unreadable data. 

Unfortunately, these coordinates translate into a place in Kyrgyzstan, and there doesn't seem to be anything else.

However, it is stated that the friend is in Brooklyn, so they must be near New York. By fiddling with negative signs, we determine that the longitude must be negative. Now, we get the address `6 MetroTech Center, Brooklyn, NY 11201, USA`

Unfortunately, this is not the flag either. A quick search of the address, however, gives us the name of the location: `NYU Tandon School of Engineering`, which is the flag.
