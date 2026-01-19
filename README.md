<div align="center"><img src="https://github.com/vtiquet/holbertonschool-resources/blob/main/image/Holberton-Logo.svg" width=40% height=40%/></div>

---

# Holberton School Networking

This repository contains introductory projects for understanding computer networking, ranging from conceptual frameworks like the OSI model to practical bash scripting for network configuration and debugging.

## 🛠 Project Structure

The repository is organized into two main sections:

* **`basics_0/`**: Fundamental networking concepts (OSI, protocols, and ports).
* **`basics_1/`**: Practical network administration and troubleshooting.

---

## 📚 Resource Summary & Task Mapping

### 1. Conceptual Frameworks (Basics 0)

The **OSI (Open Systems Interconnection) model** serves as a conceptual framework to understand complex network interactions. It is organized into 7 layers, from Physical (Layer 1) to Application (Layer 7).

* **Task 0: OSI Model**: Identified the organization and layering of the OSI model.
* **Task 1: Types of Network**: Distinguished between **LAN** (local devices), **WAN** (connecting LANs), and the **Internet**.
* **Task 2 & 3: Protocols & Addresses**: Explored **MAC** and **IP** addresses alongside the differences between **TCP** (connection-oriented) and **UDP** (connectionless).

### 2. Sockets and Ports

A **socket** is defined as the combination of an **IP address + Port**. Ports act like "windows and doors" to a device; there are 65,535 available, with some reserved for specific services like SSH (22) or HTTP (80).

* **Basics 0, Task 4**: A script to display active listening sockets, their PIDs, and associated programs.
* **Basics 1, Task 2**: Implementing a local listener on port 98 using `nc` (Netcat) to intercept incoming text.

### 3. Network Administration (Basics 1)

This section focuses on local machine configuration using the `/etc/hosts` file and interface management.

* **Task 0: Change your home IP**: Modifying the `/etc/hosts` file so that `localhost` resolves to `127.0.0.2` and `facebook.com` redirects to `8.8.8.8`.
* **Task 1: Show attached IPs**: Using `ifconfig` and text processing (`grep`, `awk`) to display only active IPv4 addresses.
* **Basics 0, Task 5**: Using the **ICMP** protocol via the `ping` command to verify if a host is online.

---

## 📝 General Requirements

* **Interpreter**: Ubuntu 22.04.
* **Formatting**: All files must end with a new line.
* **Validation**: All scripts must pass `shellcheck` without errors.
* **Documentation**: A `README.md` at the root and within each project folder is mandatory.
