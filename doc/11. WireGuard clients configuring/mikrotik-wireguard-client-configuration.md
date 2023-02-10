# Mikrotik WireGuard client configuration

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

## Configuring Mikrotik as an WireGuard Client.

##### Make sure you have an up to date **routerOS** system.

Version must be at least: 7.6

```
[admin@VPN-CLIENT] > system package print 
Columns: NAME, VERSION
# NAME      VERSION
0 routeros  7.6    
```

##### Open a single-use shipment on the **WireGuard** section for the client's configuration request

[![image-1671100595697.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671100595697.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671100595697.png)

##### Login to **Mikrotik** via Winbox

Click on the menu item **WireGuard** In the window that opens, in the **WireGuard** tab, click the plus to add a new **WireGuard** interface

[![image-1671100789370.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671100789370.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671100789370.png)

Copy the private key from the text configuration from the **\[Interface\]** section to the **PrivateKey** field in the **WireGuard** interface settings in **Mikrotik**

Click **OK** to create the interface

[![image-1671101049703.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671101049703.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671101049703.png)

Go to the peers tab.  
Click plus to add a new peer

[![image-1671101223879.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671101223879.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671101223879.png)

**Interface** - Select the previously created **WireGuard** interface

**Public key** - Copy the public key from the text configuration from the **\[Peer\]** section to the Public key field

**Endpoint** - Copy the server **address** from the text configuration from the **\[Peer\]** section to the endpoint field

**Endpoint Port -** Copy the server **port** from the text configuration from the **\[Peer\]** section to the Endpoint Port field

**Allowed Address -** Copy **AllowedIPs** from the text configuration from the **\[Peer\]** section to the Allowed Address field

**Persistent Keepalive -** Copy the **PersistentKeepalive** from the text configuration from the **\[Peer\]** section to the Persistent Keepalive field

Click **OK** to create a peer

[![image-1671101662963.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671101662963.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671101662963.png)

##### In order to have communication with the server, you need to set the address on the **WireGuard** interface

Go to the menu item **IP-&gt;Addresses** In the window that opens, click the plus to assign an IP address to the WireGuard interface

[![image-1671101826333.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671101826333.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671101826333.png)

**Addresse -** Copy the Address from the text configuration from the **\[Interface\]** section to the Address field

**Interface** - Select the previously created **WireGuard** interface

Press the OK button to confirm

[![image-1671102046038.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671102046038.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671102046038.png)

<p class="callout info">You also need to configure the traffic routes you need at your discretion.</p>