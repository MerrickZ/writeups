# Pickle Rick
=============

>[TryHackMe Room: Pickle Rick](https://tryhackme.com/room/picklerick)

This one is easy and fun, I'll just write some thoughts.

## 1. Scan

nmap first, got 2 open ports ( 22/ssh and 80/http ), so:

1. gobuster scan with -x php to find hidden pages.
2. view the source of 80/http to get some *comments* .

You'll find a username and password in this step, also you'll find a login page.

## 2. CTF

After login, there's a textbox which tells me to input commands, see which commands I can use:

1. try sudo -l
2. try whoami
3. try ls /home
4. try cat, well, it's disabled
5. try less
6. try sudo ls /root

You'll find 2 answers in these steps, but where's the 1st potion?

### 3. Somewhere Else?

Since I can use sudo, maybe it's ok to search whole disk for that `login.php` file ?

1. try `find / -name login.php`
2. try ls to that directory
3. see some weird files
4. try less to those files

Done.
