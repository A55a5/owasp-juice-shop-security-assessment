# Forged Feedback — Broken Access Control

## Overview

The Forged Feedback challenge demonstrated a broken-access-control issue involving user identity data submitted with a product review.

## Testing

Burp Suite was used to intercept the HTTP request associated with submitting a product review.

The user identity/email parameter was modified before the request was forwarded to the application.

The application accepted the modified identity rather than securely determining the identity from the authenticated session.

## Impact

This could allow an attacker to submit content while impersonating another user, potentially damaging trust and application integrity.

## Recommended Mitigation

- Determine user identity from the authenticated server-side session.
- Do not trust client-supplied identity fields.
- Enforce server-side authorisation.
- Validate session ownership and permissions.

## Classification

Broken Access Control.
