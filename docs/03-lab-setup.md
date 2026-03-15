

# Lab Setup
The purpose of this laboratory is to demonstrate how a vulnerability scanner can identify security weaknesses in a vulnerable system. The goal of the lab is to perform a vulnerability scan against the Metasploitable system using OpenVAS.

## Machines Used in the Lab

### Scanner Machine

- Operating System: Kali Linux
- Network Configuration: NAT Network
- Tool: OpenVAS / Greenbone Vulnerability Manager
- Role: Vulnerability scanner

<p align="center">
  <img src="../screenshots/network-topology.png" width="700">
</p>

### Target Machine

- Operating System: Metasploitable 2
- 
- Role: Vulnerable target system used for security testing

Metasploitable is an intentionally vulnerable virtual machine designed for security training and penetration testing exercises.

## Laboratory Environment

The laboratory environment consists of two virtual machines running in the same network, to allow communication between the scanner and the target.

- **Kali Linux**: attacker machine used to install and run OpenVAS.
- **Metasploitable 2**: intentionally vulnerable machine used as the scan target.

<p align="center">
  <img src="../screenshots/network-topology.png" width="700">
</p>

## Comprobaciones de que el laboratorio funicona
