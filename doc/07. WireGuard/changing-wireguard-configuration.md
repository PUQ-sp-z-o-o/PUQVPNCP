# Changing WireGuard Configuration

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

##### **WireGuard** configuration is available in the menu item **VPN servers-&gt;WireGuard**

Select the **WireGuard** interface you want to change and click on the **Edit** button

<p class="callout info">You must understand that changing any interface parameters will completely remove all old configuration and create an interface with new parameters.  
  
In case of changing critical parameters, each client must reconfigure the connection taking into account the new configuration.</p>

[![image-1671007016158.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671007016158.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671007016158.png)

[![image-1671007061670.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671007061670.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671007061670.png)

**You can change the following parameters of the WireGuard interface**

- **Private key/Public key -** Keys for encrypting the traffic of the WireGuard interface, the system generated new keys, but you can set them yourself when creating the **WireGuard** interface
- **IP/MASK -**The parameters of the internal network of clients of this **WireGuard** interface, the address that is specified will be assigned to the interface and for all clients of this interface it will be the default gateway.
- **Internal Traffic -** Allow or deny traffic exchange between the client of this interface
- **Port -** Port on which the interface will listen for incoming connections
- **External IP -** The public IP address that will be used in the interface configuration, NAT will be organized through this address for all clients of this interface. **The address must be public and configured on the server**.
- **DNS 1/DNS 2 -** DNS servers that will be issued to the client of this interface
- **Bandwidth download/Bandwidth upload -** conditional value for the throughput of each peer connected to this **WireGuard** interface. This data will be automatically applied when creating a VPN client for this WireGuard interface.
- **Persistent Keepalive -** A sensible interval that works with a wide variety of firewalls is 25 seconds. Setting it to 0 turns the feature off, which is the default, since most users will not need this, and it makes **WireGuard** slightly more chatty
- **IKEv2 Enabled -** Enables **IKEv2** protocol support for this interface. If set to **YES** then users of this interface will connect to the server using the **IKEv2** protocol

"**Set Bandwidth**" button, which automatically sets the bandwidth of all clients of the external interface/server Set Bandwidth for the parameters that are entered in the section Peer configuration