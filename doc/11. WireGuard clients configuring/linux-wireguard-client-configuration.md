# Linux WireGuard client configuration

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

In order to connect to a VPN, follow these steps:

**Step 1**. Open the link you received in a browser to get instructions and configuration for your new VPN connection. And you will see the following page in the browser window  
    [![image-1670928539397.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1670928539397.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1670928539397.png)
**Step 2**. In order to start the configuration you need to download the configuration file. To download the configuration file, click the "Dowload config file" button.  
    [![image-1671007982861.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671007982861.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671007982861.png)
**Step 3**. Save the file to downloads or any other place to import later. You can download the configuration file and move it to your server, or you can create a new file and copy the configuration text into it. We will copy the configuration text into a new file in this WireGuard client setup guide.
**Step 4**. Since we are setting up a connection for an Linux device, we need the WireGuard client for Linux. To download and install the client on your device, by command `<strong>sudo apt install wireguard</strong>`
**Step 5**. After installing the client, navigate to the folder `<strong>cd /etc/wireguard/</strong>` and create a configuration file. With the help of the command `<strong>nano wg0.conf</strong>`
**Step 6**. Copy the configuration text into your terminal window.  
    [![image-1671008968309.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671008968309.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671008968309.png)
**Step 7**. Save the file, after saving the file you need to complete the connection.   
    Connect using the command: `<strong>sudo wg-quick up wg0</strong>`
