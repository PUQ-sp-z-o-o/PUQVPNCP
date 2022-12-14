# Installation

<p class="callout info">It is important to follow instructions during the installation of VPN server software for several reasons:</p>

- <p class="callout info">Following instructions ensures that the software is installed correctly and all required components are present. This can prevent errors and ensure that the software functions properly.</p>
- <p class="callout info">Instructions often include important information about system requirements, compatibility, and potential issues that may arise during installation. By following these instructions, you can avoid encountering problems that could affect the performance or stability of the software.</p>
- <p class="callout info">Instructions may also include important information about configuring and setting up the software, such as creating user accounts, assigning permissions, and establishing connections with other systems or devices. By following these instructions, you can ensure that the software is set up correctly and ready to use.</p>
- <p class="callout info">Finally, following instructions during installation is a good practice that can help you avoid wasting time, effort, and resources. It can also help you avoid making mistakes that could be difficult or costly to fix later.</p>

<p class="callout warning">We suggest installing the software on a clean, freshly installed Debian/Ubuntu server.</p>

<p class="callout warning">We issue all comments after logging into the SSH terminal window as the root user.</p>

##### Linux kernels less than 5.6 (&lt;=5.5) did not include Wireguard as a feature in the upstream kernel code. Adding Wireguard support to these (older) kernels is possible via additional modules

**Check kernel version**

```shell
uname -sr

Linux 5.10.0-10-amd64
```

##### **1. Update and Install the required packages**

```shell
apt-get update
apt-get upgrade
reboot
```

```shell
apt-get update
apt-get install wireguard wireguard-dkms wireguard-tools -y
apt-get install strongswan strongswan-pki libstrongswan-extra-plugins -y
apt-get install bind9 -y
apt-get install iproute2 iptables -y
```

##### **2. Download the latest version of the package**

The latest version of software is always located at this address:  
[https://download.puqcloud.com/cp/puqvpncp/](https://download.puqcloud.com/cp/puqvpncp/)

##### **3. Install the puqvpncp package**

We carry out the installation by issuing the following command

```shell
wget https://download.puqcloud.com/cp/puqvpncp/puqvpncp_1.2-3_amd64.deb
dpkg -i puqvpncp_1.2-3_amd64.deb
```

##### **4. After installation, connect to your server via a web browser.**

Point Your web browser to following Address: ***[http://YOUR\_SERVER\_IP:8098](http://YOUR_SERVER_IP:8098)*** (replace the value of YOUR\_SERVER\_IP with your unique IP address)  
**Username**: *admin*  
**Password**: *admin*

[![image-1669217804065.png](https://doc.puq.info/uploads/images/gallery/2022-11/scaled-1680-/image-1669217804065.png)](https://doc.puq.info/uploads/images/gallery/2022-11/image-1669217804065.png)

[![image-1671024918085.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1671024918085.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1671024918085.png)

##### **5. Edit the configuration file if necessary.**

If you need to change basic server parameters after installation, you can edit the configuration file and change parameters such as IP address, port number, SSL setting or changing the path to files. You must restart the server after making changes.

```
nano /etc/puqvpncp/puqvpncp.conf 
```

##### **6. Restart**

For the server to start working properly, you must restart the server.

```shell
service puqvpncp restart
```

##### **Status** 

To quickly know the status of a server service, just issue the following command

```shell
service puqvpncp status
```

After issuing this comment, you should see a similar result. Pay attention to the status information - the service is loaded and active.

```shell
● puqvpncp.service - PUQVPNCP
     Loaded: loaded (/etc/systemd/system/puqvpncp.service; enabled; vendor preset: enabled)
     Active: active (running) since Wed 2022-11-23 13:29:09 CET; 3h 0min ago
   Main PID: 4180349 (puqvpncp)
      Tasks: 9 (limit: 9509)
     Memory: 31.0M
        CPU: 1min 18.873s
     CGroup: /system.slice/puqvpncp.service
             └─4180349 /usr/sbin/puqvpncp
```