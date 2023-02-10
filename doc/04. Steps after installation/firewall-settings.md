# Firewall settings

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

Due to the fact that different types of firewalls may be installed in the system, please pay attention to the correct settings in the **Settings&gt;Firewall** section, as described below.

<p class="callout warning">This step is required for the solution to work properly.</p>

#### Firewall configuration is available in the menu item **Settings-&gt;Firewall**

[![image-1668693211000.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668693211000.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668693211000.png)

The following Firewall configurations are required for the correct operation of the WireGuard server

##### **Forwarding (NAT)**

- <span style="text-decoration: underline;">Must</span> be **Enabled** for VPN clients to access the internet.

##### **INPUT/FORWARD/OUTPUT policy**

- <span style="text-decoration: underline;">Must</span> be **ACCEPT** for VPN clients to access the internet.

##### **Internal Traffic**

- **ACCEPT -** If you want to allow traffic exchange between VPN clients
- **DROP -** If you want to prohibit the exchange of traffic between VPN clients (it is possible to allow only on specific WireGuard interfaces)

## FILTER Rules

In this configuration section it is possible to add/delete firewall rules in the filtr table

<p class="callout info">Attention. Rules whose name starts with system\_ are system rules and cannot be deleted.</p>

[![image-1668756192496.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668756192496.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668756192496.png)

## NAT Rules

In the NAT Rules section, it is possible to view all the rules for which the system has automatically created.

[![image-1668756378760.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668756378760.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668756378760.png)

## MANGLE Rules

In the MANGLE Rules section, it is possible to view all the rules for which the system has automatically created.

[![image-1668756441052.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1668756441052.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1668756441052.png)