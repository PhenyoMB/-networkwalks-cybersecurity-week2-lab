# NetworkWalks Cybersecurity Internship – Week 2

A collection of practical cybersecurity exercises completed as part of the NetworkWalks cybersecurity internship. The exercises introduce reconnaissance, open-source intelligence (OSINT), information gathering, and basic network discovery using commonly used security tools.

The repository documents the tools used, the commands or workflows followed, and the observations recorded during the exercises.

## Learning objectives

- Understand how publicly available information can contribute to an organisation's attack surface.
- Practise domain and DNS reconnaissance.
- Identify technologies and potential web application security controls.
- Use OSINT tools to collect and correlate publicly available information.
- Discover active hosts on a network and interpret basic network scan results.
- Document findings clearly while working within authorised testing boundaries.

## Tools and technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Linux environment used for reconnaissance exercises |
| WHOIS | Retrieve domain registration information |
| WhatWeb | Identify technologies used by websites |
| nslookup | Query DNS records and resolve domain names |
| curl | Inspect HTTP responses and headers |
| wafw00f | Check for the presence of web application firewalls |
| DNSRecon | Perform DNS reconnaissance |
| Google Search / GHDB | Use search operators to locate publicly indexed information |
| Maltego | Conduct graphical, entity-based OSINT |
| theHarvester | Gather publicly available email addresses, hosts, and related information |
| Zenmap / Nmap | Discover hosts and visualise network topology |
| Windows Command Prompt | Inspect local network configuration with `ipconfig` |

## Modules

### Module 1 – Website and Domain Reconnaissance

<badge color="success">Flagship module</badge>

This module brings together several command-line tools to examine a target domain and its publicly observable web infrastructure. It provides the broadest practical introduction to reconnaissance among the exercises documented in this repository.

Tools covered:

- **WHOIS:** Review domain registration and name-server information.
- **WhatWeb:** Fingerprint technologies used by a website.
- **nslookup:** Perform DNS lookups and resolve domain names.
- **curl:** Inspect HTTP responses and response headers.
- **wafw00f:** Check whether a web application firewall can be identified.
- **DNSRecon:** Enumerate DNS information for a domain.

**Skills demonstrated:** Domain reconnaissance, DNS enumeration, web technology fingerprinting, HTTP inspection, and introductory attack-surface discovery.

### Module 2 – Google Hacking Database (GHDB)

This exercise introduces the use of Google search operators and entries from the Google Hacking Database (GHDB) to identify information that may be publicly indexed by search engines.

The documented activities include searches relating to publicly accessible camera resources and mathematics PDF documents.

**Security consideration:** Search results can expose sensitive information. Any potentially sensitive URLs, credentials, personal information, or identifying details should be excluded or redacted before publishing screenshots or findings. Only conduct follow-up testing where explicit authorisation exists.

**Skills demonstrated:** Search-engine reconnaissance, use of Google dorks, identifying publicly indexed resources, and responsible handling of OSINT findings.

### Module 3 – Maltego OSINT

This exercise uses Maltego on Windows to explore entity-based OSINT.

The documented workflow includes creating a Domain entity for `networkwalks.com` and running email-related transforms to explore information associated with the domain.

**Skills demonstrated:** Maltego setup, entity creation, transform execution, and graphical OSINT workflows.

The available exercise notes do not establish that the transforms returned verified email addresses, so no specific email findings are claimed here.

### Module 4 – theHarvester

This exercise uses theHarvester in Kali Linux to gather publicly available information associated with a domain.

The documented target is `microsoft.com`. The exercises include the following commands:

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
theHarvester -d microsoft.com -l 50 -b all
```

The recorded Baidu-source output returned one email address and no host or IP records. The all-sources run reported that a Brave API key was missing. Results therefore depend on the selected sources, available API credentials, and the information those sources make available.

**Skills demonstrated:** Domain-based OSINT, source selection, command-line reconnaissance, and interpreting incomplete or source-dependent results.

### Module 5 – Network Discovery with Zenmap and Nmap

<badge color="info">Mandatory capstone</badge>

The capstone exercise uses Zenmap, the graphical interface for Nmap, to discover active hosts on a local network and visualise the results.

The documented workflow includes:

1. Running `ipconfig` in Windows Command Prompt to inspect local network configuration.
2. Identifying the relevant network range.
3. Performing a ping scan to identify responsive hosts.
4. Reviewing discovered IP and MAC address information.
5. Using Zenmap's topology view and exporting the visualisation to PDF.

Example scan command:

```bash
nmap -sn 10.0.0.0/24
```

The `10.0.0.0/24` range is the example subnet used in the exercise material. Replace it with the subnet you are authorised to scan and have confirmed from your own network configuration. Host counts and discovered devices will vary by network and scan conditions.

**Skills demonstrated:** Basic IP addressing and subnet awareness, host discovery, interpreting scan output, and network topology visualisation.

## Key skills covered

- Domain and DNS reconnaissance
- OSINT and search-engine reconnaissance
- Web technology fingerprinting
- HTTP response and header inspection
- Basic network discovery and host identification
- Interpreting tool output and recognising data-source limitations
- Documenting technical workflows and observations

## Evidence and screenshots

Screenshots and exported scan results should be added alongside the relevant module documentation. Before publishing, review images for exposed credentials, personal information, sensitive URLs, API keys, or details from networks that you are not authorised to disclose.

Suggested evidence to include:

- Module 1: terminal output for the reconnaissance tools.
- Module 2: representative GHDB searches with sensitive results redacted.
- Module 3: Maltego workspace showing the Domain entity and transforms.
- Module 4: theHarvester commands and output, including the API-key limitation where relevant.
- Module 5: local network configuration, Zenmap scan results, topology view, and exported PDF.

## Responsible use

These exercises are intended for education and authorised security work. Reconnaissance and scanning should only be performed against domains, systems, and networks for which permission has been granted. Public availability of information does not automatically mean that further access or testing is authorised.

## Author

**GitHub:** [PhenyoMB](https://github.com/PhenyoMB)
