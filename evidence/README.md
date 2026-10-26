Week 1 — Cybersecurity Lab Evidence

Programme: Network Walks Cybersecurity Internship
Project: Cybersecurity Lab Environment Setup

Overview

This directory contains screenshots documenting the setup and verification of my Kali Linux virtual machine using Oracle VirtualBox.

The evidence is organized in sequence to demonstrate the lab environment, network configuration, connectivity testing, and troubleshooting activities completed during Week 1.

Evidence 01 — Kali Linux Virtual Machine Running

Description:
This screenshot shows the Kali Linux desktop fully loaded inside Oracle VirtualBox on my Windows desktop.

Purpose:
To provide visual evidence that the Kali Linux virtual machine starts successfully and that the desktop environment is accessible.

Result:
The Kali Linux desktop is visible inside the running virtual machine.



## Evidence 02 — VirtualBox Host-Only Network Configuration

**Purpose:** To document the configuration of a VirtualBox Host-Only Network for the cybersecurity lab environment.

**Network requirement:** `10.0.0.0/24`

**Description:**
The VirtualBox Host-Only Network settings were configured using the required network range before verifying the network configuration inside Kali Linux.

**Technical significance:**
The `10.0.0.0/24` notation identifies a network with the subnet mask `255.255.255.0`. A host-only network allows the host computer and connected virtual machines to communicate through a virtual network interface.

**Next step:** Verify the IP address, network interface, and routing information inside Kali Linux.

**Note:** The actual IP address assigned to Kali Linux and the connectivity between network devices must be verified separately.



## Evidence 03 — VirtualBox NAT Network Configuration

**Purpose:** To document the network mode assigned to the Kali Linux virtual machine in Oracle VirtualBox.

**Configuration:** The virtual machine's network adapter is attached to a NAT Network.

**Technical significance:** A NAT Network can allow connected virtual machines to communicate with external networks through Network Address Translation (NAT). Actual connectivity depends on the network configuration and must be tested separately.

**Next step:** Verify Kali Linux's assigned IP address and network interface from inside the virtual machine.



## Evidence 04 — Kali Linux IP Address Verification

**Purpose:** To verify the IP address assigned to the Kali Linux virtual machine after configuring its network adapter in VirtualBox.

**Command used:**

`ip -br addr`

**Observed results:**

- **Loopback interface:** `lo`
- **Loopback IPv4 address:** `127.0.0.1/8`
- **Network interface:** `eth0`
- **Interface status:** `UP`
- **Assigned IPv4 address:** `10.0.0.3/24`
- **Subnet mask:** `255.255.255.0`

**Technical explanation:**

The `ip -br addr` command displays network interfaces and their assigned addresses in a brief format. The output shows that the `eth0` interface is enabled and has been assigned the IPv4 address `10.0.0.3` within the `10.0.0.0/24` subnet.

This confirms that Kali Linux has an IPv4 address on the configured network. However, this result alone does not confirm successful communication with the gateway or access to the internet.

**Result:** The network interface is up, and an IPv4 address has been assigned.

**Next step:** Inspect the routing table to identify the configured network routes and determine whether a default gateway exists.


## Evidence 05 — Kali Linux Routing Table

**Purpose:** To inspect the routing table and identify the default gateway configured for the Kali Linux virtual machine.

**Command used:**

`ip route`

**Observed results:**

- **Default gateway:** `10.0.0.1`
- **Network interface:** `eth0`
- **Kali IPv4 address:** `10.0.0.3`
- **Local subnet:** `10.0.0.0/24`
- **Route source:** DHCP for the default route

**Technical explanation:**

The `ip route` command displays the routes Kali Linux uses to direct network traffic. The default route, shown as `default via 10.0.0.1 dev eth0`, indicates that traffic without a more specific matching route is directed to the gateway at `10.0.0.1` through `eth0`.

The second route shows that the `10.0.0.0/24` subnet is directly connected through the same interface.

**Result:** A default route and a directly connected subnet route are present.

**Next step:** Test whether Kali can communicate with its configured default gateway.


Evidence 06 — Default Gateway Connectivity Test

Purpose: To test whether Kali Linux can communicate with its configured default gateway.

Command used:

ping -c 4 10.0.0.1

Observed results:

Destination gateway: 10.0.0.1

Packets transmitted: 4

Packets received: 4

Packet loss: 0%

Minimum round-trip time: 0.576 ms

Average round-trip time: 1.747 ms

Maximum round-trip time: 3.966 ms

Technical explanation:

The ping command uses Internet Control Message Protocol (ICMP) echo requests to test communication with another network device. The -c 4 option limits the test to four requests.

All four requests received replies from 10.0.0.1, with no packet loss. This confirms successful communication between Kali Linux and its configured gateway during this test.

Result: Gateway connectivity verified, with 0% packet loss during the test.

Limitation: This test does not independently confirm internet access or DNS resolution.

Next step: Test external network connectivity separately.


Evidence 07 — DNS Resolution and External Connectivity Test

Purpose: To test domain name resolution and connectivity to an external server from Kali Linux.

Command used:

ping -c 4 google.com

Observed results:

Domain tested: google.com

Resolved IPv4 address: 142.250.140.101

Packets transmitted: 4

Packets received: 4

Packet loss: 0%

Minimum round-trip time: 130.323 ms

Average round-trip time: 165.100 ms

Maximum round-trip time: 214.894 ms

Technical explanation:

The ping command tested connectivity to google.com. Kali Linux successfully resolved the domain name to 142.250.140.101 and received replies to all four ICMP echo requests.

The successful name resolution demonstrates that DNS was functioning for this request. The replies confirm that the external destination was reachable using ICMP during the test.

Result: DNS resolution and external connectivity verified for this test, with 0% packet loss.

Limitation: This test does not verify access to every website or confirm that all network services are functioning.

Next step: Review the collected evidence and summarize the network configuration and connectivity results.
