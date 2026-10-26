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

**Filename:** `02-host-only-network-configuration.png`

**Purpose:** To document the configuration of a VirtualBox Host-Only Network for the cybersecurity lab environment.

**Network requirement:** `10.0.0.0/24`

**Description:**
The VirtualBox Host-Only Network settings were configured using the required network range before verifying the network configuration inside Kali Linux.

**Technical significance:**
The `10.0.0.0/24` notation identifies a network with the subnet mask `255.255.255.0`. A host-only network allows the host computer and connected virtual machines to communicate through a virtual network interface.

**Next step:** Verify the IP address, network interface, and routing information inside Kali Linux.

**Note:** The actual IP address assigned to Kali Linux and the connectivity between network devices must be verified separately.


## Evidence 03 — VirtualBox NAT Network Configuration

**Filename:** `03-kali-nat-network-configuration.png`

**Purpose:** To document the network mode assigned to the Kali Linux virtual machine in Oracle VirtualBox.

**Configuration:** The virtual machine's network adapter is attached to a NAT Network.

**Technical significance:** A NAT Network can allow connected virtual machines to communicate with external networks through Network Address Translation (NAT). Actual connectivity depends on the network configuration and must be tested separately.

**Next step:** Verify Kali Linux's assigned IP address and network interface from inside the virtual machine.
