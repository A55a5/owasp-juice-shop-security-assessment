# Payback Time — Business Logic Flaw

## Overview

The Payback Time challenge demonstrated a weakness in application business logic and input handling.

## Testing

The application's functionality was tested manually to identify behaviour that could be manipulated through unexpected input.

The weakness demonstrated that security problems are not always caused by a traditional injection vulnerability; application logic itself can also create exploitable conditions.

## Impact

Business logic flaws can allow users to perform actions outside the intended rules of an application and may affect application integrity or financial/business processes.

## Recommended Mitigation

- Validate business rules server-side.
- Do not rely solely on client-side validation.
- Test abnormal and unexpected input values.
- Enforce limits and workflow requirements on the server.

## Classification

OWASP A04:2021 — Insecure Design.
