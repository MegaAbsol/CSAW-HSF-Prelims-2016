Legit Check - 75
======

Category: Steganography & Image Forensics
------
Problem Statement:
So I bought these online from my go-to sketchy dude named David. He sent me this picture as QA, but I'm not sure if this image was really from him. Can you check?

https://s3.amazonaws.com/hsf2016/IMG_0517.JPG

------

Writeup
------

Looking at the download link, we are given a jpg file. Running `file` on it quickly reveals that it indeed is a normal jpg file. 
After opening it with an image editor, there is no clear evidence of tampering.

However, it's a relatively low value problem, so we can simply open it in a hex editor and search for "flag{".

After doing so, the flag is revealed!
`flag{d0nt_r3p_fr0m_c4n4l_str33t}`
