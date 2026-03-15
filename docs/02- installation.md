# OpenVAS Installation Guide

## Supported Operating Systems

  As mentioned in the [Overview](01-openvas-overview.md) section although there are     workarounds to run OpenVAS from a Windows environment, such as using virtual          machines or similar solutions, the tool is designed to run natively on Linux          systems. OpenVAS can be installed directly on several Linux distributions. The most   commonly   used ones are:
  
    - Kali Linux
    - Ubuntu / Debian
    - Parrot OS
    
  These distributions provide the necessary dependencies and package repositories       required to install and run the Greenbone Vulnerability Management components.

## 1. Update Package List

````markdown
kali@kali:~$ sudo apt install gvm
---

This command updates the list of available packages on the system.The system queries the Linux repositories and downloads the most recent list of available software.
This command does not install any software yet, but ensures that the latest versions of packages are available before installing new software.

<p align="center">
  <img src="../screenshots/aptinstall.png" width="700">
  <br>
  <em>Update Package List</em>
</p>

## 2. Install Greenbone Vulnerability Manager (GVM)

sudo apt install gvm

This command installs the Greenbone Vulnerability Management framework, which includes:

  -OpenVAS Scanner
  
  -Greenbone Vulnerability Manager (gvmd) 
  
  -Greenbone Security Assistant (web interface)
  
  -vulnerability test plugins (VTs)
  
All required dependencies are automatically installed during this process.

<p align="center">
  <img src="../screenshots/aptinstallopenvas.png" width="700">
  <br>
  <em>OpenVAS installation process</em>
</p>
