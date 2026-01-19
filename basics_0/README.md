<div align="center"><img src="https://github.com/vtiquet/holbertonschool-resources/blob/main/image/Holberton-Logo.svg" width=40% height=40%/></div>

# Resources

## Table of Contents :

  - [0. OSI model](#subparagraph0)
  - [1. Types of network](#subparagraph1)
  - [2. MAC and IP address](#subparagraph2)
  - [3. UDP and TCP](#subparagraph3)
  - [4. TCP and UDP ports](#subparagraph4)
  - [5. Is the host on the network](#subparagraph5)

## Resources
### Read or watch:
* [OSI model](/rltoken/0gZBJLBZ0DVlkVIsZek1Cg)
* [Different types of network](/rltoken/uhwKSwkglP91KoNRsqj33g)
* [LAN network](/rltoken/AY_BwkDbIntiUUEzzAOYpw)
* [WAN network](/rltoken/UlbohQRQTWFbcOKGN36D3g)
* [Internet](/rltoken/vV8mtIuKF8oMktJeS7o06w)
* [MAC address](/rltoken/uCjZlyba4pa0vjcFOc_HWg)
* [What is an IP address](/rltoken/SBU_OXL5nGyhkiPWDqBL8Q)
* [Private and public address](/rltoken/Si0prYb_5y_cCLCqf395TQ)
* [IPv4 and IPv6](/rltoken/-CJ08KJ1fgGd5TaBVtxvjw)
* [Localhost](/rltoken/IA3wOeXxbQFuwhWutfH3Cw)
* [TCP and UDP](/rltoken/M4UIOFvUfdzrggyY9rwliw)
* [TCP/UDP ports List](/rltoken/cS-GlmuJlLCth1uWA6VeKA)
* [What is ping /ICMP](/rltoken/tjQjQ3agyLJeWc4XLYYXVA)
* [Positional parameters](/rltoken/oQGsRVbeISPfys8EG2Oetw)

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
* What it is
* How many layers it has
* How it is organized

## Requirements
### General
* Allowed editors:vi,vim,emacs
* All your Bash script files will be interpreted on Ubuntu 22.04
* All your files should end with a new line
* AREADME.mdfile, at the root of the folder of the project, is mandatory
* All your Bash script files must be executable
* Your Bash script must passshellcheckwithout any error
* The first line of all your Bash scripts should be exactly#!/usr/bin/env bash
* The second line of all your Bash scripts should be a comment explaining what is the script doing

## Task
### 0. OSI model <a name='subparagraph0'></a>

OSI (Open Systems Interconnection) is an abstract model to describe layered communication and computer network design. The idea is to segregate the different parts of what make communication possible.

It is organized from the lowest level to the highest level:

* <p>The lowest level: layer 1 which is for transmission on physical layers with electrical impulse, light or radio signal</p>
* <p>The highest level: layer 7 which is for application specific communication like SNMP for emails, HTTP for your web browser, etc</p>

Keep in mind that the OSI model is a concept, it’s not even tangible. The OSI model doesn’t perform any functions in the networking process.

It is a conceptual framework so we can better understand complex interactions that are happening.

Most of the functionality in the OSI model exists in all communications systems.

<img alt="" loading="lazy" src="https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/medias/2018/6/4e6a0ad87a65d7054248.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20260119%2Feu-west-3%2Fs3%2Faws4_request&amp;X-Amz-Date=20260119T082026Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=5679d2264647bc0dfc37e737ffa487dd2645a8c3a79b236524a9fa8ccee8720f" style=""/>

In this project we will mainly focus on:

* <p>The Transport layer and especially TCP/UDP</p>
* <p>On the Network layer with IP and ICMP</p>

The image bellow describes more concretely how you can relate to every level.

<img alt="" loading="lazy" src="https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/medias/2020/9/0fc96bd99faa7941b18bcae4c5f90c6acd11791d.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20260119%2Feu-west-3%2Fs3%2Faws4_request&amp;X-Amz-Date=20260119T082026Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=90c56461961401ccb46f03755a0cd90aeb0d4717fd65bf013cc39964a71bb573" style=""/>

Questions:

What is the OSI model?

How is the OSI model organized?

---

### 1. Types of network <a name='subparagraph1'></a>

<img alt="" loading="lazy" src="https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/medias/2020/9/4b995d4f8078b44afa968d68a98035d2bd7e8fac.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20260119%2Feu-west-3%2Fs3%2Faws4_request&amp;X-Amz-Date=20260119T082026Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=e97e7485d1debedf1795ff1327436f72cf4822b34d791e81783beea226c24b84" style=""/>

LAN connect local devices together, WAN connects LANs together, and WANs are operating over the Internet.

Questions:

What type of network a computer in local is connected to?

What type of network could connect an office in one building to another office in a building a few streets away?

What network do you use when you browse www.google.com from your smartphone (not connected to the Wifi)?

---

### 2. MAC and IP address <a name='subparagraph2'></a>

<img alt="" loading="lazy" src="https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/medias/2020/9/1e348ba3bcbb094b02922f821ffeb3d8c5438b7b.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20260119%2Feu-west-3%2Fs3%2Faws4_request&amp;X-Amz-Date=20260119T082026Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=a38a03f5b22c68f7982802501067f0847a18e4909dfcbfbe2274beb7c418bd34" style=""/>

Questions:

What is a MAC address?

What is an IP address?

---

### 3. UDP and TCP <a name='subparagraph3'></a>

<img alt="" loading="lazy" src="https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/medias/2020/9/3d92e3c4a470f8ecf4c73db511fcbbadaa002e1c.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20260119%2Feu-west-3%2Fs3%2Faws4_request&amp;X-Amz-Date=20260119T082026Z&amp;X-Amz-Expires=86400&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Signature=c350343729716ec31295a3637f9f3ef4398242a56698166ffddd376ff68278a1" style=""/>

Let’s fill the empty parts in the drawing above.

Questions:

* Which statement is correct for the TCP box:

* Which statement is correct for the UDP box:

* Which statement is correct for the TCP worker:

---

### 4. TCP and UDP ports <a name='subparagraph4'></a>

Once packets have been sent to the right network device using IP using either UDP or TCP as a mode of transportation, it needs to actually enter the network device.

If we continue the comparison of a network device to your house, where IP address is like your postal address, UDP and TCP ports are like the windows and doors of your place. A TCP/UDP network device has 65535 ports. Some of them are officially reserved for a specific usage, some of them are known to be used for a specific usage (but nothing is officially declared) and the rest are free of use.

While the full list of ports should not be memorized, it is important to know the most used ports, let’s start by remembering 3 of them:

* <p><strong>22</strong> for SSH</p>
* <p><strong>80</strong> for HTTP</p>
* <p><strong>443</strong> for HTTPS</p>

Note that a specific <a href="/rltoken/OAVRWajoWeUN6TcMNpI-Bg" target="_blank" title="IP + port = socket">IP + port = socket</a>.

Write a Bash script that displays listening ports:

* <p>That only shows listening sockets</p>
* <p>That shows the PID and name of the program to which each socket belongs</p>

Example:

```
sylvain@ubuntu$ sudo ./4-TCP_and_UDP_ports
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 *:sunrpc                *:*                     LISTEN      518/rpcbind
tcp        0      0 *:ssh                   *:*                     LISTEN      1240/sshd
tcp        0      0 *:32938                 *:*                     LISTEN      547/rpc.statd
tcp6       0      0 [::]:sunrpc             [::]:*                  LISTEN      518/rpcbind
tcp6       0      0 [::]:ssh                [::]:*                  LISTEN      1240/sshd
tcp6       0      0 [::]:33737              [::]:*                  LISTEN      547/rpc.statd
udp        0      0 *:sunrpc                *:*                                 518/rpcbind
udp        0      0 *:691                   *:*                                 518/rpcbind
udp        0      0 localhost:723           *:*                                 547/rpc.statd
udp        0      0 *:60129                 *:*                                 547/rpc.statd
udp        0      0 *:3845                  *:*                                 562/dhclient
udp        0      0 *:bootpc                *:*                                 562/dhclient
udp6       0      0 [::]:47444              [::]:*                              547/rpc.statd
udp6       0      0 [::]:sunrpc             [::]:*                              518/rpcbind
udp6       0      0 [::]:50038              [::]:*                              562/dhclient
udp6       0      0 [::]:691                [::]:*                              518/rpcbind
Active UNIX domain sockets (only servers)
Proto RefCnt Flags       Type       State         I-Node   PID/Program name    Path
unix  2      [ ACC ]     STREAM     LISTENING     7724     518/rpcbind         /run/rpcbind.sock
unix  2      [ ACC ]     STREAM     LISTENING     6525     1/init              @/com/ubuntu/upstart
unix  2      [ ACC ]     STREAM     LISTENING     8559     835/dbus-daemon     /var/run/dbus/system_bus_socket
unix  2      [ ACC ]     STREAM     LISTENING     9190     1087/acpid          /var/run/acpid.socket
unix  2      [ ACC ]     SEQPACKET  LISTENING     7156     378/systemd-udevd   /run/udev/control
sylvain@ubuntu$
```

---

### 5. Is the host on the network <a name='subparagraph5'></a>

<img alt="" loading="lazy" src="https://media.giphy.com/media/uDxkJAVSU7GY8/giphy.gif" style=""/>

The Internet Control Message Protocol (ICMP) is a protocol in the Internet protocol suite. It is used by network devices, to check if other network devices are available on the network. The command <code>ping</code> uses ICMP to make sure that a network device remains online or to troubleshoot issues on the network.

Write a Bash script that pings an IP address passed as an argument.

Requirements:

* <p>Accepts a string as an argument</p>
* <p>Displays <code>Usage: 5-is_the_host_on_the_network {IP_ADDRESS}</code> if no argument passed</p>
* <p>Ping the IP 5 times</p>

Example:

```
sylvain@ubuntu$ ./5-is_the_host_on_the_network 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=63 time=12.9 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=63 time=13.6 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=63 time=7.83 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=63 time=11.3 ms
64 bytes from 8.8.8.8: icmp_seq=5 ttl=63 time=7.57 ms

--- 8.8.8.8 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4006ms
rtt min/avg/max/mdev = 7.570/10.682/13.679/2.546 ms
sylvain@ubuntu$
sylvain@ubuntu$ ./5-is_the_host_on_the_network
Usage: 5-is_the_host_on_the_network {IP_ADDRESS}
sylvain@ubuntu$
```

It is interesting to look at the <code>time</code> value, which is the time that it took for the ICMP request to go to the <code>8.8.8.8</code> IP and come back to my host. The IP <code>8.8.8.8</code> is owned by Google, and the quickest roundtrip between my computer and Google was 7.57 ms which is pretty fast, which is a sign that the network path between my computer and Google’s datacenter is in good shape. A slow ping would indicate a slow network.

Next time you feel that your connection is slow, try the <code>ping</code> command to see what is going on!

---


## Authors
vtiquet - [GitHub Profile](https://github.com/vtiquet)
