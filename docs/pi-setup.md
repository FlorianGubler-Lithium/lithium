# Raspberry Pi Setup Documentation (Debian)
## General setup
These steps must be done manual and cannot be automated with ansible.<br><br>
See: [Debian Setuo Doc](https://raspberrytips.com/install-debian-on-raspberry-pi/)<br>
Dont forget to configure a static IP with the IP concept. This can be done as following:
1. Got to network interface config for ethernet:
```
sudo nano /etc/network/interfaces
```
2. Configure static IP
```
auto eth0
iface eth0 inet static
    address <YOUR IP>
    netmask 255.255.255.0
    gateway 192.168.1.1
    dns-nameservers 8.8.8.8 8.8.4.4
```
3. Reboot or restart networking service
```
sudo reboot
```
or
```
sudo systemctl restart networking
```
