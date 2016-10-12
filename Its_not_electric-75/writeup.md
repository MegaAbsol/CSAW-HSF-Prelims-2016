It's [not] electric! - 75
======

Category: Trivia
------
Problem Statement:
If you have in your custody a suspect's digital device, and you want to prevent remote wiping and alteration of the device while it's in your custody, what would you put the device in?

------

Writeup
------

The keyword here seems to be "remote." In order to prevent remote access to an object, we need to block out all communication signals coming to the device. How might we do that? With a [Faraday Cage](https://en.wikipedia.org/wiki/Faraday_cage). These block out electric fields from the outside, which would stop this remote connection. Therefore, the flag is `faraday cage`.

Interesting note: on the wikipedia page it says:
```
Faraday bags are a type of faraday cage made of flexible metallic fabric. They are typically used to block remote wiping or alteration of wireless devices recovered in criminal investigations, but may also be used by the general public to protect against data theft or to enhance digital privacy.
```
