# PUQVPNCP
Provision and management of WireGuard VPN servers/accounts via WEB.

Managing WireGuard VPN server using web interface

Easy to setup, all-in-one WireGuard and Management Web UI

[**Documentation**](https://panel.puqcloud.com/link.php?id=42")

# Description
[![image-1668782960072.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668782960072.png)](https://panel.puqcloud.com/link.php?id=42 "https://panel.puqcloud.com/link.php?id=42")

[![image-1668783561800.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668783561800.png)](https://www.wireguard.com/ "https://www.wireguard.com/")

****PUQVPNCP**-** It is a software product written in the GO language. Distributed as a deb package. And it is designed for LINUX Debian and Ubuntu operating systems.

##### The main goal of the product is to manage WireGuard servers and clients in an easy and intuitive way.

##### **The main features of the control panel:**

- Simple and Intuitive Web Interface
- Integrated SSL Let’s Encrypt
- Creating and managment servers WireGuard
- Creating and Managing WireGuard Server Clients
- Possibility to limit the speed of clients WireGuard
- Collection of traffic usage statistics for WireGuard clients
- Generating QR Codes for Configuration of WireGuard Clients
- One-time links for transferring WireGuard client configuration data
- Server firewall management
- DNS caching server management for WireGuard clients
- A full-fledged ability to remotely control the panel via API

##### **Limitations in the free version:**

- **User limit 50**
- **API usage limit**

##### **Minimum technical requirements:**

- **Virtual machine or physical server**
- **Operating systems: Debian 9+ (amd64), Ubuntu 18+ (amd64)**
- **CPU: 1**
- **RAM: 1Gb**
- **Internet access**

**Quick installation**

```shell
wget https://download.puqcloud.com/cp/puqvpncp/puqvpncp_1.0-1_amd64.deb
dpkg -i puqvpncp_1.0-1_amd64.deb
```

[![image-1668690609770.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668690609770.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668690609770.png)

# WireGuard

##### WireGuard configuration is available in the menu item **VPN servers-&gt;WireGuard**

[![image-1668757030784.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668757030784.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668757030784.png)

##### To create a new WireGuard server, click the Create button.

[![image-1668757138560.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668757138560.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668757138560.png)

The system will automatically fill in the form for creating a new server with unique data.

You can change the data if necessary.

In the **Peers configuration** section, you can set a conditional value for the throughput of each peer connected to this WireGuard interface. This data will be automatically applied when creating a VPN client for this WireGuard interface.

##### Edit WireGuard

[![image-1668757576157.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668757576157.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668757576157.png)

- On the WireGuard interface/server page, it is possible to change everything except Name and Interface name.
- Sections for diagnostics and work checks are updated in real time and it is possible to observe the change of counters on the rules. This section is very helpful in diagnosing problems if they occur.
- Also on this page is a list of all WireGuard clients that use this WireGuard interface.

"**Set Bandwidth**" button, which automatically sets the bandwidth of all clients of the external interface/server Set Bandwidth for the parameters that are entered in the section Peer configuration
