# Linux IKEv2 client configuration

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

In order to connect to a VPN, follow these steps:

1. Open the link you received in a browser to get instructions and configuration for your new VPN connection. And you will see the following page in the browser window  
    [![image-1670928539397.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1670928539397.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1670928539397.png)
2. In order to start the configuration you need install some software, before installing the software, do not forget to update the package list using the command `sudo apt update`. After the package list is updated, install additional software:  
    `sudo apt install strongswan libcharon-extra-plugins`
3. Next, prepare a certificate to encrypt the connection. You can download the certificate, open the certificate file as text and create a new file at `nano /etc/ipsec.d/cacerts/ca-cert.pem`
4. To prevent automatic connection, use systemctl to disable StrongSwan from starting automatically   
    `sudo systemctl disable --now strongswan-starter`
5. Next, you need to edit or create a file with authentication data  
    `sudo nano /etc/ipsec.secrets`  
    In this file, you need to enter your login and password data from the IKEv2 section  
    ```
    <mark><span style="background-color: #ff6600;">your_username</span></mark> : EAP <mark>"<span style="background-color: #ff6600;">your_password</span>"</mark>
    ```
6. The next step is to edit the configuration file   
    `nano /etc/ipsec.conf`  
    The contents of the configuration file should be the following  
    ```
    <mark>config setup<br></br><br></br>conn ikev2-rw<br></br>    right=<span style="background-color: #ff6600;">adres_server</span><br></br>    # This should match the `leftid` value on your server's configuration<br></br>    rightid=adres_server<br></br>    rightsubnet=0.0.0.0/0<br></br>    rightauth=pubkey<br></br>    leftsourceip=%cfg<br></br>    leftauth=eap-mschapv2<br></br>    leftid=<span style="background-color: #ff6600;">your_username</span><br></br>    eap_identity=%identity<br></br>    auto=start</mark>
    ```
    
    <p class="callout warning">**Attention!** Please note that you need to enter your data in the configuration file and the authentication file.</p>
7. To activate the connection, enter the command `sudo ipsec start` and to disable run the command `sudo ipsec stop`