# Module 5: Network Discovery with Zenmap and Nmap

<sub>NetworkWalks Cybersecurity Internship · Week 2 · Capstone</sub>

## Overview

This capstone exercise uses **Zenmap**, the graphical interface for Nmap, to identify responsive hosts on a network and visualise the scan results.

The workflow begins by checking the local Windows network configuration, identifying the subnet to examine, running a ping scan, and reviewing the discovered hosts. The exercise also includes a Zenmap topology visualisation exported as a PDF.

## Objectives

- Inspect local IP configuration using Windows Command Prompt.
- Identify the network range relevant to the exercise.
- Perform a host-discovery scan.
- Interpret discovered IP and MAC address information.
- Review the network topology view and export it to PDF.

## Workflow and evidence

### 1. Inspect local network configuration

Run the following command in Windows Command Prompt:

```cmd
ipconfig
```

Use the output to identify the active network adapter and its IPv4 address, subnet mask, and default gateway. Determine the appropriate subnet before scanning.

![Windows IP configuration](<1. IP Config Details.png>)

### 2. Perform a ping scan

The exercise material uses the following example command:

```bash
nmap -sn 10.0.0.0/24
```

The `-sn` option performs host discovery without a port scan. The `10.0.0.0/24` range is an example from the exercise material. Replace it with the subnet you have confirmed for your own authorised lab network.

![Zenmap or Nmap ping scan results](<2. Ping Scan Results.png>)

The documented example output reports four hosts as up. Treat that count as the captured exercise result only; the number of responsive hosts will vary by network, firewall settings, and scan conditions.

### 3. Review the topology export

The repository also includes the topology/network-scanning PDF generated for the exercise.

[Open the Zenmap network scanning PDF](zenmap_network_scanning.pdf)

## What this demonstrates

- Basic IPv4 network configuration and subnet awareness.
- Host discovery using Nmap.
- Reading scan output and identifying responsive devices.
- Reviewing IP and MAC address information.
- Using Zenmap's topology view to visualise discovered hosts.

## Limitations and safe handling

A ping scan identifies hosts that respond to the discovery probes. A host that does not respond is not necessarily offline; a firewall or network configuration may block probes.

Before publishing screenshots or the PDF, review them for private IP addresses, MAC addresses, device names, usernames, and other details that identify a personal or organisational network. Redact information that should not be public.

## Responsible use

Only scan networks you own or have explicit permission to assess. Confirm the target subnet before running Nmap, and do not scan unrelated networks.
