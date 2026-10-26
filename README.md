# 🛡️ Cybersecurity Lab Environment Setup

**Network Walks Cybersecurity Internship | Week 1**

## 📌 1. Project Overview

This project documents the setup and network verification of a Kali Linux virtual machine using Oracle VirtualBox.

It demonstrates practical skills in **virtualization, Linux networking, connectivity testing, troubleshooting, and technical documentation.**

## 🎯 2. Project Objectives

- 🖥️ Access Kali Linux through VirtualBox.
- 🌐 Understand virtual machine network configuration.
- 🔎 Identify network interfaces, IP addresses, and gateways.
- 📡 Test network and DNS connectivity.
- 📸 Capture genuine technical evidence.
- 📝 Document findings professionally.

## 🧰 3. Tools and Technologies

| Tool | Purpose |
|---|---|
| Windows 11 | Host operating system |
| Oracle VirtualBox | Runs the virtual machine |
| Kali Linux | Cybersecurity lab environment |
| Linux commands | Network inspection and testing |
| GitHub | Documentation and version control |

## 🌐 4. Virtual Machine and Network Configuration

Kali Linux ran inside VirtualBox with its active network adapter configured to **NAT Network**. The Host-Only Network settings were documented separately.

| Network detail | Observed value |
|---|---|
| Interface | `eth0` |
| Status | `UP` |
| IPv4 address | `10.0.0.3` |
| Subnet prefix | `/24` |
| Default gateway | `10.0.0.1` |
| Subnet mask | `255.255.255.0` |

*These values reflect the configuration observed during testing.*

## 🔬 5. Network Verification Results

| Test | Command | Result |
|---|---|---|
| Interface and IP | `ip -br addr` | `eth0` was UP |
| Routing table | `ip route` | Default gateway: `10.0.0.1` |
| Gateway connectivity | `ping -c 4 10.0.0.1` | 4 received; 0% packet loss |
| DNS and external connectivity | `ping -c 4 google.com` | Domain resolved; 4 received; 0% packet loss |

### ✅ What the Results Mean

- The interface had an assigned IPv4 address.
- The routing table identified a default gateway.
- The gateway responded to connectivity tests.
- DNS resolution and external ICMP communication succeeded during testing.

## 📸 6. Technical Evidence

Screenshots and explanations are available in the project evidence folder.

**[📂 View Technical Evidence](evidence/)**

Evidence includes the Kali Linux desktop, VirtualBox network settings, IP address, routing table, and connectivity tests.

## 📚 7. Key Learning Outcomes

Through this exercise, I practised:

- 🖥️ Virtual machine networking.
- 🌐 IPv4 addressing and subnet masks.
- 🧭 Routing tables and default gateways.
- 📡 Connectivity testing and DNS resolution.
- 📝 Evidence-based technical reporting.

## ⚠️ 8. Limitations

These results represent the network state during testing. Successful ping responses do not guarantee that every website, port, or network service is reachable.

**Note:** NAT Network and Host-Only are separate VirtualBox networking modes; the documented Host-Only settings should not be confused with the VM’s active NAT Network adapter.

## 🔗 9. Tools and Resources

Official resources for the software used in this project:

- **Oracle VirtualBox:** [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- **Kali Linux:** [Download Kali Linux](https://www.kali.org/get-kali/)
- **7-Zip:** [Download 7-Zip](https://www.7-zip.org/) — for extracting `.7z` archives when needed.

## 🏁 10. Conclusion and Next Steps

This project established a foundation in **virtualization, Linux networking, and evidence-based documentation**.

Next, I will build on these skills through further hands-on cybersecurity exercises and structured lab reporting.

---

**Project:** Cybersecurity Lab Environment Setup  
**Programme:** Network Walks Cybersecurity Internship  
**Week:** 1  
**Platform:** GitHub
