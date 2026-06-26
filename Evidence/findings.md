--------# API Security Risk Analysis Findings

## API Information

**API Tested:** JSONPlaceholder

**Endpoint:** `/posts`

**Method:** GET

**Response Status:** 200 OK

---

## Observation 1 – Public Endpoint

**Risk Level:** Low

**Observation:**
The `/posts` endpoint is publicly accessible without authentication.

**Business Impact:**
This behavior is acceptable because JSONPlaceholder is a public demonstration API intended for learning and testing. In a production environment, publicly accessible endpoints should expose only non-sensitive data.

**Recommendation:**
Ensure that production APIs require authentication for endpoints containing sensitive or user-specific information.


---

## Observation 2 – User Information Exposure

**Risk Level:** Medium

**Observation:**
The `/users` endpoint returns user-related information, including names, email addresses, phone numbers, addresses, websites, and company details.

**Business Impact:**
Although this API is intentionally public for educational purposes, exposing detailed user information in a production environment could increase the risk of privacy issues, data harvesting, spam campaigns, or social engineering attacks.

**Recommendation:**
Return only the minimum data required by the client application. Sensitive fields should be protected using proper authentication and authorization mechanisms.


---

## Observation 3 – Public Read Access

**Risk Level:** Low

**Observation:**
The `/todos` endpoint is publicly accessible and returns task-related information without requiring authentication.

**Business Impact:**
For a demonstration API, this behavior is expected. However, in a production environment, task or user-specific information should only be accessible to authenticated and authorized users.

**Recommendation:**
Implement authentication and authorization for endpoints containing user-specific or business-sensitive information.
