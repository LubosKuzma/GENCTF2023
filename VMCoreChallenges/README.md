# Virtual Machine Challenges List

GENCTF{Welcome_t0_BigBang}

From Harkirat:
Nick sent the  ova file yesterday evening. He added the website to the VM. The web server is setup on port 80 and 8000 (I also added a firewall exception for the ports). There’s a SSH key for each user in the database, but only the 1 is real and the rest are fake. I used MD5 for the passwords and it’s pretty easy to do a reverse lookup of the hash to find out it’s “happy123”.

Flag 1:
There’s also a XSS vulnerability and the flag is “CTF{Str1ngTh30ry_Wizard}”.

Flag 2:
Flag.txt : in /var/log
genctf{123789456321654987}

Flag 3:
F.jpeg in root.
genctf{998877665544332211}

Can you please test it up for me.

My concerns:

Is the history clear. I think this will work :
history -c Or history -cw

Port 8000 is open when machine boots.


## User Flag

## Root Flag
