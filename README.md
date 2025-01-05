<h1>Network Services Configuration</h1>

<h2>Description</h2>
Welcome to the first installment of an ongoing series where we explore administrative tasks on Windows Server with a focus on Active Directory. This project lays the foundation for a series of network configurations and administrative simulations.
<br><br>
This project will focus on the installation and configuration of Active Directory on DC1.
Below is a reference to the topology of the network we are working on.
<br />

<p align="center">
Topology: <br/>
<img src="https://imgur.com/X1H5wHU.png" height="80%" width="80%" alt="Topology"/>
<br /> 

<h2>Key Configurations</h2>

- <b>Dynamic Host Configuration Protocol (DHCP): Set up DHCP to automatically assign IP addresses to all connected clients, enhancing network efficiency.<b>
- <b>Domain Name System (DNS): Implement DNS to resolve hostnames to IP addresses, critical for network communication between diverse operating systems.<b>
- <b>Network Address Translation (NAT)/Remote Access Service (RAS): Configure NAT/RAS to enable secure internet access and remote connections, bridging the gap between internal networks and external resources.<b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10 (21H2)</b>

<h2>Project walk-through:</h2>

<h3>Follow the steps below to configure network services on DC1 and CL1:</h3>
<p></p>
<b>
<img src=".png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p></p>
<img src=".png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

</b>
<h2> Final Thoughts </h2>

<p>
We've successfully configured Network Services on DC1. This allowed for CL1 to be added to the domain and connect to the internet utilizing NAT/RAS through DC1.</p>



</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
