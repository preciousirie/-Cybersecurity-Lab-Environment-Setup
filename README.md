# Cybersecurity Lab Environment Setup

**Network Walks Cybersecurity Internship | Week 1**

## 1. Project Overview

This project documents my hands-on experience setting up and validating a Kali Linux virtual machine as part of my Network Walks Cybersecurity Internship.

The project focuses on virtual machine configuration, Linux networking, connectivity testing, troubleshooting, and technical evidence collection.

My objective is to understand how a cybersecurity lab environment is prepared, how network connectivity is verified, and how technical activities are documented professionally.

## 2. Project Objectives

- Set up and access a Kali Linux virtual machine using VirtualBox.
- Understand virtual machine network configuration.
- Identify the virtual machine's network interface, IP address, and default gateway.
- Test gateway connectivity, external connectivity, and DNS resolution.
- Document completed activities using genuine technical evidence.
- Develop practical troubleshooting and technical reporting skills.

## 3. Tools and Purposes

| Tool | Purpose |
|---|---|
| Windows 11 | Host operating system |
| Oracle VirtualBox | Virtualization platform |
| Kali Linux | Linux-based cybersecurity lab environment |
| Linux networking commands | Network inspection and connectivity testing |
| GitHub | Project documentation and version control |

## 4. Virtual Machine and Network Configuration

Kali Linux was run inside Oracle VirtualBox. The virtual machine's active network adapter was configured to use a NAT Network.

The VirtualBox Host-Only Network configuration was also documented separately as part of the lab setup process.

The following network details were observed inside Kali Linux during verification:

- **Network interface:** `eth0`
- **Interface status:** `UP`
- **IPv4 address:** `10.0.0.3`
- **Subnet prefix:** `/24`
- **Default gateway:** `10.0.0.1`

The `/24` prefix corresponds to the subnet mask `255.255.255.0`.

These values represent the configuration observed during testing and may differ in other virtual machine environments.

## 5. Network Verification and Connectivity Testing

Several Linux networking commands were used to inspect the network configuration and test connectivity.

| Test | Command | Observed result |
|---|---|---|
| Network interface and IP address | `ip -br addr` | `eth0` was UP with `10.0.0.3/24` |
| Routing table | `ip route` | Default gateway identified as `10.0.0.1` |
| Gateway connectivity | `ping -c 4 10.0.0.1` | 4 packets received; 0% packet loss |
| DNS resolution and external connectivity | `ping -c 4 google.com` | Domain resolved to `142.250.140.101`; 4 packets received; 0% packet loss |

### Interpretation of Results

The routing table showed a default route through `10.0.0.1`. The gateway ping test confirmed communication with that gateway during testing.

The `google.com` test confirmed that DNS resolution succeeded for the domain and that the resolved destination returned all four ICMP replies.

Together, these results demonstrated that the virtual machine had working gateway connectivity, DNS resolution, and external ICMP connectivity during the tests.

## 6. Troubleshooting and Learning

This exercise provided practical experience in:

- Inspecting Linux network interfaces.
- Reading IPv4 addresses and subnet prefixes.
- Identifying a default gateway from the routing table.
- Testing connectivity with ICMP ping requests.
- Interpreting packet loss and response times.
- Distinguishing DNS resolution from basic IP connectivity.
- Recording test results without assuming success before verification.

## 7. Technical Evidence

Screenshots and supporting explanations are maintained in the repository's evidence folder.

The evidence covers the Kali Linux desktop, VirtualBox network configuration, IP address verification, routing information, gateway connectivity, and the external connectivity test.

**Evidence repository:** [View project evidence](evidence/)

Each evidence item should correspond to an actual configuration step or completed test, with filenames and explanations matching the recorded results.

## 8. Learning Outcomes

Through this exercise, I developed a better understanding of:

- Virtualization and virtual machine networking.
- Basic Linux networking commands.
- IPv4 addressing, subnet prefixes, and default gateways.
- Routing tables and network connectivity testing.
- DNS resolution and external ICMP connectivity.
- Evidence-based technical documentation using GitHub.

## 9. Limitations

These tests reflect the network state at the time they were performed. Successful ping responses do not establish that every website, port, protocol, or network service is reachable.

The Host-Only Network configuration and the active NAT Network adapter represent different VirtualBox networking modes. They should be understood as separate configuration details rather than treated as the same active connection.

## 10. Conclusion and Next Steps

Setting up and validating the Kali Linux virtual machine established a foundation for my practical cybersecurity learning journey.

By inspecting network interfaces, reviewing routing information, and testing connectivity, I gained hands-on experience with essential networking concepts.

The next stages of my development will build on these fundamentals through further hands-on cybersecurity exercises, troubleshooting, and structured technical documentation.

---

**Project:** Cybersecurity Lab Environment Setup  
**Programme:** Network Walks Cybersecurity Internship  
**Week:** 1
