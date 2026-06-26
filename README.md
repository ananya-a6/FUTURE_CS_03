# # FUTURE_CS_03

## API Security Risk Analysis

### Objective

The objective of this project is to perform a read-only API Security Risk Analysis on a public demonstration API, identify potential security risks, evaluate API behavior, and provide practical security recommendations based on industry best practices.

### Target API

JSONPlaceholder (Public Demo REST API)

Base URL:
https://jsonplaceholder.typicode.com

### Assessment Type

Read-Only API Security Assessment

### Tools Used

* Postman
* Browser
* GitHub
* Markdown Documentation

### Scope

The assessment was limited to publicly available API endpoints using safe GET requests. No exploitation, authentication bypass, denial-of-service testing, or unauthorized activities were performed.

### Methodology

1. Selected a public demonstration API.
2. Reviewed the available endpoints.
3. Tested API endpoints using Postman.
4. Inspected request and response headers.
5. Reviewed API responses.
6. Identified potential security risks.
7. Assessed business impact.
8. Documented remediation recommendations.

## Findings Summary

| ID     | Finding                              | Risk   |
| ------ | ------------------------------------ | ------ |
| API-01 | Public API Endpoints                 | Low    |
| API-02 | User Information Exposure            | Medium |
| API-03 | Public Task Data Exposure            | Low    |
| API-04 | Public Comment Data Exposure         | Low    |
| API-05 | Rate Limiting Not Clearly Documented | Medium |

### Overall Risk Rating

**Low to Medium**

### Key Findings

* Public endpoints were accessible without authentication.
* User-related information was returned by the `/users` endpoint.
* Response headers were inspected for security-related information.
* No authentication or authorization mechanisms were observed, which is expected for a demonstration API.
* No critical security vulnerabilities were identified during this read-only assessment.

### Repository Structure

* Evidence → Postman screenshots and findings
* Report → Final API Security Risk Analysis Report
* README.md → Project overview

### Author

Ananya Achalendran

### Internship

Future Interns Cyber Security Internship 2026
