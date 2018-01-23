# Network Analysis Tools

## ipconfig / ifconfig

ipconfig (Windows)
ifconfig (OS X/Linux)

ipconfig is used to determine the current machine's IP configuration. It returns the IPv4 address, the subnet mask, and the default gateway.

Here's a sample output on Windows 10:

```
C:\Users\RadamanthusBatnag>ipconfig

Windows IP Configuration


Wireless LAN adapter Wi-Fi:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 1:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::c001:92f6:6d2d:7c58%14
   IPv4 Address. . . . . . . . . . . : 192.168.1.111
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1

Ethernet adapter Bluetooth Network Connection:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Tunnel adapter Teredo Tunneling Pseudo-Interface:

   Connection-specific DNS Suffix  . :
   IPv6 Address. . . . . . . . . . . : 2001:0:9d38:6abd:3059:1f1e:49ed:2ab5
   Link-local IPv6 Address . . . . . : fe80::3059:1f1e:49ed:2ab5%9
   Default Gateway . . . . . . . . . : ::
```

_Exercise: Run ipconfig on your machine. What is your machine's IP address and subnet mask? Compare it with your seatmate._

## ping

ping is used to determine network connectivity to a specific host. It also gives a rough idea of the network connection speed to the specified target host.

```
C:\Users\RadamanthusBatnag>ping www.github.com

Pinging github.com [192.30.255.112] with 32 bytes of data:
Reply from 192.30.255.112: bytes=32 time=207ms TTL=53
Reply from 192.30.255.112: bytes=32 time=205ms TTL=53
Reply from 192.30.255.112: bytes=32 time=205ms TTL=53
Reply from 192.30.255.112: bytes=32 time=204ms TTL=53

Ping statistics for 192.30.255.112:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 204ms, Maximum = 207ms, Average = 205ms
```

_Exercise: ping the following web sites:
- www.telkom.co.za (South African telecommunications company)
- www.singtel.sg (a Singaporean telecommunications company)
- www.pldt.com.ph
- www.att.com (a US telecommunications company)
Rank the four web sites according to speed, in descending order.
What do you think accounts for the differences in speed?
_

## traceroute

## host

## whois

## netstat
