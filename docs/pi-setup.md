# Raspberry Pi Setup Documentation (Debian)
## General setup
These steps must be done manual and cannot be automated with ansible.<br><br>
Basic Pi Setup See: [Debian Setup Doc](https://raspberrytips.com/install-debian-on-raspberry-pi/)<br><br>
Dont forget to configure a static IP with the IP concept. This can be done as following:
1. Got to network interface config for ethernet:
```
nano /etc/network/interfaces.d/eth0
```
2. Configure static IP
```
auto eth0
iface eth0 inet static
    address <YOUR IP>
    netmask 255.255.255.0
    gateway 192.168.1.1
    dns-nameservers 1.1.1.1 8.8.8.8
```
3. Set hostname
```
nano /etc/hostname
```
```
nano /etc/hosts
```
4. Reboot server
```
reboot
```

