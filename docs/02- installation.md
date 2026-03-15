# OpenVAS Installation Guide

## Supported Operating Systems

  As mentioned in the [Overview](01-openvas-overview.md) section although there are     workarounds to run OpenVAS from a Windows environment, such as using virtual          machines or similar solutions, the tool is designed to run natively on Linux          systems. OpenVAS can be installed directly on several Linux distributions. The most   commonly   used ones are:
  
    - Kali Linux
    - Ubuntu / Debian
    - Parrot OS
    
  These distributions provide the necessary dependencies and package repositories       required to install and run the Greenbone Vulnerability Management components.

## Install GVM
1. sudo apt update
<p align="center">
  <img src="../screenshots/aptinstall.png" width="700">
  <br>
  <em>OpenVAS installation process</em>
</p>

sudo apt install gvm

## Setup OpenVAS

sudo gvm-setup

This process:

- downloads vulnerability feeds
- initializes the database
- creates certificates
- creates the admin user

## Start the service

sudo gvm-start

The web interface is available at:

https://127.0.0.1:9392
