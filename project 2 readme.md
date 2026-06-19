# Vulnerability Assessment Project – OWASP Juice Shop

## Overview

This project documents a vulnerability assessment performed against OWASP Juice Shop in a controlled lab environment. The purpose of the assessment was to gain practical experience in web application security testing, authentication analysis, session management, vulnerability identification, risk assessment, and professional security reporting.

**Target:** OWASP Juice Shop  
**Assessment Type:** Vulnerability Assessment  
**Environment:** Local Lab Environment  
**Assessment Date:** June 2026

---

## Objectives

- Understand authentication mechanisms
- Analyze session management
- Observe web application traffic
- Practice vulnerability assessment methodology
- Apply OWASP Top 10 concepts
- Develop professional report-writing skills

---

## Scope

The assessment focused on:

- User authentication process
- Login request analysis
- Session management
- Cookie handling
- Network traffic observation
- Basic vulnerability identification

### Out of Scope

- Production systems
- Third-party services
- Denial-of-service testing
- Unauthorized exploitation

---

## Methodology

The assessment followed a basic black-box testing approach:

1. Set up OWASP Juice Shop in a controlled environment.
2. Created a test user account.
3. Monitored network traffic using browser Developer Tools.
4. Captured authentication requests and responses.
5. Analyzed session cookies and authentication tokens.
6. Observed application behavior during login and logout.
7. Documented findings and assigned risk ratings.

---

## Tools Used

| Tool | Purpose |
|--------|---------|
| OWASP Juice Shop | Vulnerable web application |
| Firefox / Chrome | Web browser |
| Browser Developer Tools | Network traffic analysis |
| OWASP ZAP (Optional) | Web application security testing |
| Burp Suite Community (Optional) | Traffic interception and analysis |
| GitHub | Project documentation |

---

## Authentication Analysis

### Login Endpoint

Example endpoint observed:

```http
POST /rest/user/login
```

### Request Method

```http
POST
```

### Authentication Flow

1. User enters email and password.
2. Browser sends POST request to login endpoint.
3. Server validates credentials.
4. Authentication token/session is generated.
5. Browser stores session information.
6. Subsequent requests include authentication data.

---

## Session Management Analysis

### Observations

- Session established after successful authentication.
- Authentication token stored by application.
- User remained authenticated during active session.
- Session terminated after logout.

### Security Controls Observed

- Session-based authentication
- Token management
- Logout functionality

---

## Findings

### Finding 1 – Authentication Request Visibility

**Description**

Authentication requests were observable within browser Developer Tools.

**Impact**

Credentials may be exposed if transmitted without secure transport mechanisms.

**OWASP Category**

A02: Cryptographic Failures

**Risk Rating**

Medium

---

### Finding 2 – Session Token Generation

**Description**

Session token was generated following successful authentication.

**Impact**

Improper token handling may increase risk of unauthorized session reuse.

**OWASP Category**

A07: Identification and Authentication Failures

**Risk Rating**

Medium

---

### Finding 3 – Session Persistence

**Description**

Authenticated session remained active until logout.

**Impact**

Improper session expiration could increase exposure to session hijacking risks.

**OWASP Category**

A07: Identification and Authentication Failures

**Risk Rating**

Low

---

## Risk Rating Summary

| Severity | Count |
|-----------|---------|
| Critical | 0 |
| High | 0 |
| Medium | 2 |
| Low | 1 |

---

## Recommendations

- Enforce HTTPS for all authentication traffic.
- Implement secure cookie attributes.
- Enable HttpOnly cookies.
- Enable Secure cookie flags.
- Use strong password policies.
- Implement session expiration controls.
- Apply rate limiting on authentication endpoints.
- Consider multi-factor authentication (MFA).

---

## Screenshots

### Login Page
_Add screenshot here_

### Authentication Request
_Add screenshot here_

### Session Cookie Analysis
_Add screenshot here_

### Network Traffic Capture
_Add screenshot here_

---

## Key Skills Demonstrated

- Vulnerability Assessment
- Web Application Security
- Authentication Analysis
- Session Management Analysis
- OWASP Top 10 Awareness
- Risk Assessment
- Security Documentation
- Technical Reporting
- GitHub Portfolio Development

---

## Learning Outcomes

This project improved practical understanding of:

- Web application architecture
- Authentication workflows
- Session management mechanisms
- Security testing methodology
- Professional cybersecurity reporting

---

## Disclaimer

This assessment was performed exclusively within a controlled lab environment using intentionally vulnerable applications. No unauthorized testing was conducted against production systems or third-party targets.
