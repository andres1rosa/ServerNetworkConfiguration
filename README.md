<h1>Network Services Configuration</h1>

<h2>Description</h2>
Welcome to the second installment of an ongoing series where we explore administrative tasks on Windows Server with a focus on Active Directory. This project goes over the necessary network configurations required for our devices to communicate with each other as well as having internet connectivity.
<br><br>
This project will focus on the DHCP, DNS, and NAT/RAS.
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
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<b>
<p>Go to “Add Roles and Features” and choose your server to install Remote Access.</p>
<img src="https://imgur.com/P8Qk40G.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Select Remote Access. Remote Access allows us to configure NAT.</p>
<img src="https://imgur.com/jf7cCL3.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Select Routing.</p>
<img src="https://imgur.com/1YbAZwl.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Selecting Routing should auto select DirectAccess and VPN. Make sure these are both selected.</p>
<img src="https://imgur.com/Q9Zm4aR.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Select “Install”.</p>
<img src="https://imgur.com/9ZHyVD7.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Close the Wizard after installation.</p>
<img src="https://imgur.com/iUvbkmO.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Navigate to Routing and Remote Access </p>
<img src="https://imgur.com/rPdmjgL.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Select “Configure and Enable Routing and Remote Access”</p>
<img src="https://imgur.com/w0YmRO7.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Select “Next”.</p>
<img src="https://imgur.com/yyZXGIe.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Select “Network address translation” this will allow the clients in our network to connect to the internet using our domain controllers IP address.</p>
<img src="https://imgur.com/e41pkuw.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Choose the external switch we identified previously; this switch communicates the internet. After this step, you can go through the rest of the wizard with default configurations.</p>
<img src="https://imgur.com/5VVy6zv.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>DC1 should now have a green arrow to ensure NAT is working properly.
</p>
<img src="https://imgur.com/UdyVmkk.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Go to “Add roles and Features” once more and select the DHCP role.</p>
<img src="https://imgur.com/nFADjMf.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Ensure DHCP installs succesfully.</p>
<img src="https://imgur.com/DL1fLnn.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Navigate to tools on the windows server and select DHCP. This is where we create a new scope.</p>
<img src="https://imgur.com/tBoQuks.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>The name of the scope will be the IP range.</p>
<img src="https://imgur.com/m22uwwq.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>The IP Range we use is 172.16.0.100-200 with a subnet mask of 255.255.255.0.</p>
<img src="https://imgur.com/XipkZx0.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>The Default gateway is the IP address of the domain controller.</p>
<img src="https://imgur.com/ac5JqG1.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>
The lease Duration is simply how long the clients will have the same ip address before they use another address. The default configuration will be adequate.
</p>
<img src="https://imgur.com/IOw31a2.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>After configuring the DHCP scope, we will add a router to the server options.
</p>
<img src="https://imgur.com/VMUrpqz.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>
Our IPV4 should now be green in our DHCP.
</p>
<img src="https://imgur.com/xVoTkjS.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Log into CL1 and change the name and add the client to the domain.
</p>
<img src="https://imgur.com/j3Md55E.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Input your admin credentials.</p>
<img src="https://imgur.com/9kVcXSd.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>See the success.</p>
<img src="https://imgur.com/keGTNNF.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Utilizing CMD, verify the hostname changed. Use ‘ipconfig’ to verify the client now has an IP address in the IPV4 range we previously configured. In this case, we were automatically assigned ‘172.16.0.101’. This is the first IP address in the range we configured.
</p>
<p>
Utilizing ping, we ping google.com and verify we have internet connectivity.
</p>
<img src="https://imgur.com/mFqR9PP.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>We sign out and verify we can sign into the computer utilizing our admin credentials.</p>
<img src="https://imgur.com/bweXxEX.png" height="50%" width="50%" alt="install AD DS"/>
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
