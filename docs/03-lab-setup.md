

# Lab Setup
The purpose of this laboratory is to demonstrate how a vulnerability scanner can identify security weaknesses in a vulnerable system. The goal of the lab is to perform a vulnerability scan against the Metasploitable system using OpenVAS.

## 1. Machines Used in the Lab

  ### Scanner Machine

- Operating System: Kali Linux
- Network configuration: NAT Network (VirtualBox)
- Tool: OpenVAS / Greenbone Vulnerability Manager
- Role: Vulnerability scanner
<p align="center">
  <img src="../screenshots/kalired.png" width="700">
  <br>
  <em>Kali Network Configurationt</em>
</p>

  ### Target Machine

- Operating System: Metasploitable 2
- Network configuration: NAT Network (VirtualBox)
- Role: Vulnerable target system used for security testing

Metasploitable is an intentionally vulnerable virtual machine designed for security training and penetration testing exercises. Instructions for downloading and configuring the Metasploitable2 machine can be found in the [Lab Setup > Metasploitable2 Installation and Configuration](07-troubleshooting.md) section.

<p align="center">
  <img src="../screenshots/metasploitred.png" width="700">
  <br>
  <em>Metasploitable2 Network Configurationt</em>
</p>

## 2. Laboratory Environment

The laboratory environment consists of two virtual machines connected to the same network. Both machines are configured within the same **NAT Network in VirtualBox**, enabling communication between the vulnerability scanner and the target system.

- **Kali Linux**: attacker machine used to install and run OpenVAS.
- **Metasploitable 2**: intentionally vulnerable machine used as the scan target.

<p align="center">
  <img src="../screenshots/Esquema Lab.png" width="700">
  <br>
  <em>Laboratory Diagram</em>
</p>


## 3.  Network Verification

Before starting the vulnerability scan, it is necessary to identify the IP address assigned to the target virtual machine within the network. This can be done using standard network commands such as `ip a` or `ifconfig` on each machine. However, in this case, the Nmap host discovery function will be used to identify active hosts in the network, simulating a real-world environment.

<p align="center">
  <img src="../screenshots/kaliip.png" width="700">
  <br>
  <em>Kali IP</em>
</p>

<p align="center">
  <img src="../screenshots/metaip.png" width="700">
  <br>
  <em>Nmap Discovery Function</em>
</p

Once the IP address of the target system (Metasploitable2) has been identified (10.0.2.7), connectivity between the scanner and the target should be verified.

For this purpose, a simple `ping` command can be executed from the Kali Linux machine to confirm that both systems can communicate within the same network.
<p align="center">
  <img src="../screenshots/ping.png" width="700">
  <br>
  <em>Comunication Check</em>
</p

 At this point, the environment is ready and the vulnerability scan can be configured.
