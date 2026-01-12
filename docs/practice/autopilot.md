# Windows Autopilot – Lab Walkthrough

## Goal
Implement and validate a full Windows Autopilot user-driven deployment
including hardware hash registration, profile assignment and OOBE behavior.

---

## Key Steps

1. Created Windows 11 Hyper-V VM (Gen2, TPM enabled)
2. Installed Windows until first OOBE screen
3. Collected hardware hash using Get-WindowsAutopilotInfo (-Online)
4. Imported device into Windows Autopilot
5. Assigned Autopilot deployment profile (User-Driven, Entra ID join)
6. Triggered clean OOBE reset
7. Completed Autopilot-driven setup with Entra user

---

## Validation

- Device recognized as Autopilot device before user login
- OOBE forced Entra ID authentication (no local account possible)
- Device automatically enrolled into Microsoft Intune
- Enrollment profile visible in Intune device details
- Device compliant after deployment

---

## Key Learnings

- Autopilot identifies the **device first**, not the user
- Hardware hash must be registered **before** OOBE
- Entra Join + Intune enrollment ≠ Autopilot
- Profile assignment is required before reset
- Inconsistent OOBE states require full reset (WinRE)

---

## Result

Successful end-to-end Autopilot deployment in lab environment.
