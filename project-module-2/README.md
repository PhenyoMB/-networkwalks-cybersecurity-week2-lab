# Module 2: Google Hacking Database (GHDB)

<sub>NetworkWalks Cybersecurity Internship · Week 2</sub>

## Overview

This exercise explores how Google search operators and Google Hacking Database (GHDB) queries can reveal resources that have been indexed and made discoverable through a search engine.

The exercise notes cover two search themes:

1. Publicly indexed camera-related pages and interfaces.
2. Mathematics PDF documents that may be discoverable through search.

The focus of this module is search-engine reconnaissance and understanding the security implications of information that is unintentionally exposed to public indexing.

## Objectives

- Understand the purpose of Google search operators and GHDB.
- Explore how search queries can narrow results by page title, URL path, or file type.
- Recognise that indexed information can reveal an organisation's external exposure.
- Distinguish between discovering a result and being authorised to access or test it.

## Exercise themes

### 1. Camera-related search results

The exercise investigated search results associated with camera interfaces, including a query theme using:

```text
intitle:webcamxp inurl:8080
```

This is an example of a search pattern documented in the exercise notes. Search results can change over time, and a result appearing in Google does not establish that a device is currently online, vulnerable, or authorised for access.

### 2. Mathematics PDF documents

The second exercise theme was finding mathematics PDF documents through search. The notes currently stored with this repository repeat the camera-related URLs under the mathematics PDF heading. They therefore do not provide reliable evidence of specific PDF results. No individual PDF findings are claimed in this README.

## Findings and limitations

- Search engines can index pages and files that an organisation did not intend to make easy to discover.
- Search results are time-dependent and may become unavailable or change.
- A search result alone does not prove that a resource is misconfigured or exploitable.
- The current exercise notes need to be supplemented with verified, non-sensitive examples of the PDF search results if those findings are to be documented.

## Evidence

No dedicated screenshots for this module are currently present in the repository. Add screenshots of representative search queries and result pages if available.

Before adding evidence, redact or omit:

- Live camera URLs, IP addresses, and hostnames that could direct others to exposed devices.
- Credentials, session tokens, personal information, or identifiable individuals.
- Any content that would facilitate unauthorised viewing or access.

Do not reproduce lists of live camera endpoints in a public portfolio. The earlier notes contained direct camera URLs; those have intentionally been omitted from this README.

## Security and responsible use

This exercise is limited to search-engine reconnaissance. Do not attempt to access, control, view, or further test cameras or other resources discovered through search unless you have explicit authorisation from the owner. Public indexing is not permission.

## Further work

Add a concise observation for each authorised search exercise: the query theme, the type of result returned, why it may matter from a defensive perspective, and any limitations. Use sanitised screenshots rather than publishing live endpoints.
