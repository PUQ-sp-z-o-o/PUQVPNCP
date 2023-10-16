# IPv6 Configure

**I suggest you the following configuration**

#####   
On Router:

IPv6 address: fd00:1111:2222:3333::1/120 (Interface to PUQVPNCP)  
Add route: fd00:1111:2222:3333::101/120 via fd00:1111:2222:3333::2 (this route indicates that the VPN client subnet is on PUQVPNCP)

##### On PUQVPNCP:

Interface eth0:  
IPv6 address: fd00:1111:2222:3333::2/120  
Default route: fd00:1111:2222:3333::1

Interface wg0(via web interface):  
IPv6 address: fd00:1111:2222:3333::101/120  
IPv6 range: fd00:1111:2222:3333::100 - fd00:1111:2222:3333::1ff

You can use any network ranges. The router and PUQVPNCP must be on the same network subnet (eth0), and the VPN clients must be on a completely different one (wg0).  
On the router must have a route that indicates that the wg0 subnet is located at the eth0 address.

Then incoming traffic to VPN clients will be routed through the router to PUQVPNCP, and outgoing traffic will go through the default route on PUQVPNCP.

[![image-1691054014677.png](https://doc.puq.info/uploads/images/gallery/2023-08/scaled-1680-/image-1691054014677.png)](https://doc.puq.info/uploads/images/gallery/2023-08/image-1691054014677.png)