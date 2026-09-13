# Task 2: Basic Firewall Configuration Using UFW

## Objective

The objective of this task is to configure and verify a basic firewall using UFW in Kali Linux.

## Tools Used

- Kali Linux
- WSL2
- UFW - Uncomplicated Firewall

## Firewall Configuration

The following firewall rules were configured:

- Deny incoming connections by default
- Allow outgoing connections by default
- Allow SSH traffic on port 22
- Enable firewall logging
- Enable the UFW firewall

## Commands Used

```bash
sudo apt update
sudo apt install -y ufw
sudo ufw status verbose
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw enable
sudo ufw status verbose