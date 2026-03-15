

# Lab Setup
The purpose of this laboratory is to demonstrate how a vulnerability scanner can identify security weaknesses in a vulnerable system. The goal of the lab is to perform a vulnerability scan against the Metasploitable system using OpenVAS.

## Machines Used in the Lab

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

Metasploitable is an intentionally vulnerable virtual machine designed for security training and penetration testing exercises. Instructions for downloading and configuring the Metasploitable2 machine can be found in the [Lab Setup > Metasploitable2 Installation and Configuration](06-troubleshooting.md) section.

<p align="center">
  <img src="../screenshots/metasploitred.png" width="700">
  <br>
  <em>Metasploitable2 Network Configurationt</em>
</p>

## Laboratory Environment

The laboratory environment consists of two virtual machines connected to the same network. Both machines are configured within the same **NAT Network in VirtualBox**, enabling communication between the vulnerability scanner and the target system.

- **Kali Linux**: attacker machine used to install and run OpenVAS.
- **Metasploitable 2**: intentionally vulnerable machine used as the scan target.

<p align="center">
  <img src="../screenshots/Esquema Lab.png" width="700">
  <br>
  <em>Laboratoy Diagram</em>
</p>

## Comprobaciones de que el laboratorio funicona
