# PUQVPNCP
Provision and management of WireGuard VPN servers/accounts via WEB.

Managing **WireGuard** VPN server using web interface
Managing **IKEv2** VPN server using web interface


Easy to setup, all-in-one WireGuard and Management Web UI

[**Documentation**](https://panel.puqcloud.com/link.php?id=42")

# Description

#### Introducing the ultimate solution <span class="hljs-keyword">for</span> managing VPN servers!

<span class="hljs-keyword">With</span> our software, you can easily create <span class="hljs-built_in">and</span> manage VPN servers <span class="hljs-keyword">using</span> the latest <span class="hljs-built_in">and</span> most secure protocols, such <span class="hljs-keyword">as</span> **WireGuard** <span class="hljs-built_in">and</span> **IKEv2**. Whether you need a VPN server <span class="hljs-keyword">for</span> personal use <span class="hljs-built_in">or</span> <span class="hljs-keyword">for</span> your business, our software has you covered.

But that<span class="hljs-comment">'s not all - our software is also universal and easy to use, making it perfect for users of all skill levels. You don't need to be a technical expert to set up and manage your VPN servers - our software makes it simple and straightforward.</span> <span class="hljs-keyword">Try</span> our software today <span class="hljs-built_in">and</span> see how it can help you secure your online connections <span class="hljs-built_in">and</span> protect your data!

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)

[![image-1668782960072.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668782960072.png)](https://panel.puqcloud.com/index.php?rp=/store/puqvpn "https://panel.puqcloud.com/index.php?rp=/store/puqvpn")

[![image-1668783561800.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668783561800.png)](https://www.wireguard.com/ "https://www.wireguard.com/")

****PUQVPNCP**-** It is a software product written in the GO language. Distributed as a deb package. And it is designed for LINUX Debian and Ubuntu operating systems.

The main goal of the product is to manage **WireGuard** and **IKEv2** servers and clients in an easy and intuitive way.

##### **The main features of the control panel:**

- Simple and Intuitive Web Interface
- Integrated SSL Let’s Encrypt
- Creating and managment servers **WireGuard** and **IKEv2**
- Creating and Managing **WireGuard** and **IKEv2** Clients
- Possibility to limit the speed of clients **WireGuard** and **IKEv2**
- Collection of traffic usage statistics for **WireGuard** and **IKEv2** clients
- Generating QR Codes for Configuration of **WireGuard** Clients
- One-time links for transferring **WireGuard** and **IKEv2** client configuration data
- Server firewall management
- DNS caching server management for **WireGuard** clients
- A full-fledged ability to remotely control the panel via API

##### **Limitations in the free version:**

- **User limit 50**
- **API usage limit**

##### **Minimum technical requirements:**

- **Virtual machine or physical server**
- **Operating systems: Debian 11+ (amd64), Ubuntu 20+ (amd64)**
- **CPU: 1**
- **RAM: 1Gb**
- **Internet access (real IP address on the interface)**

##### **Quick installation**

```shell
wget https://download.puqcloud.com/cp/puqvpncp/puqvpncp_1.2-3_amd64.deb
dpkg -i puqvpncp_1.2-3_amd64.deb
```

##### After installation, connect to your server via a web browser.

http://SERVER_IP:8098  
Username: **admin**  
Password: **admin**

[![image-1669217732209.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1669217732209.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1669217732209.png)

[![image-1668690609770.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668690609770.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668690609770.png)


# Creating a WireGuard Configuration

<p class="callout info">In order for the WireGuard solution to work properly, it is necessary to create, among others: interface for Wireguard and configure other settings</p>

##### **WireGuard's** configuration is available in the menu item **VPN servers-&gt;WireGuard**

[![image-1671005452213.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671005452213.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671005452213.png)

To create a new **WireGuard** server, click the Create button.

[![image-1671005591390.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671005591390.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671005591390.png)

The system will automatically fill in the form for creating a new server with unique data.

You can change the data if necessary.

- **Name** - This is a unique configuration name, this name appears in the system as the main configuration model of the **WireGuard** interface, this parameter cannot be changed later
- **Private key/Public key -** Keys for encrypting the traffic of the WireGuard interface, the system generated new keys, but you can set them yourself when creating the **WireGuard** interface
- **Interface name -** Name of the **WireGuard** network interface in the system, this parameter cannot be changed
- **IP/MASK -**The parameters of the internal network of clients of this **WireGuard** interface, the address that is specified will be assigned to the interface and for all clients of this interface it will be the default gateway.
- **Internal Traffic -** Allow or deny traffic exchange between the client of this interface
- **Port -** Port on which the interface will listen for incoming connections
- **External IP -** The public IP address that will be used in the interface configuration, NAT will be organized through this address for all clients of this interface. **The address must be public and configured on the server**.
- **DNS 1/DNS 2 -** DNS servers that will be issued to the client of this interface
- **Bandwidth download/Bandwidth upload -** conditional value for the throughput of each peer connected to this **WireGuard** interface. This data will be automatically applied when creating a VPN client for this WireGuard interface.
- **Persistent Keepalive -** A sensible interval that works with a wide variety of firewalls is 25 seconds. Setting it to 0 turns the feature off, which is the default, since most users will not need this, and it makes **WireGuard** slightly more chatty
- **IKEv2 Enabled -** Enables **IKEv2** protocol support for this interface. If set to **YES** then users of this interface will connect to the server using the **IKEv2** protocol


# Create a server certificate

<p class="callout info">Before creating a server certificate, you must create or import a root certificate.</p>

Go to menu item **VPN servers -&gt; IKEv2**

[![image-1670924167899.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1670924167899.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1670924167899.png)

You need to fill in the required fields such as:

- **Server Domain**
- **Server IP**
- **Common name**
- **Organization**

Then click the button **Generate SERVER certificate**

After these steps, the **Server certificate and private key** will be generated.  
Information about the certificate will be available in the same place.

[![image-1670924293587.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1670924293587.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1670924293587.png)

To remove the server certificate, use the **Delete SERVER certificate** button

After a successful server certificate generation process, the IKEv2 server transitions to the enabled state.

[![image-1670924457963.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1670924457963.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1670924457963.png)

# Diagnostic Information

##### Information about VPN account diagnostics is available in the menu item **VPN accounts -&gt; List accounts.** Select the VPN account for which you want to display diagnostic information by clicking the **EDIT** button

[![image-1671016077083.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671016077083.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671016077083.png)

[![image-1671016081489.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671016081489.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671016081489.png)

##### IKEv2 section

Actual data from the system about the connection in the **IKEv2** protocol

##### WireGuard

Actual data from the system about the connection in the **WireGuard** protocol

##### Firewall Mangle

The actual data is taken from the system firewall, these are rules that mark traffic from the client and to the client for bandwidth limitation purposes and to collect traffic statistics, with statistics on packet counters and traffic passing through these rules.  
While the system is reading the brush value, the counter is reset to zero.

##### Traffic control

The actual data is taken from the system with the Traffic Control configuration, it shows that the interfaces are involved in traffic filtering in order to limit the rate for clients of this interface.

##### Traffic

Actual traffic usage in the current month

There is also a section with the configuration of the **WireGuard** client in the form of a QR code and in text form
