# OpenVAS Installation Guide

The laboratory environment uses Kali Linux.

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
