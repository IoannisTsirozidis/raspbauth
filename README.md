# RaspbAuth

![raspbauth](raspbauth.png)

A raspberry-pi, <span style="color:#8a2962">IoT</span>  
technology, for  
Time-Based One-Time Password <span style="color:#3d5766">(TOTP)</span> authentication

developed by  
**<span style="color:#8a2962">Ioannis Tsirozidis</span>**

## High level  
### Architectural Diagram  
![architecturaldiagram](architecturaldiagram.png)

## APACHE2  
### domains & subdomains used  
![apache2](apache2.png)

![raspbauth](raspbauth.png)  ![raspbhost](raspbhost.png)  
raspbauth.com               work.raspbauth.com

## DATABASE IMPLEMENTATION  
### WITH SQLITE

![sqlite3](sqlite3.png)

- username
- plainpassword
- hashedpassword
- otp
- session_status

![database](database.png)