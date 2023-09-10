1.How many TCP ports are open on the target?
First what i reccomend is use: nmap -sCV -p- <IP> with this switch, you can get everything you want.
We get a lot of information from this scan.

![obraz](https://github.com/Anogota/Delivery/assets/143951834/c3ac5c8b-3c65-4955-aad4-f4cfb54c4b87)

First is the port 22 we know is a SSH, port 80 HTTP, and some new port i see this port first time 8065 and this port is unknow.

2.What is the FQDN for the Help Desk?
I go to the website and do manualy some recon, and ther we can see, CONTACT US, i go this website, before this you need to add domain to /etc/hosts helpdesk.delivery.htb, without this u can't acces to this page, after when you add this to hosts you can see the page, and there we need to do some recon to find what we wnat :P Hmm i did here small mistake because i don't google what that mean FQDN i trying found but i don't know what. The answer for this task is:helpdesk.delivery.htb
The shortcut FQDN mean Fully Qualified Domain Name

Here is the screanshot, how look the website:

![obraz](https://github.com/Anogota/Delivery/assets/143951834/03d64b91-d915-4c62-b4f5-4d7f205d7950)
