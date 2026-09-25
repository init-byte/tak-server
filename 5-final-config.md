# Final Configuration & Client Setup
This page covers the final steps to make the server operational and connect clients.

## Configure Uncomplicated Firewall (UFW)

Install the Uncomplicated Firewall (UFW) management tool:
```
sudo apt install ufw
```
Reload the firewall's configuration:
```
sudo ufw reload
```
>⚠︎ Warning: For Raspberry Pi OS installs, please reboot your device after installing ufw. 

Check the current operational status and list of active rules for your firewall:
```
sudo ufw status
```

Set the firewall's default behavior to block all incoming network connections for enhanced security:
```
sudo ufw default deny incoming
```

Configure the firewall's default behavior to permit all outbound network connections from your server:

## Configure TAK Server Certificate


## Install Client Certificates on ATAK
