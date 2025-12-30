## Tenant Verification (Initial Setup)

Tenant verification pending after Business Premium trial creation.
Access to Entra ID and Endpoint Manager is restricted during this phase.

## Tenant Rebuild (Billing Verification Deadlock)

Initial tenant entered a stuck verification state (>7 days).
Billing actions were blocked while organization fields were read-only.
Decision: discard tenant and rebuild clean.

Lesson learned:
- If verification exceeds ~5 days with billing blocked, rebuild is faster than waiting.

  
Conditional Access & Compliance (Practice Lab)

Lesson learned:

- Configuration Policies enforce state but may not provide reliable or immediate reporting.
- Compliance Policies evaluate state and are the authoritative source for device compliance.
- Conditional Access is evaluated per sign-in, not per device check-in.
- “Not applied” in Conditional Access does not indicate misconfiguration, only that scope or conditions did not match.
- Device-level views (device compliance, device configuration) are more reliable than policy summary dashboards.
