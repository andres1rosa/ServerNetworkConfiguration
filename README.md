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

- <b>Active Directory Domain Services (AD DS): Configure AD DS to manage all users, groups, and computers within the network domain, providing a single point of administration.<b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>

<h2>Project walk-through:</h2>

<h3>Follow the steps below to configure install and configure AD DS:</h3>
<p>Click Add Roles and Features.</p>
<b>
<img src="https://imgur.com/Ombvtoh.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Observe the beofre you begin page, click "Next".</p>
<img src="https://imgur.com/D9bqZEn.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Ensure this is a role based installation click "Next".</p>
<img src="https://imgur.com/X7FQzyn.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Choose the server to install AD DS.</p>
<img src="https://imgur.com/9fv1GCi.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Choose Active Directory Domain Services.</p>
<img src="https://imgur.com/G8gx9r4.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>The necessary features will be prompted to install, choose "Add Features".</p>
<img src="https://imgur.com/PqvcqvF.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Click "Next".</p>
<img src="https://imgur.com/FT5QOtk.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Click "Next".</p>
<img src="https://imgur.com/6NEGG6N.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Click "Install".</p>
<img src="https://imgur.com/qigupMD.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Close the wizard when the installation process is complete.</p>
<img src="https://imgur.com/IJ6vrb0.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Navigate to the flag and click “Promote this server to a domain controller.”</p>
<img src="https://imgur.com/sNWGUKq.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>We create a new forest and name our root domain “techcorp.com”.</p>
<img src="https://imgur.com/AK55WpR.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Ensure we have DNS and Global Catalog capabilities. After this step, you can go through the next steps clicking "Next" with the default configurations.</p>
<img src="https://imgur.com/91XCmfW.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>When we have completed the configuration, we will be notified of a restart. 
After restarting you will have to log into our server.
</p>
<img src="https://imgur.com/GkAmsYR.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>After logging in, we create a new Organizational Unit in our domain named “Admins”. This is where we create an account for ourselves that we can use to log into machines on our network.</p>
<img src="https://imgur.com/3XtDEWd.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Navigate to our accounts properties and add the account to “Domain Admins” to gain privileged access. </p>
<img src="https://imgur.com/PKuLcMD.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p>Now we can sign into the server using our admin account with our information.</p>
<img src="https://imgur.com/EyaI9ZB.png" height="50%" width="50%" alt="install AD DS"/>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
</b>
<h2> Final Thoughts </h2>

<p>
We've successfully configured Active Directory on our domain controller. We established our infrastructure by creating a forest and administrator account. In the upcoming project, we'll be configuring the network services on our domain controller to allow our devices to conect to the internet.</p>



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
