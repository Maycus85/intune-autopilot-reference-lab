## Test Policy – Wrong Scope (Learning Case)

Policy:
- Platform: Windows 10 and later
- Type: Settings catalog
- Setting: Device name
- Assignment: Users (All users)

Observed status:
- Device status: Not applicable

Lesson:
- Device-based settings assigned to users result in Not applicable
- Scope must match setting type (device vs user)


### Learning Case: Device policy assigned to users

- Policy: BitLocker – Require device encryption
- Initial assignment: Users (All users)
- Result: No evaluation, all status counters = 0
- Root cause: Device-only setting without valid evaluation context
- Fix: Reassigned policy to Devices (All devices)
- Result after fix: Policy evaluated successfully

Key takeaway:
Policy evaluation requires a matching scope AND an evaluation context.



### Learning Case: Configuration vs Compliance

- Configuration Policy used to enforce BitLocker
- No visible status despite successful enforcement
- Reason: Device already met required state

- Compliance Policy used to evaluate BitLocker status
- Immediate visibility of device compliance
- Device marked Compliant = Yes

Key takeaway:
Configuration policies enforce state.
Compliance policies evaluate state and provide reporting for Conditional Access.


### Final Observation: Evaluation vs Reporting

- Device shows Configuration Policy: Succeeded
- Device shows Compliance Policies: Compliant
- Configuration policy overview remained at 0 counts
- Compliance policy overview updated after aggregation

- This behavior was observed in a fresh tenant with a single enrolled device,
making reporting delays more visible than in larger environments.

Conclusion:
Device-level views are authoritative.
Policy-level summaries are delayed and not suitable for troubleshooting.
