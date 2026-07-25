# OWASP Top 10 Notes

## Introduction

The OWASP Top 10 is a list of the most critical web application security risks published by the Open Worldwide Application Security Project (OWASP). It helps organizations identify and mitigate common web application vulnerabilities.

---

## A01: Broken Access Control

### Definition

Broken Access Control occurs when users can access resources or perform actions that they are not authorized to access.

### Example

A user changes a URL from:

/account/123

to:

/account/124

and gains access to another user's account information.

### Prevention

* Implement role-based access control (RBAC)
* Enforce authorization checks on the server side
* Use the principle of least privilege

---

## A02: Cryptographic Failures

### Definition

Sensitive information is not properly protected through encryption.

### Example

Passwords stored in plain text within a database.

### Prevention

* Use strong encryption algorithms
* Encrypt sensitive data in transit and at rest
* Hash passwords using secure algorithms such as bcrypt

---

## A03: Injection

### Definition

Injection vulnerabilities occur when untrusted input is interpreted as commands or queries.

### Example

SQL Injection allowing attackers to access database information.

### Prevention

* Use parameterized queries
* Validate user input
* Apply input sanitization

---

## A04: Insecure Design

### Definition

Security weaknesses resulting from poor application design.

### Example

No account lockout mechanism after multiple failed login attempts.

### Prevention

* Include security during the design phase
* Perform threat modeling
* Follow secure development practices

---

## A05: Security Misconfiguration

### Definition

Improperly configured systems expose security weaknesses.

### Example

Using default usernames and passwords.

### Prevention

* Remove unnecessary services
* Change default credentials
* Regularly review configurations

---

## A06: Vulnerable and Outdated Components

### Definition

Using outdated software, libraries, or frameworks containing known vulnerabilities.

### Example

Running an old version of a web framework with known security flaws.

### Prevention

* Keep software updated
* Monitor vulnerability advisories
* Remove unsupported components

---

## A07: Identification and Authentication Failures

### Definition

Weak authentication mechanisms allow unauthorized access.

### Example

Weak password policies or lack of multi-factor authentication.

### Prevention

* Enforce strong passwords
* Implement MFA
* Monitor authentication attempts

---

## A08: Software and Data Integrity Failures

### Definition

Failures related to software updates, code integrity, and trusted data sources.

### Example

Downloading software updates from untrusted sources.

### Prevention

* Verify software integrity
* Use digital signatures
* Secure CI/CD pipelines

---

## A09: Security Logging and Monitoring Failures

### Definition

Insufficient logging and monitoring prevent detection of attacks.

### Example

Failed login attempts are not recorded.

### Prevention

* Enable logging
* Monitor security events
* Implement alerting systems

---

## A10: Server-Side Request Forgery (SSRF)

### Definition

An attacker tricks a server into making requests to unintended resources.

### Example

A web application retrieves internal network resources on behalf of an attacker.

### Prevention

* Validate URLs
* Restrict outbound connections
* Use network segmentation

---

## Conclusion

The OWASP Top 10 highlights the most common and critical web application security risks. Understanding these vulnerabilities is essential for vulnerability assessment, penetration testing, and secure software development.
