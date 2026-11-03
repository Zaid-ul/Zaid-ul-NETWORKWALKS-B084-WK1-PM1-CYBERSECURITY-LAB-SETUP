# 🔐 Cybersecurity Lab Environment Setup

**Building a Linux-based environment for cybersecurity practice, ethical hacking and penetration testing.**

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-C00000?style=flat-square" />
  <img src="https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Environment-Dual%20Boot-0070C0?style=flat-square" />
  <img src="https://img.shields.io/badge/Focus-Ethical%20Hacking-C00000?style=flat-square" />
</p>

---

## 📌 1. Project Overview

This project focuses on preparing and understanding a practical cybersecurity environment using Kali Linux.

Kali Linux is installed directly on my laptop through a dual-boot configuration alongside Windows 11. This allows me to choose between both operating systems whenever I start my computer.

Kali Linux is a Debian-based Linux distribution specifically designed for penetration testing, digital forensics and information security operations. It provides access to numerous security tools that support practical cybersecurity exercises.

The purpose of this project is to establish a functional environment where I can explore cybersecurity tools, understand network configurations, perform reconnaissance and develop practical ethical hacking skills.

### 📌 Note on Lab Environment Selection

The original lab instructions specified using Oracle VirtualBox to run Kali Linux as a virtual machine. However, I already had Kali Linux installed directly on my laptop through a dual-boot configuration alongside Windows 11.

Due to limited internet data availability and the additional download required to obtain the Kali Linux virtual machine image, I decided to use my existing Kali Linux installation rather than download and install another copy.

This allowed me to proceed with the practical exercises using the resources already available on my system while avoiding unnecessary data consumption and additional storage requirements.

I understand that this approach differs from the specified VirtualBox setup, particularly regarding virtual network isolation and VM snapshot functionality. Nevertheless, it provides a functional Linux environment for carrying out relevant cybersecurity exercises and developing practical skills.

I acknowledge this deviation from the original instructions and remain open to adopting the VirtualBox configuration if it becomes necessary for subsequent lab activities.

---

## 🎯 2. Project Objectives

The main objectives of this project are to:

- Understand the Kali Linux operating environment.
- Explore Linux system administration and command-line operations.
- Identify network interfaces and understand their configurations.
- Verify network and internet connectivity.
- Understand IP addressing, DNS and routing.
- Explore essential cybersecurity tools.
- Develop practical network reconnaissance and vulnerability assessment skills.
- Document technical procedures, challenges and solutions.

## 🛡️ 3. Purpose of the Lab

A cybersecurity laboratory provides a controlled environment for learning and experimenting with security technologies.

It allows cybersecurity students and professionals to understand how systems communicate, how vulnerabilities can occur and how security weaknesses can be identified.

This environment will support practical activities such as:

- **Network Reconnaissance:** Gathering information about devices and services on a network.
- **Port Scanning:** Identifying open ports and discovering services running on a target system.
- **Vulnerability Assessment:** Examining systems for known security weaknesses.
- **Packet Analysis:** Inspecting network traffic to understand communication between devices.
- **Web Application Security:** Learning how to identify common web application vulnerabilities.
- **Linux Administration:** Managing files, users, permissions, packages and system configurations.

**Ethical Consideration:** All security-testing activities must be performed on systems I own or have explicit authorization to test.

## 🏗️ 4. Lab Architecture

The laboratory uses a dual-boot configuration.

Dual booting means having two operating systems installed on the same computer, allowing the user to select which operating system to run during startup.

In this setup, Kali Linux is my primary working environment, while Windows 11 remains available as a secondary operating system.

Unlike virtualization, dual booting allows Kali Linux to run directly on the computer's hardware rather than inside a virtual machine.

| Component | Configuration |
|---|---|
| Primary Operating System | Kali Linux |
| Secondary Operating System | Windows 11 |
| Installation Type | Dual Boot |
| Kali Installation | Direct hardware installation |
| Hypervisor | Not used |
| Working Environment | Native Linux |
| Primary Purpose | Cybersecurity Practice |

**Understanding the difference:**

- Native installation: Kali Linux runs directly on the computer's hardware.
- Virtual machine: Kali Linux runs inside virtualization software such as VirtualBox.
- Dual boot: Two operating systems are installed on the same computer, but normally only one runs at a time.

This distinction is important because the current environment does not provide the virtual network isolation and VM snapshot functionality described in the original VirtualBox lab instructions.

## ⚙️ 5. Tools and Their Functions

The following tools are relevant to the cybersecurity environment.

### 1. Nmap – Network Mapper

Nmap is a network discovery and security auditing tool.

It helps identify devices connected to a network, discover open ports and determine which services are running on target systems.

Example:

`nmap --version`

This command checks whether Nmap is installed and displays its version.

### 2. Wireshark – Network Protocol Analyzer

Wireshark is used to capture and inspect network traffic.

It allows security professionals to examine communication between devices, identify unusual network activity and troubleshoot connectivity problems.

### 3. Burp Suite – Web Application Security Testing

Burp Suite is a platform for testing web application security.

It allows users to intercept, inspect and modify HTTP requests and responses to understand how web applications communicate and identify potential vulnerabilities.

### 4. Metasploit Framework

Metasploit is a penetration-testing framework used to validate security weaknesses in authorized testing environments.

