![obraz](https://github.com/Anogota/Delivery/assets/143951834/15c7150e-a95e-465f-8cb3-d91720fdb09a)1.How many TCP ports are open on the target?
First what i reccomend is use: nmap -sCV -p- <IP> with this switch, you can get everything you want.
We get a lot of information from this scan.

![obraz](https://github.com/Anogota/Delivery/assets/143951834/c3ac5c8b-3c65-4955-aad4-f4cfb54c4b87)

First is the port 22 we know is a SSH, port 80 HTTP, and some new port i see this port first time 8065 and this port is unknow.

2.What is the FQDN for the Help Desk?
I go to the website and do manualy some recon, and ther we can see, CONTACT US, i go this website, before this you need to add domain to /etc/hosts helpdesk.delivery.htb, without this u can't acces to this page, after when you add this to hosts you can see the page, and there we need to do some recon to find what we wnat :P Hmm i did here small mistake because i don't google what that mean FQDN i trying found but i don't know what. The answer for this task is:helpdesk.delivery.htb
The shortcut FQDN mean Fully Qualified Domain Name

Here is the screanshot, how look the website:

![obraz](https://github.com/Anogota/Delivery/assets/143951834/03d64b91-d915-4c62-b4f5-4d7f205d7950)

3.Do you need an account to create a ticket on the support center?
For the test i make some ticket, and i don't need any account to create it.

4.Is it possible to update a ticket in any way besides interacting with the website?
First what we need to do is create a ticket and analyze what we can do with this ticket
But like me I encountered problem, i can't did a ticket, but after change VPN we got this :P

And the answer for this question is "yes" because we can add more information to your ticket, just email 2063627@delivery.htb.

![obraz](https://github.com/Anogota/Delivery/assets/143951834/b54dbae0-38a6-459e-b868-96da5cc68d44)

5.What chat software is served on TCP port 8065?
Because we can't see in as scan, we must google it or turn on more power to nmap, first what i did is use google and check what google tell me about this port.
I didn't find anything intresting, because somethimes my methodology is little bit broken, i visit the website and there we can see big text, and this is as version:

![obraz](https://github.com/Anogota/Delivery/assets/143951834/8d71dc68-daf3-453e-926f-9f15043918ab)
 
6.What user has been posting in the Internal channel?
This to escalate is awesome, spend 1 hour but i figure out how this working.
First what we need to do is create the ticket, we can see there "add more information to your ticket, just email 4141432@delivery.htb, if you create the ticket, save this e-mail and ticket number, go to view ticket and insert e-mail (your e-mail which you provided) and the ticket number, we can see as ticket, now go to the http://delivery.htb:8065/ and create the account, but with this e-mail what you save 4242432432@delivery.htb and insert there username and password, if u create this account you can see there approve your e-mail in inbox (or something like that) :P, move back to your ticket and you can see there " Please activate your email by going to: <link> " click this link and we got this :D 

![obraz](https://github.com/Anogota/Delivery/assets/143951834/983005a1-cafd-489a-bea6-4791b17a134f)
 
![obraz](https://github.com/Anogota/Delivery/assets/143951834/acb5a9c8-d60b-42bc-b134-6fd2c6e0d84b)

next step is to log in into this helpdesk.

![obraz](https://github.com/Anogota/Delivery/assets/143951834/ecc2ff98-59c7-4af6-8d33-73677dc769e1)

And we access into this page, the answer for this question is root

7.Submit the flag located in the maildeliverer user's home directory.
In this conversation are some creds

![obraz](https://github.com/Anogota/Delivery/assets/143951834/41bc3d19-2fe4-438e-bcbe-72e13c9c2e77)

I try to use it into the SSH, and i got this, this creds is correct

![obraz](https://github.com/Anogota/Delivery/assets/143951834/cfb60f29-8713-408f-95af-de42e63bf111)
