## Tenant Verification (Initial Setup)

Tenant verification pending after Business Premium trial creation.
Access to Entra ID and Endpoint Manager is restricted during this phase.

## Tenant Rebuild (Billing Verification Deadlock)

Initial tenant entered a stuck verification state (>7 days).
Billing actions were blocked while organization fields were read-only.
Decision: discard tenant and rebuild clean.

Lesson learned:
- If verification exceeds ~5 days with billing blocked, rebuild is faster than waiting.

- 
