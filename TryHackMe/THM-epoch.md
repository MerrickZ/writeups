# Epoch
=======

[Epoch on TryHackMe](https://tryhackme.com/room/epoch?ref=x.com/anpho)

> Epoch is a UNIX utility to convert UNIX dates and timestamps.

This is simple room with just 1 question. HINT said: `The developer likes to store data in environment variables, can you find anything of interest there?`  So all you need is to call `env`.

Read the description:

>Our website actually just passes your input right along to that command-line program!

Well, try `;env` , it works.
