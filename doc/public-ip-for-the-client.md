# Public IP for the client

#### Announcing a Proper IP Address Pool

To use public IP addresses for VPN clients in PUQVPNCP (WireGuard), the first step is to have a properly announced IP address pool. Public IP addresses must be allocated and reserved for the VPN clients. Ensure that the IP addresses you allocate are not already in use on the public internet to prevent conflicts.

#### Routing the IP Address Pool to the WireGuard Server

Once you have a pool of public IP addresses, you need to route this pool to the PUQVPNCP (WireGuard) server. This is crucial for establishing connectivity between the clients and the server. You can achieve this through various routing methods, such as static routes, OSPF (Open Shortest Path First), BGP (Border Gateway Protocol), or any other routing protocol of your choice. The goal is to make sure that traffic destined for the public IP addresses allocated to VPN clients is directed to the PUQVPNCP (WireGuard) server.

#### Disabling NAT in PUQVPNCP (WireGuard) Settings

To ensure that outgoing traffic from VPN clients uses the correct public IP addresses, you need to disable NAT (Network Address Translation) in the PUQVPNCP (WireGuard) settings. NAT is a technique used to map private IP addresses to a public IP address, typically done on routers or gateways. However, when using public IP addresses for VPN clients, you want the traffic to flow directly without any address translation.

[![image-1697375165947.png](https://doc.puq.info/uploads/images/gallery/2023-10/scaled-1680-/image-1697375165947.png)](https://doc.puq.info/uploads/images/gallery/2023-10/image-1697375165947.png)

#### **Conclusion**

Configuring public IP addresses for PUQVPNCP (WireGuard) VPN clients is a technical process that involves proper IP address allocation, routing configuration, and disabling NAT. By following these steps, you can create a secure and efficient VPN network with PUQVPNCP (WireGuard) that allows clients to use public IP addresses, meeting the specific requirements of your network setup.

PUQVPNCP, based on the WireGuard protocol, provides a powerful and secure solution for VPN services. Correctly configuring public addresses for clients ensures that your network operates smoothly and securely, leveraging the simplicity and performance of the WireGuard protocol.