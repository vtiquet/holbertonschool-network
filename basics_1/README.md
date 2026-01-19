<div align="center"><img src="https://github.com/vtiquet/holbertonschool-resources/blob/main/image/Holberton-Logo.svg" width=40% height=40%/></div>

# Resources

## Table of Contents :

  - [0. Change your home IP](#subparagraph0)
  - [1. Show attached IPs](#subparagraph1)
  - [2. Port listening on localhost](#subparagraph2)

## Resources
### Read or watch:
* [What is localhost](/rltoken/7n2kKjq50U_Uv-TrEK-NUA)
* [What is 0.0.0.0](/rltoken/1efC1iImna8ubDSgokLbpQ)
* [What is the hosts file](/rltoken/6o7mmDL8joIrC5DXNRSnKw)
* [Netcat examples](/rltoken/_TN2G4Djh-f7MSukzToXpw)

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:
* What is localhost/127.0.0.1
* What is 0.0.0.0
* What is/etc/hosts
* How to display your machine’s active network interfaces

## Requirements
### General
* Allowed editors:vi,vim,emacs
* All your files will be interpreted on Ubuntu 22.04
* All your files should end with a new line
* AREADME.mdfile, at the root of the folder of the project, is mandatory
* All your Bash script files must be executable
* Your Bash script must passShellcheck(version0.7.0viaapt-get) without any errors
* The first line of all your Bash scripts should be exactly#!/usr/bin/env bash
* The second line of all your Bash scripts should be a comment explaining what is the script doing

## Task
### 0. Change your home IP <a name='subparagraph0'></a>

Write a Bash script that configures an Ubuntu server with the below requirements.

Requirements:

* <p><code>localhost</code> resolves to <code>127.0.0.2</code></p>
* <p><code>facebook.com</code> resolves to <code>8.8.8.8</code>.</p>

Example:

```
sylvain@ubuntu$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms
^C
--- localhost ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.012/0.012/0.012/0.000 ms
sylvain@ubuntu$
sylvain@ubuntu$ ping facebook.com
PING facebook.com (157.240.11.35) 56(84) bytes of data.
64 bytes from edge-star-mini-shv-02-lax3.facebook.com (157.240.11.35): icmp_seq=1 ttl=63 time=15.4 ms
^C
--- facebook.com ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 15.432/15.432/15.432/0.000 ms
sylvain@ubuntu$
sylvain@ubuntu$ sudo ./0-change_your_home_IP
sylvain@ubuntu$
sylvain@ubuntu$ ping localhost
PING localhost (127.0.0.2) 56(84) bytes of data.
64 bytes from localhost (127.0.0.2): icmp_seq=1 ttl=64 time=0.012 ms
64 bytes from localhost (127.0.0.2): icmp_seq=2 ttl=64 time=0.036 ms
^C
--- localhost ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1000ms
rtt min/avg/max/mdev = 0.012/0.024/0.036/0.012 ms
sylvain@ubuntu$
sylvain@ubuntu$ ping facebook.com
PING facebook.com (8.8.8.8) 56(84) bytes of data.
64 bytes from facebook.com (8.8.8.8): icmp_seq=1 ttl=63 time=8.06 ms
^C
--- facebook.com ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 8.065/8.065/8.065/0.000 ms
```

In this example we can see that:

* <p>before running the script, <code>localhost</code> resolves to <code>127.0.0.1</code> and <code>facebook.com</code> resolves to <code>157.240.11.35</code></p>
* <p>after running the script,  <code>localhost</code> resolves to <code>127.0.0.2</code> and <code>facebook.com</code> resolves to <code>8.8.8.8</code></p>

If you’re running this script on a machine that you’ll continue to use, be sure to revert <code>localhost</code> to <code>127.0.0.1</code>. Otherwise, a lot of things will stop working!

---

### 1. Show attached IPs <a name='subparagraph1'></a>

Write a Bash script that displays all active IPv4 IPs on the machine it’s executed on.

Example:

```
sylvain@ubuntu$ ./1-show_attached_IPs | cat -e
10.0.2.15$
127.0.0.1$
sylvain@ubuntu$
```

Obviously, the IPs displayed may be different depending on which machine you are running the script on.

Note that we can see our <code>localhost</code> IP :)

---

### 2. Port listening on localhost <a name='subparagraph2'></a>

Write a Bash script that listens on port <code>98</code> on <code>localhost</code>.

<strong>Terminal 0</strong>

Starting my script.

```
sylvain@ubuntu$ sudo ./2-port_listening_on_localhost
```

<strong>Terminal 1</strong>

Connecting to <code>localhost</code> on port <code>98</code> using <code>telnet</code> and typing some text.

```
sylvain@ubuntu$ telnet localhost 98
Trying 127.0.0.2...
Connected to localhost.
Escape character is '^]'.
Hello world
test
```

<strong>Terminal 0</strong>

Receiving the text on the other side.

```
sylvain@ubuntu$ sudo ./2-port_listening_on_localhost
Hello world
test
```

For the sake of the exercise, this connection is made entirely within <code>localhost</code>. This isn’t really exciting as is, but we can use this script across networks as well. Try running it between your local PC and your remote server for fun!

As you can see, this can come in very handy in a multitude of situations. Maybe you’re debugging socket connection issues, or you’re trying to connect to a software and you are unsure if the issue is the software or the network, or you’re working on firewall rules… Another tool to add to your debugging toolbox!

---


## Authors
vtiquet - [GitHub Profile](https://github.com/vtiquet)
