# OpenVAS Overview

OpenVAS is an open-source vulnerability scanner that is part of the Greenbone Vulnerability Management (GVM) framework.It is designed to detect security vulnerabilities in systems and services by executing thousands of vulnerability tests against a target host.

Main components:
- OpenVAS Scanner
- Greenbone Vulnerability Manager
- Greenbone Security Assistant (Web UI)
- Vulnerability Test Feed

Each vulnerability test is implemented using NASL scripts that check for known security issues.

Detected vulnerabilities are usually linked to CVE identifiers and evaluated using the CVSS scoring system.

The following official resources provide detailed information about the tool:

- 🌐 Official Greenbone website: https://www.greenbone.net
- 📚 Greenbone documentation: https://docs.greenbone.net
- 💻 OpenVAS source code: https://github.com/greenbone
- 🐛 Vulnerability test feed information: https://greenbone.github.io/docs/
- 🐞 Vulnerabilities detected by OpenVAS are typically referenced using standard      security identifiers such as CVE (Common Vulnerabilities and Exposures) and CVSS (Common Vulnerability Scoring System). Useful references:
  - https://cve.mitre.org
  - https://nvd.nist.gov
