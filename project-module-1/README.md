# Module 1: Website and Domain Reconnaissance

<sub>NetworkWalks Cybersecurity Internship · Week 2</sub>

## Overview

This module introduces passive and command-line reconnaissance techniques used to gather information about a domain and its publicly observable web infrastructure. It combines six tools, each providing a different view of domain registration, DNS, web technologies, HTTP responses, and possible web application security controls.

This is the flagship module in this repository because it demonstrates the broadest range of practical reconnaissance techniques covered in the week.

## Objectives

- Retrieve domain registration and name-server information.
- Identify technologies associated with a website.
- Resolve domain names and inspect DNS information.
- Review HTTP response headers.
- Check whether a web application firewall can be identified.
- Perform DNS reconnaissance and interpret the results.

## Tools and tasks

| Tool | What it is used for |
|---|---|
| **WHOIS** | Retrieve domain registration details and name-server information. |
| **WhatWeb** | Fingerprint technologies used by a website. |
| **nslookup** | Query DNS and resolve domain names. |
| **curl** | Make HTTP requests and inspect response headers. |
| **wafw00f** | Check for indicators of a web application firewall (WAF). |
| **DNSRecon** | Gather DNS-related information about a domain. |

## Evidence

The screenshots below are the evidence files already included in this module folder.

### 1. WHOIS
![WHOIS command output](<1. whois.png>)

### 2. WhatWeb
![WhatWeb technology fingerprinting output](<2. whatweb.png>)

### 3. nslookup
![nslookup DNS lookup output](<3. nslookup.png>)

### 4. curl
![curl HTTP response output](<4. curl -l.png>)

### 5. wafw00f
![wafw00f output](<5. wafw00f.png>)

### 6. DNSRecon
![DNSRecon output](<6. dnsrecon -d.png>)

## Key learning points

- Reconnaissance is more useful when information from multiple tools is considered together.
- DNS records, registration data, HTTP responses, and technology fingerprints provide different perspectives on a domain.
- A tool's output is an observation, not proof that a vulnerability exists.
- A WAF detection result should not be treated as a complete assessment of an application's security.

## Scope and responsible use

Only run active or intrusive checks against domains and systems for which you have permission. Publicly available information does not grant permission to probe, access, or test a system.

## Further work

For a stronger technical record, add a short **Observations** subsection beneath each screenshot describing what the output showed, what it did not establish, and any limitations encountered. Avoid publishing credentials, tokens, personal information, or sensitive target details.
