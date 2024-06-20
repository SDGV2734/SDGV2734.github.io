---
Title: Try Hack Me (Lazy Admin)
categories: [SWS101, Try Hack Me CTF ]
tags: [SWS101]
---

### Topic: Lazy Admin
![Alt text](../image/lazyadmin.png)

Hello welcome back to another CFT room and in this room we will doing this room to expend our knowledge in Linux comnmands.

So  basically i  started this room with and nmap scan to see the port open this room, and in this i found that:

![Alt text](../image/LA_nmap.png)



so i went to the browser and and pasted this IP address.

![Alt text](../image/LA_webpage.png)

so i tried some common directories with gobuster and got the following:

![Alt text](../image/LA_gobuster.png)

In the /content i got the following message:

![Alt text](../image/LA_C.png)

In which i never heard of the term sweetRice and i tried to expand the knowledge and again did gobuster on the content directory an d found the following:

![Alt text](../image/LA_Content_as.png)

So i went into the /as endpoint and it gave me a login pager for the SeetRice website.

![Alt text](../image/LA_as_login.png)

and also into /inc i got a bunch of directories.

![Alt text](../image/LA_inc.png)

Than i went to the /latest.txt and i think i got the version here

![Alt text](../image/LA_lastest.txt.png)

I also went to the "mysql_backup" and i think i found the username and password to login in the  SweetRice login site.

![Alt text](../image/LA_mysql.png)

for the password i used crack station to crack hashed password 

![Alt text](../image/LA_crackHash.png)

so i used this credentails to login into the login page and i was in.


![Alt text](../image/LA_SR.png)

![Alt text](../image/LA_searchsploit.png)

![Alt text](../image/LA_search_copied.png)

![Alt text](../image/LA_cat.png)

So according to this, I need to go to the Adding Ads section and upload this, which will allow me to add PHP code to the server.












 



