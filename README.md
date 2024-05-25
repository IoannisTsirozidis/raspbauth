# RaspbAuth

<img src="raspbauth.png" alt="raspbauth" width="10%">

raspbauth is a raspberry-pi, <span style="color:#8a2962">IoT</span>  
technology, for  
Time-Based One-Time Password (<span style="color:#3d5766">TOTP</span>) authentication

<br/>

developed by  
**<span style="color:#8a2962">Ioannis Tsirozidis</span>**

## __
### High level Architectural Diagram  
<img src="architecturaldiagram.png" alt="architectural diagram" width="60%">

## APACHE2  
### domains & subdomains used  
<img src="apache2.png" alt="apache2" width="60%">

<div style="display: flex; align-items: flex-start;">
    <div style="text-align: center; margin-right: 20px;">
        <img src="raspbauth1.png" alt="raspbauth" width="60%">
        <div>raspbauth.com</div>
    </div>
    <div style="text-align: center;">
        <img src="raspbhost.png" alt="raspbhost" width="60%">
        <div>work.raspbauth.com</div>
    </div>
</div>

## DATABASE IMPLEMENTATION  
### WITH SQLITE

<img src="sqlite3.png" alt="sqlite3" width="30%">

- username
- plainpassword
- hashedpassword
- otp
- session_status

<img src="database.png" alt="database" width="40%">