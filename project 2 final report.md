# Vulnerability Assessment Report

---

# Executive Summary
This report presents the results of a vulnerability assessment conducted on a deliberately vulnerable web application in a controlled lab environment. The objective of this assessment was to understand basic web application security concepts, including authentication mechanisms, session management, and common vulnerabilities based on OWASP Top 10.

The assessment identified several security observations related to authentication handling and session management. These findings are documented along with risk ratings and recommendations for improvement.

---

# Scope
The scope of this assessment is limited to:

- Target application: OWASP Juice Shop / DVWA / Metasploitable (lab environment)
- Web application authentication system
- Session management and cookie handling
- Network traffic observation during login and interaction

Out of scope:
- Real-world production systems
- External networks or services
- Exploitation beyond controlled lab testing

---

# Methodology
The following methodology was used during the assessment:

1. Set up and accessed the vulnerable web application in a controlled lab environment.
2. Created a test user account for authentication testing.
3. Performed login attempts using valid and invalid credentials.
4. Captured HTTP/HTTPS traffic using browser Developer Tools.
5. Analyzed login requests, responses, and session cookies.
6. Observed session behavior during login and logout actions.
7. Mapped observations to OWASP Top 10 categories.

This assessment followed a black-box testing approach, where no internal source code was reviewed.

---

# Tools Used

- Mozilla Firefox / Google Chrome (Web Browser)
- Browser Developer Tools (Network tab, Application/Storage tab)
- OWASP Juice Shop / DVWA / Metasploitable (Target Lab Application)
- Optional: Burp Suite Community Edition / OWASP ZAP

---

# Findings

## Finding 1: Authentication Request Exposure
- Login credentials were transmitted via HTTP POST request.
- Username and password were visible in the request payload.

**Impact:**
If not properly secured with HTTPS, credentials could be intercepted.

**OWASP Category:**
A02: Cryptographic Failures

**Risk Level:**
Medium

---

## Finding 2: Session Cookie Generation
- Session cookies were generated after successful login.
- Cookie was used to maintain user authentication state.

**Impact:**
Session handling depends on secure cookie configuration.

**OWASP Category:**
A07: Identification and Authentication Failures

**Risk Level:**
Medium

---

## Finding 3: Session Persistence Behavior
- Session remained active during page navigation.
- Logout invalidated session in most cases (based on observation).

**Impact:**
Improper session termination could lead to unauthorized access.

**OWASP Category:**
A07: Identification and Authentication Failures

**Risk Level:**
Low to Medium

---

# Risk Ratings Summary

- Low: 1 finding
- Medium: 2 findings
- High: 0 findings
- Critical: 0 findings

---

# Recommendations

- Enforce HTTPS for all authentication requests
- Implement secure session management practices
- Enable HttpOnly and Secure flags on cookies
- Use strong password policies
- Implement session expiration and regeneration after login
- Apply rate limiting on login endpoints

---

# Conclusion
The vulnerability assessment provided insights into how web applications handle authentication and session management. While the tested environment is intentionally vulnerable, the findings highlight common security weaknesses found in real-world applications.

Improving authentication security, session handling, and transport encryption can significantly reduce the risk of unauthorized access and data exposure.

---

# Evidence

- Login page screenshot
- Network request capture (login POST request)
- Session cookie observation
- Application behavior screenshots
