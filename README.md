# OWASP Juice Shop Security Assessment

## Overview

A security assessment of the OWASP Juice Shop vulnerable web application conducted as part of an academic Web Application Security project.

The assessment combined manual testing, dynamic application security testing (DAST), and static application security testing (SAST) to identify and analyse web application vulnerabilities.

## My Contributions

The assessment was completed as a group project. My individual contributions focused on:

- SQL Injection
- Broken Access Control / IDOR
- Forged Feedback
- Injection / Data Exposure
- Business Logic Flaw

## Methodology

The assessment involved:

- Local deployment of OWASP Juice Shop using Docker
- Browser-based application exploration
- Browser Developer Tools
- Burp Suite for HTTP request interception and modification
- Semgrep for SAST
- Manual vulnerability validation
- Vulnerability impact and mitigation analysis

## Vulnerabilities Assessed

| Vulnerability | Category | Testing Approach |
| --- | --- | --- |
| SQL Injection | OWASP A03:2021 Injection | Manual testing |
| Broken Access Control / IDOR | OWASP A01:2021 Broken Access Control | Browser Developer Tools / request manipulation |
| Forged Feedback | Broken Access Control | Burp Suite |
| Business Logic Flaw | OWASP A04:2021 Insecure Design | Manual testing |
| Injection / Data Exposure | Injection / Data Exposure | Manual testing / application behaviour |

## Key Findings

### SQL Injection

The Login Admin challenge demonstrated an SQL injection vulnerability that allowed authentication to be bypassed through manipulation of login input.

The assessment demonstrated how SQL injection can alter database query logic and bypass authentication.

Recommended mitigations included parameterised queries or prepared statements, input validation and appropriate database privileges.

See: `writeups/sql-injection.md`

### Broken Access Control / IDOR

Testing of basket functionality identified a broken-access-control issue where changing a user-controlled basket identifier could expose another user's data.

The assessment highlighted the importance of server-side authorisation and ownership checks.

See: `writeups/broken-access-control.md`

### Forged Feedback

Burp Suite was used to intercept a product-review request and modify user identity information submitted with the request.

The application accepted the modified identity rather than securely determining identity from the authenticated session.

See: `writeups/forged-feedback.md`

### Business Logic Flaw

The Payback Time challenge demonstrated a weakness in application business logic and input handling.

The finding showed that security problems are not always traditional injection vulnerabilities and that application logic itself can create exploitable conditions.

See: `writeups/business-logic.md`

### Injection / Data Exposure

The Change Bender's Password challenge demonstrated weaknesses involving input handling and exposure of sensitive functionality.

See: `writeups/password-injection.md`

## Security Testing Tools

- Burp Suite
- Semgrep
- Browser Developer Tools
- Docker
- OWASP Juice Shop

## Security Concepts Demonstrated

- SQL Injection
- Broken Access Control
- IDOR
- Authentication Bypass
- Business Logic Testing
- SAST
- DAST
- HTTP Request Analysis
- Input Validation
- Server-Side Authorisation
- Secure Coding Practices

## Academic Context

This was completed as part of a university Web Application Security module.

The repository is a cleaned portfolio representation of the assessment and does not contain the original university submission or identifying academic information.

## Disclaimer

OWASP Juice Shop is an intentionally vulnerable application designed for security education and testing. The techniques documented here were performed against the intentionally vulnerable application in an authorised educational environment.
