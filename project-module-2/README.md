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


| No. | Link                                                             | Relevant Dork                     | Username /Password (if any) |
| --- | ---------------------------------------------------------------- | --------------------------------- | --------------------------- |
| 1   | http://109.233.191.130:8080/multi.html                           | intitle:webcamxp inurl:8080       | N/A                         |
| 2   | http://72.199.200.5:8080/                                        | intitle:webcamxp inurl:8080       | N/A                         |
| 3   | http://139.64.168.120:8080/                                      | intitle:webcamxp inurl:8080       | N/A                         |
| 4   | http://75.149.26.30:1024/                                        | intitle:webcamxp inurl:8080       | N/A                         |
| 5   | http://99.114.240.169:8080/                                      | intitle:"Webcam" inurl:WebCam.htm | N/A                         |
| 6   | [https://www.lmc.edu/webcam.htm](https://www.lmc.edu/webcam.htm) | intitle:"Webcam" inurl:WebCam.htm | N/A                         |
| 7   | http://219.111.32.218:8088/viewer/live/index.html                | inurl:viewer/live/index.html      | N/A                         |
| 8   | http://206.72.28.209/viewer/live/index.html?lang=en              | inurl:viewer/live/index.html      | N/A                         |
| 9   | http://122.249.124.12/viewer/live/index.html?lang=en             | inurl:viewer/live/index.html      | N/A                         |
| 10  | http://www.onizaki-yc.com:8080/viewer/live/en/live.html          | inurl:"/viewer/live.html"         | N/A                         |

### 2. Mathematics PDF documents

The second exercise theme was finding mathematics PDF documents through search. The notes currently stored with this repository repeat the camera-related URLs under the mathematics PDF heading. They therefore do not provide reliable evidence of specific PDF results. No individual PDF findings are claimed in this README.

| No. | Link                                                                                                                                                                   | Relevant Dork                                               | Username/Password (if any) |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | -------------------------- |
| 1   | http://erewhon.superkuh.com/library/Math/A%20Concise%20Introduction%20to%20Mathematical%20Logic_%203rd%20ed_%20Wolfgang%20Rautenberg_%202009.pdf                       |                                                             | N/A                        |
| 2   | [https://www.aetkin.com/files/Math 150 Calculus I/Advanced Calculus Textbook/](https://www.aetkin.com/files/Math%20150%20Calculus%20I/Advanced%20Calculus%20Textbook/) | intitle index of "parent directory" math ebook pdf          | N/A                        |
| 3   | https://freecomputerbooks.com/books/Discrete-Mathematics-with-SageMath.pdf                                                                                             | intitle index of "parent directory" math ebook pdf          | N/A                        |
| 4   | https://www.atadcrazy.net/misc/ebooks/Introduction%20to%20Mathematics%20by%20Alfred%20North%20Whitehead.pdf                                                            | intitle index of "parent directory" "mathematics" ebook pdf | N/A                        |
| 5   | http://erewhon.superkuh.com/library/Math/Direct%20Methods%20in%20the%20Calculus%20of%20Variations_%20Enrico%20Giusti_%202005.pdf                                       | intitle index of "parent directory" mathematics ebook pdf   | N/A                        |
| 6   | https://lira.epac.to/DOCS-TECH/Math/Engineering%20and%20Applied/Applied%20Calculus.pdf                                                                                 | intitle index of "parent directory" mathematics ebook pdf   | N/A                        |
| 7   | https://lira.epac.to/DOCS-TECH/Math/Engineering%20and%20Applied/Advanced%20Mathematical%20Methods%20for%20Scientists%20and%20Engineers.pdf                             | intitle index of "parent directory" "mathematics" pdf       | N/A                        |
| 8   | http://library.cusat.ac.in/cat/2013/mathematics.pdf                                                                                                                    | intitle index of "parent directory" "mathematics" pdf       | N/A                        |
| 9   | http://f.javier.io/public/books/Graham%20-%20Knuth%20-%20Patashnik%20-%20%20Concrete%20Mathematics.pdf                                                                 | intitle index of "parent directory" "mathematics" ebook pdf | N/A                        |
| 10  | https://www.eletrica.ufpr.br/graduacao/e-books/Mathematics%20-%20Fourier%20Transforms%20and%20Waves.pdf                                                                | intitle index of "parent directory" "mathematics" ebook pdf | N/A                        |

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
