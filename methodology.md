# Methodology

## 1. Application Deployment

OWASP Juice Shop was deployed locally using Docker for controlled security testing.

## 2. Application Reconnaissance

The application was explored through the browser to understand authentication, product, basket and feedback functionality and identify areas suitable for testing.

## 3. Dynamic Testing

Browser Developer Tools were used to inspect network requests and responses.

Burp Suite was used to intercept and modify HTTP requests to test how the application handled manipulated user-controlled data.

## 4. Static Testing

Semgrep was used to scan the Juice Shop source code for security-relevant coding patterns.

The SAST results were reviewed and compared with vulnerabilities identified during dynamic testing.

## 5. Vulnerability Validation

Potential findings were manually tested against the running application to confirm whether the suspected behaviour could be reproduced.

## 6. Impact and Mitigation

For each relevant finding, the assessment considered potential security impact and recommended defensive measures such as:

- Parameterised queries
- Input validation
- Output encoding
- Server-side authorisation
- Session-based identity validation
- Rate limiting
- Secure authentication controls
- Appropriate access-control enforcement

Note: the above are recommended mitigations, not measures that were implemented during the assessment.
