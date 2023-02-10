# Traffic Logging Config

##### [Order now](https://panel.puqcloud.com/index.php?rp=/store/puqvpn) | [Download](https://download.puqcloud.com/cp/puqvpncp/)| [FAQ](https://faq.puqcloud.com)

##### To enable and configure traffic logging go to **Settings-&gt;Traffic logging**

<p class="callout warning">Logging all traffic passing through a server can be very resource intensive and can have a significant impact on the performance of the server. This is because logging requires the server to process and store a large amount of data, which can consume a significant amount of CPU, memory, and disk resources. In addition, logging all traffic can generate a large number of log messages, which can further strain the server's resources.  
  
As a result, it is important to carefully consider the need for logging all traffic and to balance this need with the potential impact on the performance of the server. In some cases, it may be more appropriate to only log a subset of traffic or to use sampling or filtering techniques to reduce the volume of logs generated. It is also important to consider the hardware resources of the server and to ensure that the server has sufficient capacity to handle the load of logging all traffic.  
  
In summary, while logging all traffic can be useful for certain purposes, it is important to be aware of the potential impact on the server's performance and to carefully evaluate the need for this level of logging.</p>

[![image-1672237369542.png](https://doc.puq.info/uploads/images/gallery/2022-12/scaled-1680-/image-1672237369542.png)](https://doc.puq.info/uploads/images/gallery/2022-12/image-1672237369542.png)

#### Remote syslogTraffic logging section

you can enable logging of client traffic passing through the server

##### Logging options

You can choose the following logging options:

1. Traffic Incoming - Log also incoming traffic. By default, only outgoing traffic is logged.
2. Connections - What connection types to log (ESTABLISHED and RELATED are recommended) 
    - **ESTABLISHED -** a successfully established connection
    - **RELATED -** a connection that is related to an already established connection
    - **NEW -** a new connection that has just been established
    - **INVALID -** a connection that does not match any of the standard connection states
    - **UNTRACKED -** a connection that is not being tracked by the system

<p class="callout info">**If none is selected it will log all connections**</p>

##### Metrics

What data will be collected and transmitted to a remote server

<p class="callout info">**Already logged in by default: TIMEGENERATED, PUBLIC, SRC, SPT, DST, DPT, PROTO**</p>

##### Remote syslog

Remote syslog server configuration options

##### InfluxDB

Remote InfluxDB server configuration options

<p class="callout info">To use logging to the InfluxDB server, you need to install telegraf  
  
[https://docs.influxdata.com/telegraf/v1.21/introduction/installation/](https://docs.influxdata.com/telegraf/v1.21/introduction/installation/)</p>