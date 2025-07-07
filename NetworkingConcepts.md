ARP: Address Resolution Protocol

Maps IP addresses to MAC addresses on local network.
Its a reason behind we can use network in LAN. Can see via "arp -a" command.

DNS Resolution: Translates the domain names to an IP address.
Command: nslookup <domain_name>
Command: dig <domain_name>

IP Address (Internet Protocol address): A unique address that identifies the device over the network.
IP address devided into two parts: x1.x2.x3.x4
1. [x1.x2.x3] is the network ID
2. [x4] is the Host ID

Vesions of IP Address: 

1. IPV4: First version of IP address. The address size of IPV4 is a 32-bit number. Internet Protocol security (IPSec) for network security is optional.
2. IPV6: Recent version of IP address. The address size of IPV6 is a 128-bit number.  Internet Protocol security (IPSec) for network security is mandatory.

Types of IP addresses:

1. Public: Public IP address is accessed over the internet. The public IP address is a different international IP address assigned to a computer device. It is the IP address that assigned by ISP (Internet service provider). This is what websites like whatismyip.com show.

2. Private: Private IP address is used within a private network. The private IP address is a local IP address assigned to a computer device. This IP address not visible to internet. It can be seen via "ipconfig" command.

3. Static: IP address that never change. It can be manually assigned or reserved.

4. Dynamic:  IP address that changes. It is assigned by DHCP (Dynamic Host Configuration Protocol) server. The IP address is leased for a specific period of time. The lease time can be configured on the DHCP server.Your ISP might also give your home a dynamic public IP, which can change over time.

5. Loopback: Used by your computer to talk to itself. It is always "127.0.0.1".

6. Reserved: Special-purpose IPs not used for normal traffic. Like 0.0.0.0 , 255.255.255.255
