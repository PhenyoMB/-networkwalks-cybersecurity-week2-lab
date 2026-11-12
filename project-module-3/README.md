# Module 3: Maltego-Based OSINT

<sub>NetworkWalks Cybersecurity Internship · Week 2</sub>

## Overview

This module uses **Maltego** on Windows to explore entity-based open-source intelligence (OSINT). The documented workflow creates a Domain entity for `networkwalks.com`, then uses Maltego transforms to explore related email and DNS information.

Maltego presents relationships between entities in a visual graph, helping an analyst organise and explore information gathered from available data sources.

## Objectives

- Set up and use the Maltego interface.
- Create a Domain entity for an authorised target.
- Run transforms related to email information.
- Explore common DNS names and name-server information.
- Review how related entities are represented in a graph.

## Workflow and evidence

### 1. Add a Domain entity

The initial screenshot shows the Domain entity being added to the Maltego workspace.

![Adding a Domain entity in Maltego](<1. Add domain to maltego.png>)

### 2. Set the target domain

The entity is changed to `networkwalks.com`.

![Domain entity set to networkwalks.com](<2. Change domain to networkwalks.com.png>)

### 3. Run email-related transforms

The following screenshots document the email-related transform workflow and its output.

![Running email-related transforms](<3. Email Terraforms.png>)

![Further email-related transform results](<4. Email Terraforms.png>)

![Extracted email results](<5. Extracted Emails.png>)

### 4. Explore DNS relationships

The remaining screenshots document transforms relating to common DNS names, DNS name servers, and NS/MX records.

![Finding common DNS names](<6. Find Common DNS Names.png>)

![DNS name-server results](<7. DNS Name Servers.png>)

![Further NS and MX exploration](<8. DNS Name NS & MX going further.png>)

## What this demonstrates

- Entity creation and graph-based OSINT workflows.
- Use of transforms to explore relationships associated with a domain.
- Exploration of email-related and DNS-related information.
- The importance of reviewing the source and context of returned data.

## Interpretation and limitations

A transform returning an entity does not, by itself, verify that the information is current, complete, or owned by the target organisation. Results depend on the transform, connected data sources, and their coverage.

The screenshots are evidence of the workflow, not a claim that every returned email address or DNS relationship has been independently verified. Review screenshots for personal information and redact any details that should not be made public before sharing this repository.

## Responsible use

Use Maltego only with domains and information that you are authorised to investigate. Treat collected contact details as potentially sensitive and avoid unnecessary publication or contact.
