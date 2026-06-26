# API Security Risk Analysis Findings

## Target API

**API:** JSONPlaceholder

**Base URL:** https://jsonplaceholder.typicode.com

---

## Tested Endpoints

* GET /posts
* GET /users
* GET /todos
* GET /comments

---

## Findings

### API-01 – Public API Endpoints

**Risk:** Low

Public endpoints were accessible without authentication. This behavior is expected for a demonstration API but should be restricted for production APIs containing sensitive information.

---

### API-02 – User Information Exposure

**Risk:** Medium

The `/users` endpoint returned user information such as names, email addresses, phone numbers, addresses, websites, and company details. In production environments, this level of exposure should be minimized.

---

### API-03 – Public Task Data

**Risk:** Low

The `/todos` endpoint returned task-related information without authentication. This is acceptable for a demonstration API but would require access controls in production.

---

### API-04 – Public Comment Data

**Risk:** Low

The `/comments` endpoint returned publicly accessible comment data. Production systems should evaluate whether such information should require authentication.

---

### API-05 – Response Header Review

**Risk:** Informational

HTTP request and response headers were inspected. No sensitive server-side information was identified during the assessment.

---

### API-06 – Rate Limiting

**Risk:** Medium

Rate limiting was not clearly documented. Production APIs should implement request throttling to reduce abuse and automated attacks.

---

## Overall Assessment

**Overall Risk:** Low to Medium

The assessment identified expected characteristics of a public demonstration API. No critical security vulnerabilities were observed during the read-only assessment. The recommendations provided should be considered when developing production APIs.
