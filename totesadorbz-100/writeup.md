totesadorbz - 100
======

Category: Steganography & Image Forensics
------
Problem Statement:
Hedgehogs are totally adorable, but there's something more than cuteness in this picture.

https://s3.amazonaws.com/hsf2016/hedgehog.jpeg

------

Writeup
------
In this problem, we are given a .jpeg file of a hedgehog. Unfortunately, preliminary tests such as stegsolve and `strings` do not reveal anything useful. Additionally, there does not seem to be any extraneous data in the file.

However, this is only 100 points, so the solution must be simple.

Eventually, we stumble upon an online steg solver at https://futureboy.us/stegano/decinput.html. Unfortunately, it either doesn't work or it requires a password.

However, again, we must remind ourselves that it is a low point (and thus simple) problem. As it turns out, the password is simply the problem title: `totesadorbz`

Running it again, we get the flag: `flag{H3dgeh0gsAreLikeS00perCute}`
