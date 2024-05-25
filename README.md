# RaspbAuth

![raspbauth](raspbauth.png)

A raspberry-pi, ![#a0295a](https://via.placeholder.com/15/a0295a/000000?text=+) `IoT`
technology, for  
Time-Based One-Time Password ![#4b6a82](https://via.placeholder.com/15/4b6a82/000000?text=+) `(TOTP)` authentication

developed by  
**![#a0295a](https://via.placeholder.com/15/a0295a/000000?text=+) Ioannis Tsirozidis**

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
