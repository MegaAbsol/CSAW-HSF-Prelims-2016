How To Get Away With Murder - 350
======

Category: File & Disk Forensics
------
Problem Statement:
What time did the file start downloading to the machine?
https://s3.amazonaws.com/hsf2016/History

Your answer should be a Unix time stamp

Challenge by Tina Ferati

------

Writeup
------

In this problem, we are given a file called `History`. If we look at this file in a hex editor, we see that it is a SQLite 3 database. In Kali Linux, there is a built-in viewer to make visualizing these databases easier. We can use this `SQLite Database Viewer` to open the file, allowing us to see the tables in the database.

The first thing that should come to mind when seeing the list of tables is that the problem is asking for the download time of a file. There is a table called `downloads`, so this is the first place you should look. In here, we see a column called `start_time`. There is no column for `end_time`, nor is there anything about download speed, so there is no way to get the actual end time. Therefore, we just look at the start time and hope that this is what they are looking for.

If we look at the timestamp provided in the `start_time` column, we see that it is far too long to be a correct timestamp in the UNIX timestamp format (what the problem asks for). If we paste the timestamp into a UNIX timestamp converter, we see that it actually ends up being in the future. Even if we assume that its time since epoch in nanoseconds or some other more precise unit, the time would still not be a reasonable one - it is either in the future or a really long time ago. The timestamp, then, must be in some other format. If we look around on the internet, we find that one of the timestamp formats that usually has 17 digits is the Chrome/WebKit timestamp format.

If we put the timestamp given by the `start_time` column into http://www.epochconverter.com/webkit, we are able to get a date/time: `Mon, 08 Aug 2016 07:37:32 GMT`. Unfortunately, entering it in the correct format doesn't work either. As it turns out, the correct time zone was UTC rather than GMT. 

UPDATE: Later, the flag format was changed to unix epoch time, which is `1470641852`.
