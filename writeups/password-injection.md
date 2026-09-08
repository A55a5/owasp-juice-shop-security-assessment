# Change Bender's Password — Injection / Data Exposure

## Overview

The Change Bender's Password challenge was assessed as an injection/data-exposure issue involving weak input handling.

## Testing

The functionality was tested as part of the Juice Shop security assessment and demonstrated weaknesses in how input was handled by the application.

## Impact

Weak input handling around sensitive account functionality can expose or compromise security-sensitive operations.

## Recommended Mitigation

- Validate and sanitise input appropriately.
- Protect sensitive account functionality with strong authorisation checks.
- Avoid exposing sensitive information unnecessarily.
- Apply secure handling practices to password-related functionality.

## Classification

Injection / Data Exposure.
