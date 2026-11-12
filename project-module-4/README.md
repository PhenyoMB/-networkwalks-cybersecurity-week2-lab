# Module 4: Domain Reconnaissance with theHarvester

<sub>NetworkWalks Cybersecurity Internship · Week 2</sub>

## Overview

This module uses **theHarvester** in Kali Linux to collect publicly available information associated with a domain. The exercise targets `microsoft.com` and compares results from a specified search source with a broader source selection.

theHarvester can help security practitioners gather externally available email addresses, hostnames, and related information as part of an authorised reconnaissance process.

## Objectives

- Run theHarvester from Kali Linux.
- Specify a target domain, result limit, and data source.
- Compare results from different source selections.
- Understand how API-key requirements and source availability affect collection.

## Commands used

### Task 1: Search using Baidu

```bash
theHarvester -d microsoft.com -l 1000 -b baidu
```

The recorded output returned one email address and no host or IP records.

![theHarvester results using Baidu](<1. Microsoft Emails found -b baidu.png>)

### Task 2: Search using all configured sources

```bash
theHarvester -d microsoft.com -l 50 -b all
```

The recorded run reported that a Brave API key was missing. This is an example of how source configuration can limit the information a tool is able to collect.

![theHarvester results using all sources](<2. Microsoft emails found -b all.png>)

## Observations

- Results vary according to the selected source and the data available to that source.
- A missing API key can prevent a source from being queried successfully.
- A lack of returned hostnames or IP addresses does not prove that none exist.
- Collected email addresses and hostnames should be treated as unverified until independently validated.

## Limitations

The results represent the output captured during this exercise. They are not a complete inventory of the target domain's infrastructure and should not be interpreted as a current or exhaustive assessment.

Before publishing screenshots, check that email addresses and any other potentially sensitive details are appropriate to disclose. Redact them where necessary.

## Responsible use

Use theHarvester only for authorised security research. Publicly discoverable contact information should be handled responsibly and should not be used for unsolicited or harmful activity.
