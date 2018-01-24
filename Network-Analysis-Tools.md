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

### Exercise

Run ipconfig on your machine. What is your machine's IP address and subnet mask? Compare it with your seatmate.

## ping

ping is used to determine network connectivity to a specific host. It also gives a rough idea of the network connection speed to the specified target host.

Syntax:
`ping <target hostname or IP address>`

Example:
`ping www.github.com`

Sample output:

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

### Exercise

Get your seatmate's IP address and ping it. What was the ping latency?

ping the following web sites:

- www.telkom.co.za (South African telecommunications company)
- www.singtel.sg (a Singaporean telecommunications company)
- www.pldt.com.ph (a Philippine telecommunications company)
- www.att.com (a US telecommunications company)

Rank the four web sites according to speed, in descending order.
What do you think accounts for the differences in speed?

## tracert / traceroute

tracert (Windows)
traceroute (OS X/ Linux)

traceroute is used to trace the network route from the originating machine into the target machine. If possible, it shows the network connection speed for each hop.

Syntax:
`traceroute <target hostname or IP address`

Example:
`traceroute www.att.com`

Sample output:

```
C:\Users\RadamanthusBatnag>tracert www.att.com

Tracing route to e11697.dscx.akamaiedge.net [23.15.100.59]
over a maximum of 30 hops:

  1    <1 ms    <1 ms    <1 ms  192.168.1.1
  2    <1 ms    <1 ms    <1 ms  192.168.0.1
  3     *        *        *     Request timed out.
  4     9 ms     9 ms     9 ms  172.31.64.1
  5     9 ms     9 ms     8 ms  130.105.0.24
  6    38 ms    38 ms    42 ms  akamai.sgix.sg [103.16.102.77]
  7    36 ms    36 ms    36 ms  a23-15-100-59.deploy.static.akamaitechnologies.com [23.15.100.59]

Trace complete.
```

### Exercise
Do a traceroute for each of the four websites you pinged in the previous exercise. Which has the most, and which has the least number of hops? For each traceroute, identify the bottleneck (takes the longest time) hop.

## whois

whois is not installed by default on Windows, but can be installed by downloading https://docs.microsoft.com/en-us/sysinternals/downloads/whois.

You can also use the free online tool, https://www.whois.com/whois/.

Syntax:
Windows command line tool: `whois <ip address>`
Online tool: https://www.whois.com/whois/<ip address>

Example:
Windows command line: `whois 130.105.0.18`
Online tool:  https://www.whois.com/whois/130.105.0.18

Sample output for https://www.whois.com/whois/130.105.0.18:

```
% [whois.apnic.net]
% Whois data copyright terms    http://www.apnic.net/db/dbcopyright.html

% Information related to '130.105.0.0 - 130.105.0.255'

% Abuse contact for '130.105.0.0 - 130.105.0.255' is 'email@skybroadband.com.ph'

inetnum:        130.105.0.0 - 130.105.0.255
netname:        SKYBB8-PH
descr:          SKYBROADBAND
country:        PH
admin-c:        EF2049-AP
tech-c:         EF2049-AP
status:         ALLOCATED NON-PORTABLE
mnt-by:         MAINT-PH-SKYBB
mnt-irt:        IRT-SKYBB-PH
mnt-lower:      MAINT-PH-SKYBB
mnt-routes:     MAINT-PH-SKYBB
last-modified:  2015-07-06T03:56:16Z
source:         APNIC

irt:            IRT-SKYBB-PH
address:        SKYCABLE Building
address:        409 Ibanez Cor P Guevarra St
address:        San Juan MM
address:        Philippines 1600
e-mail:         email@skybroadband.com.ph
abuse-mailbox:  email@skybroadband.com.ph
admin-c:        EMF1-AP
tech-c:         EMF1-AP
auth:           # Filtered
mnt-by:         MAINT-PH-SKYBB
last-modified:  2016-10-10T00:05:26Z
source:         APNIC

person:         Eugene Flores
address:        409 P. Guevarra cor. Ibanez St,
address:        Little Baguio, San Juan City
country:        PH
phone:          +632-726-9873
e-mail:         email@skycable.com
nic-hdl:        EF2049-AP
mnt-by:         MAINT-PH-DESTINY1
last-modified:  2014-05-20T04:18:31Z
source:         APNIC

% Information related to '130.105.0.0/24AS23944'

route:          130.105.0.0/24
descr:          SKYBroadband
origin:         AS23944
mnt-by:         MAINT-PH-SKYBB
last-modified:  2015-07-06T03:23:09Z
source:         APNIC

% This query was served by the APNIC Whois Service version 1.88.15-43 (WHOIS-US3)
```

### Exercise
For each of the hops in the traceroute output to www.singtel.sg, run a whois. Determine the location (country) of each IP address in the hop. Do the same analysis for the traceroute output to www.att.com. Based on your analysis, explain which network connection is faster, and why.

## netstat

netstat shows the open connections to and from the machine.

Sample output:

```
C:\Users\RadamanthusBatnag>netstat

Active Connections

  Proto  Local Address          Foreign Address        State
  TCP    127.0.0.1:49740        DESKTOP-N1CR2G2:49741  ESTABLISHED
  TCP    127.0.0.1:49741        DESKTOP-N1CR2G2:49740  ESTABLISHED
  TCP    127.0.0.1:49742        DESKTOP-N1CR2G2:49743  ESTABLISHED
  TCP    127.0.0.1:49743        DESKTOP-N1CR2G2:49742  ESTABLISHED
  TCP    127.0.0.1:49744        DESKTOP-N1CR2G2:49745  ESTABLISHED
  TCP    127.0.0.1:49745        DESKTOP-N1CR2G2:49744  ESTABLISHED
  TCP    127.0.0.1:49879        DESKTOP-N1CR2G2:49880  ESTABLISHED
  TCP    127.0.0.1:49880        DESKTOP-N1CR2G2:49879  ESTABLISHED
  TCP    127.0.0.1:50137        DESKTOP-N1CR2G2:50138  ESTABLISHED
  TCP    127.0.0.1:50138        DESKTOP-N1CR2G2:50137  ESTABLISHED
  TCP    127.0.0.1:50145        DESKTOP-N1CR2G2:50146  ESTABLISHED
  TCP    127.0.0.1:50146        DESKTOP-N1CR2G2:50145  ESTABLISHED
  TCP    192.168.1.111:49973    130.105.56.121:https   ESTABLISHED
  TCP    192.168.1.111:49974    130.105.56.121:https   ESTABLISHED
  TCP    192.168.1.111:50105    hk2sch130020721:https  ESTABLISHED
  TCP    192.168.1.111:50110    153.254.86.143:27020   ESTABLISHED
  TCP    192.168.1.111:50669    43.251.41.28:https     ESTABLISHED
  TCP    192.168.1.111:50732    hkg12s16-in-f10:https  TIME_WAIT
  TCP    192.168.1.111:50733    server-52-222-238-3:https  ESTABLISHED
  TCP    192.168.1.111:50734    111.221.29.254:https   ESTABLISHED
```

### Exercise

Run `netstat` on your machine. You might need to press Ctrl-C to stop netstat. 

From the netstat output, what are the remote machines that you're connecting to? 
