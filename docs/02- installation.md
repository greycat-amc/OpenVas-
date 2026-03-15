# OpenVAS Installation Guide

## Supported Operating Systems

OpenVAS, which is part of the Greenbone Vulnerability Management (GVM) framework, is designed to run on Linux systems. There is currently no official native version available for Windows.

### Installation on Linux

OpenVAS can be installed directly on several Linux distributions. The most commonly used ones are:

- Kali Linux
- Ubuntu / Debian
- Parrot OS

These distributions provide the necessary dependencies and package repositories required to install and run the Greenbone Vulnerability Management components.

## Install GVM

sudo apt update
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
