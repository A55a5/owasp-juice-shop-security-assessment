# SQL Injection — Login Admin

## Overview

The Login Admin challenge demonstrated an SQL injection vulnerability that allowed authentication to be bypassed through manipulation of login input.

## Testing

The login form was tested with different inputs. SQL injection testing resulted in successful authentication without the valid password.

The assessment demonstrated that user-controlled input was being incorporated into database query logic without adequate protection.

## Impact

In a real-world application, SQL injection can potentially allow attackers to bypass authentication, access unauthorised data, modify database records or interfere with database operations, depending on the application's privileges and architecture.

## Recommended Mitigation

- Use parameterised queries or prepared statements.
- Validate input.
- Apply least-privilege database permissions.
- Avoid constructing SQL queries directly from untrusted input.

## OWASP Classification

OWASP A03:2021 — Injection.# SQL Injection — Login Admin

## Overview

The Login Admin challenge demonstrated an SQL injection vulnerability that allowed authentication to be bypassed through manipulation of login input.

## Testing

The login form was tested with different inputs. SQL injection testing resulted in successful authentication without the valid password.

The assessment demonstrated that user-controlled input was being incorporated into database query logic without adequate protection.

## Impact

In a real-world application, SQL injection can potentially allow attackers to bypass authentication, access unauthorised data, modify database records or interfere with database operations, depending on the application's privileges and architecture.

## Recommended Mitigation

- Use parameterised queries or prepared statements.
- Validate input.
- Apply least-privilege database permissions.
- Avoid constructing SQL queries directly from untrusted input.

## OWASP Classification

OWASP A03:2021 — Injection.
