# API Security Risk Analysis Findings

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
