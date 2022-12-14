# Dashboard

The dashboard is the center of information regarding the operation of the VPN server.

<p class="callout info">The dashboard view has a simple, even crude form, because it is a tool for professional use and the emphasis is mainly on stability, using as few add-ons as possible, which can be an additional attack vector.</p>

#### Dashboard

[![image-1671018260930.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671018260930.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671018260930.png)

#### The main page of PUQVPNCP contains diagnostic information.

##### **Server Information**

This section contains basic information about the host server, such as:

- Hostname
- OS Name
- Architecture of CPU
- CPU name
- CPU Threads and load
- Memory size and usage percentage

##### PUQVPNCP

This section provides basic information about the status of the VPN server service.

- Updated real-time information about server status.
- **Status:** If the status is not OK, it means that the panel is performing operations on the server configuration. At this point, user management of VPN servers and firewalls is limited.
- **Version:** current version of the **PUQVPNCP** panel.
- **WireGuards:** Number of WireGuard interfaces in the system.
- **VPN Accounts:** The number of VPN accounts in the system.
- **License:** License status and expiration date

##### WireGuard

- Status and versions of installed **WireGuard** packages

##### IKEv2

- Status and versions of installed **strongSwan** packages

##### Firewall

- Status and versions of installed packages iptables, iproute2
- Status about the included nat. Nat needs to be enabled.

##### DNS server

- Status and versions of installed package bind9
