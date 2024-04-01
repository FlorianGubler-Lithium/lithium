# Cluster Configuration
This document covers the entire cluster configuration of the lithium raspberry pi home cluster. 

## IP Concept
<b>DHCP Range</b>: 192.168.1.101 - 192.168.1.220<br>
<b>Cluster Range</b>: 192.168.1.20 - 192.168.1.30<br>
<b>MetalLB</b>: 192.168.1.31 - 192.168.1.100<br><br>
Network details can br viewed in the [Swisscom Cockpit](internetbox.swisscom.ch)

## Raspberry Pi Hosts
| Hostname    | IP-Address    | Rasp Version      | OS Version |
| ----------- | ------------- | ----------------- | ---------- |
| rasp-one    | 192.168.1.20  | 4 Model B - 4GB   | Deb 12.5   |
| rasp-two    | 192.168.1.21  | 4 Model B - 4GB   | Deb 12.5   |
| rasp-three  | 192.168.1.22  | 4 Model B - 4GB   | Deb 12.5   |
| rasp-four   | 192.168.1.23  | 2 Model B - 256MB | Deb 12.5   |