It provides tools and modules for vulnerability research, exploit validation and security assessments.

### 5. Netcat

Netcat is a networking utility used to establish connections between systems, test network services and troubleshoot communication issues.

### 6. Linux Terminal

The Linux terminal provides a command-line interface for interacting with the operating system.

It is essential for managing system configurations, installing software, troubleshooting network problems and executing cybersecurity tools.

*Tool availability and versions will be verified as practical exercises progress.*

## 🔎 6. Lab Verification and Command Explanations

The following commands are useful for understanding and verifying the Kali Linux environment.

| Command | Explanation |
|---|---|
| `cat /etc/os-release` | Displays information about the installed operating system and its version. |
| `uname -r` | Displays the currently running Linux kernel version. |
| `ip a` | Displays network interfaces and their assigned IP addresses. |
| `ip route` | Displays the routing table and default gateway information. |
| `ping -c 4 8.8.8.8` | Sends four network packets to test IP connectivity. |
| `nslookup google.com` | Checks whether DNS can resolve a domain name into an IP address. |
| `nmap --version` | Checks the installed Nmap version. |

### Understanding the Verification Process

**IP Address Verification**

The `ip a` command helps identify the network interfaces available on the system and the IP addresses assigned to them.

An IP address is a logical address used to identify a device on an IP network.

**Routing Verification**

The `ip route` command displays how network traffic is directed.

It helps identify the default gateway, which is normally the router responsible for forwarding traffic to external networks.

**Internet Connectivity**

The `ping` command tests whether another IP address can be reached over the network.

Testing an IP address directly helps distinguish basic IP connectivity problems from DNS-related problems.

**DNS Verification**

DNS stands for Domain Name System.

It translates human-readable domain names into IP addresses that computers use to communicate.

For example, DNS allows a system to resolve `google.com` instead of requiring the user to remember its numerical IP address.

*Actual command outputs and screenshots will be added after verification.*

## 🐞 7. Problems Encountered and Troubleshooting

Troubleshooting is an important part of system administration and cybersecurity.

During practical exercises, technical problems may occur due to incorrect configurations, missing dependencies or network connectivity issues.

The following are potential issues to investigate and document:

**Problem 1: Internet Connectivity Issues**

A computer may have an active network interface but still experience problems accessing the internet.

Possible causes include incorrect IP configuration, gateway problems, DNS failures or network interruptions.

Useful diagnostic commands:

- `ip a`
- `ip route`
- `ping -c 4 8.8.8.8`
- `nslookup google.com`

**Problem 2: DNS Resolution Failure**

DNS problems occur when a system cannot translate domain names into IP addresses.

Checking DNS resolution helps determine whether the problem is related to name resolution rather than general network connectivity.

**Problem 3: Missing Cybersecurity Tools**

Some security utilities may not be installed or may require updates.

Kali Linux uses the APT package manager to install and maintain software.

Example:

`sudo apt update`

This refreshes the package information available from configured software repositories.

`sudo apt upgrade`

This upgrades installed packages where updates are available.

These commands should be used with an understanding of their effects on the system.

*Actual problems and solutions will be recorded when encountered.*

## 💡 8. What I Learned

This project is intended to strengthen my practical understanding of Linux, networking and cybersecurity.

The major learning areas include:

### 1. Linux Administration

I am developing an understanding of Linux system administration, including navigating the filesystem, managing permissions, installing software and executing commands through the terminal.

### 2. Network Configuration

I am learning how IP addresses, subnet masks, default gateways, DNS servers and routing tables work together to enable network communication.

### 3. Network Troubleshooting

Understanding commands such as `ip a`, `ip route` and `ping` helps identify connectivity problems and investigate their possible causes.

### 4. Cybersecurity Tools

I am exploring tools used by security professionals to identify network devices, analyze traffic, assess vulnerabilities and test web application security.

### 5. Ethical Hacking

I am developing an understanding of authorized security testing, including reconnaissance, vulnerability identification and responsible reporting.

### 6. Technical Documentation

Documenting commands, configurations, screenshots and troubleshooting procedures helps maintain a clear record of technical work and makes practical exercises easier to reproduce.

## 🔐 9. Security and Ethical Use

This environment is intended strictly for educational purposes and authorized cybersecurity testing.

All scanning, vulnerability assessment and penetration-testing activities must be conducted within systems and networks where permission has been granted.

Responsible cybersecurity practice requires respecting privacy, protecting information and avoiding unauthorized access.

## 🔗 10. Tools and Resources

- **Kali Linux:** https://www.kali.org/
- **Nmap:** https://nmap.org/
- **Wireshark:** https://www.wireshark.org/
- **Burp Suite:** https://portswigger.net/burp
- **Metasploit:** https://www.metasploit.com/

---

## 👤 Author

**Ibrahim Adebayo Daramola**

Cybersecurity | Network Engineering | Linux

GitHub: https://github.com/Zaid-ul

---

## 📌 Project Information

**Program:** Cybersecurity Practical Lab  
**Module:** Week 1 – Project Module 1  
**Project:** Cybersecurity Lab Environment Setup  
**Operating System:** Kali Linux  
**Installation:** Dual Boot (Kali Linux / Windows 11)  
**Project Status:** In Progress
