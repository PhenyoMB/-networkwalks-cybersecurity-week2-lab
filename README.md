# NetworkWalks Cybersecurity Internship – Week 2

A practical portfolio of five cybersecurity exercises completed as part of the NetworkWalks internship. The work introduces domain and website reconnaissance, search-engine OSINT, graphical OSINT, public information gathering, and basic network discovery.

Each module has its own README with the exercise workflow, tools, evidence, observations, and limitations. Screenshots and the network topology PDF are stored in their corresponding module folders.

## Project overview

| Module | Topic | Main tools | Documentation |
|---|---|---|---|
| 1 | Website and domain reconnaissance | WHOIS, WhatWeb, nslookup, curl, wafw00f, DNSRecon | [Module 1 README](project-module-1/README.md) |
| 2 | Search-engine reconnaissance | Google Search operators, Google Hacking Database (GHDB) | [Module 2 README](project-module-2/README.md) |
| 3 | Graph-based OSINT | Maltego | [Module 3 README](project-module-3/README.md) |
| 4 | Domain information gathering | theHarvester | [Module 4 README](project-module-4/README.md) |
| 5 | Network discovery and topology | Zenmap, Nmap, Windows Command Prompt | [Module 5 README](project-module-5/README.md) |

## Flagship module: Website and domain reconnaissance

Module 1 is the flagship exercise because it combines six tools to examine different aspects of a domain's publicly observable footprint: registration information, DNS, web technologies, HTTP responses, and possible web application firewall detection.

**Key skills:** domain reconnaissance, DNS enumeration, web technology fingerprinting, HTTP inspection, and introductory attack-surface discovery.

![WHOIS reconnaissance evidence](<project-module-1/1. whois.png>)

See the [complete Module 1 walkthrough](project-module-1/README.md).

## Mandatory capstone: Network discovery

Module 5 applies basic networking knowledge to host discovery. The workflow uses `ipconfig` to inspect local network configuration, then Zenmap/Nmap to perform a ping scan and visualise responsive hosts.

![Zenmap network discovery evidence](<project-module-5/2. Ping Scan Results.png>)

The exercise material includes `nmap -sn 10.0.0.0/24` as an example. The subnet must be confirmed against the network being tested and should only be scanned with authorisation. Host counts and scan results vary by environment.

See the [complete Module 5 walkthrough](project-module-5/README.md) and the [Zenmap network scanning PDF](project-module-5/zenmap_network_scanning.pdf).

## Skills covered

- Domain and DNS reconnaissance
- OSINT and search-engine reconnaissance
- Web technology fingerprinting
- HTTP response inspection
- Email and DNS information gathering
- Basic IPv4 addressing and subnet awareness
- Host discovery and scan-output interpretation
- Network topology visualisation
- Technical documentation and evidence handling

## Repository structure

```text
.
├── README.md
├── project-module-1/
│   ├── README.md
│   └── reconnaissance screenshots
├── project-module-2/
│   └── README.md
├── project-module-3/
│   ├── README.md
│   └── Maltego screenshots
├── project-module-4/
│   ├── README.md
│   └── theHarvester screenshots
└── project-module-5/
    ├── README.md
    ├── Zenmap screenshots
    └── zenmap_network_scanning.pdf
```

## Evidence and limitations

The screenshots and PDF are supporting evidence of the documented exercises. Tool output should be interpreted in context: a discovery result does not automatically establish that a system is vulnerable, current, or fully enumerated. API-key requirements, source coverage, firewalls, and network configuration can affect results.

Module 2 currently has no dedicated screenshots in the repository. Its existing notes duplicated camera-related URLs under the mathematics-PDF heading, so those URLs have not been represented as verified PDF findings. Direct camera endpoints have also been excluded from the public-facing documentation.

Before sharing this repository, review all screenshots and the PDF for email addresses, credentials, tokens, personal information, private IP addresses, MAC addresses, device names, and other sensitive details. Redact information that should not be public.

## Responsible use

These exercises are for education and authorised security work. Only investigate domains, systems, and networks for which permission has been granted. Publicly indexed information does not grant permission to access or test a resource.

## Author

**GitHub:** [PhenyoMB](https://github.com/PhenyoMB)
