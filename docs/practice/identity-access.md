## Conditional Access – Practice Lab

### Conditional Access: Require compliant device

- CA policy scoped to test user and single cloud app
- Grant access only if device is marked compliant
- Intune provides device compliance signal
- Entra ID enforces access decision during sign-in

Result:
- Compliant device → access allowed
- Non-compliant device → access blocked

Key takeaway:
Conditional Access enforces device compliance at authentication time, not during configuration.

---

### Validation via Sign-in Logs

- Policy evaluation verified in Entra ID sign-in logs
- “Applied” indicates the policy was relevant for the sign-in
- “Not applied” indicates scope or target did not match

Key takeaway:
Sign-in logs are the authoritative source for Conditional Access evaluation.

---

### Security Defaults Interaction

- Security Defaults must be disabled to create custom CA policies
- Disabling Security Defaults can trigger Microsoft to auto-create baseline CA policies
- These baseline policies also apply to Global Administrators

Key takeaway:
Security Defaults and custom Conditional Access policies are mutually exclusive.
