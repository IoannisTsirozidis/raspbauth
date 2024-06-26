# RaspbAuth
## Check it out at: <a href="http://raspbauth.com" target="_blank">raspbauth.com</a>

<img src="images/raspbauth.png" alt="raspbauth" width="10%">

**raspbauth** is a raspberry-pi, <span style="color:#8a2962">IoT</span> technology,  
for  
Time-Based One-Time Password (<span style="color:#3d5766">TOTP</span>) authentication

<br/>

developed by  
**<span style="color:#8a2962">Ioannis Tsirozidis</span>**

## __
### High level Architectural Diagram  
<img src="images/architecturaldiagram.png" alt="architectural diagram" width="60%">

## APACHE2  
### domains & subdomains used  
<img src="images/apache2.png" alt="apache2" width="60%">

<table>
  <tr>
    <td style="text-align: center;">
      <img src="images/raspbauth1.png" alt="raspbauth" width="40%">
      <div>raspbauth.com</div>
    </td>
    <td style="text-align: center;">
      <img src="images/raspbhost.png" alt="raspbhost" width="40%">
      <div>work.raspbauth.com</div>
    </td>
  </tr>
</table>

## DATABASE IMPLEMENTATION  
### WITH SQLITE

<img src="images/sqlite3.png" alt="sqlite3" width="30%">

- username
- plainpassword
- hashedpassword
- otp
- session_status

<img src="images/database.png" alt="database" width="40%">


## How was the Cloudflared tunnel created?

```sh
sudo apt install cloudflared
cloudflared tunnel login
cloudflared tunnel create TUNNELNAME
cloudflared tunnel route dns TUNNELNAME DOMAINNAME
cloudflared tunnel run --url localhost:PORT TUNNELNAME 
```


## WEB DEVELOPMENT
### TO CHANGE APACHE2 STARTING POINT

```sh 
sudo nano /etc/apache2/sites-available/000-default.conf
```
```sh 
DocumentRoot /var/www/html
<Directory /var/www/html>    
	Options Indexes FollowSymLinks    
	AllowOverride None    
	Require all granted
</Directory>

RedirectMatch ^/$ /root.html
```
```sh 
sudo systemctl restart apache2
```
<table>
  <tr>
    <td align="center"><img src="images/heartbeat.png" alt="heartbeat" width="80%"><br>heartbeat.php</td>
    <td align="center"><img src="images/auth.png" alt="auth" width="80%"><br>auth.php</td>
    <td align="center"><img src="images/otp.png" alt="otp" width="80%"><br>otp.js</td>
  </tr>
</table>

## THE MAIN PAGES
<table>
  <tr>
    <td style="text-align: center;">
      <img src="images/raspbauthmain.png" alt="raspbauthmain" width="90%">
      <div>raspbauth.com</div>
    </td>
    <td style="text-align: center;">
      <img src="images/register.png" alt="register" width="90%">
      <div>register</div>
    </td>
    <td style="text-align: center;">
      <img src="images/otpgen.png" alt="otpgen" width="90%">
      <div>otp generator</div>
    </td>
    <td style="text-align: center;">
      <img src="images/raspbhostmain.png" alt="raspbhostmain" width="90%">
      <div>work.raspbauth.com</div>
    </td>
    <td style="text-align: center;">
      <img src="images/hostpage.png" alt="hostpage" width="90%">
      <div>host page</div>
    </td>
  </tr>
</table>


## CLOUDFRARE INFRASTRUCTURE
<img src="images/cloudflare.png" alt="cloudflare" width="60%">