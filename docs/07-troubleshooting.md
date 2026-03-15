# OpenVAS Installation > Setup Check Issue
When running gvm-check-setup, if any issue is detected, the tool provides recommendations on how to resolve it. In our case, two issues were identified:  

1 A problem related to PostgreSQL where the database was reported as **"does not exist"**. 
<p align="center">
  <img src="../screenshots/gvmchecksetuppostgres.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>


  The suggested solution was to recreate or initialize the PostgreSQL database used by GVM.
    
````markdown
kali@kali:~$ sudo runuser -u postgres -- /usr/share/gvm/create-postgresql-database
````
<p align="center">
  <img src="../screenshots/gvmchecksetuppostgres_solve.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>

2. The absence of a user account required to access the web interface.

<p align="center">
  <img src="../screenshots/gvmchecksetupuser.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>

  In this case, it is necessary to create an administrator user in order to log in to the platform.

````markdown
kali@kali:~$ sudo runuser -u _gvm -- gvmd --creat-user=admin --password=openvas
````

<p align="center">
  <img src="../screenshots/gvmchecksetupuser_solved.png" width="700">
  <br>
  <em>OpenVAS check setup</em>
</p>

For additional issues, please refer to the [official documentation](https://greenbone.github.io/docs/latest/22.4/kali/troubleshooting.html).

-----

# Lab Setup > Metasploitable2 Installation and Configuration
Metasploitable is an intentionally vulnerable Linux virtual machine. This VM can be used to conduct security training, test security tools, and practice common penetration testing techniques. 
  First, we download the Metasploitable2 virtual machine from the SourceForge website. The URL is https://sourceforge.net/projects/metasploitable/files/Metasploitable2/
The default login and password is msfadmin:msfadmin.

<p align="center">
  <img src="../screenshots/descarga.png" width="700">
  <br>
</p>

  In VirtualBox, we create a new virtual machine with the following configuration:

  - **VM Name:** MetasploitLab  
  - **OS:** Linux  
  - **OS Distribution:** Ubuntu
  - **OS Version:** Ubuntu (32-bit)

<p align="center">
  <img src="../screenshots/configuremv.png" width="700">
  <br>
</p

  Once the virtual machine has been created, we go to **Settings** and review the default configuration.  
  First, we modify the number of CPUs and set it to **2**.

<p align="center">
  <img src="../screenshots/cpus.png" width="700">
  <br>
</p


  Next, we review the Storage configuration, which determines the device from which the virtual machine will boot. As shown in the image, the system currently includes two storage controllers: an IDE controller with an empty optical drive and a SATA controller containing the virtual disk file MetasploitLab.vdi.

<p align="center">
  <img src="../screenshots/almacenamientodefecto.png" width="700">
  <br>
</p


This configuration will not work correctly for our lab because Metasploitable2 is distributed as a preconfigured virtual disk in .vmdk format, not as a .vdi disk created during the VM wizard. Therefore, the machine will not boot into the intended vulnerable environment. To correct this configuration, we first remove the IDE controller, which is unnecessary in this setup. 

<p align="center">
  <img src="../screenshots/borrarcontroleride.png" width="700">
  <br>
</p

Then, under the SATA controller, we replace the existing .vdi disk with the Metasploitable2 .vmdk file previously downloaded. This ensures that the virtual machine boots directly from the Metasploitable2 disk image containing the intentionally vulnerable system used in the laboratory.


<p align="center">
  <img src="../screenshots/borrarvdi.png" width="700">
  <br>
</p

Add .vmdk

<p align="center">
  <img src="../screenshots/añadirvmdk.png" width="700">
  <br>
</p

  After applying these modifications, the configuration is correct and ensures that the virtual machine boots directly from the Metasploitable2 disk image containing the intentionally vulnerable system used in this laboratory.


<p align="center">
  <img src="../screenshots/almacenamientook.png" width="700">
  <br>
</p

  Finally,we configure the network adapter as a NAT Network to allow the laboratory environment to be deployed.

<p align="center">
  <img src="../screenshots/metasploitred.png" width="700">
  <br>
</p



  
-----


# Scan Configuration > Feed Owner Issue

While creating a new target in OpenVAS, the following error message may appear:
“The feed owner is currently not set. This issue may be due to the feed not having completed its synchronization. Please try again shortly.”

<p align="center">
  <img src="../screenshots/issue.png" width="700">
  <br>
</p

This error occurs when the Greenbone feed has not been properly initialized or the feed owner has not been configured. As a result, OpenVAS does not allow the creation of new targets.

To resolve this issue, the feed owner must be assigned manually.  First, we obtain the UUID of the available users using:
````markdown
kali@kali:~$ sudo gvmd --get-users --verbose
````

<p align="center">
  <img src="../screenshots/uuidadmin.png" width="700">
  <br>
</p

Then we assign the administrator as the feed owner with the following command:

````markdown
kali@kali:~$ sudo gvmd --modify-setting 78eceaec-3385-11ea-b237-28d24461215b --value 009bd7bb-e708-42ce-9fb9-14f1f5c5314d
````
Note: Feed Owner UUID in GVM is 78eceaec-3385-11ea-b237-28d24461215b.
<p align="center">
  <img src="../screenshots/adminuevo.png" width="700">
  <br>
</p

After applying this configuration, it is possible to create targets normally in OpenVAS.
