# Tenant Setup – Initial State

## Tenant
- Microsoft 365 Business Premium (Trial)
- Region: EU
- Management Portal: https://endpoint.microsoft.com
- Status: Active


## Admin Accounts
- Global Admin (setup-only): ga-setup
- Endpoint Admin (daily operations): mdm-admin

## Groups
- GRP-Admins-Endpoint
- GRP-Devices-Autopilot
- GRP-Users-Intune

## State
- No Intune policies configured
- No Conditional Access policies
- No devices enrolled

## Licensing
- Microsoft 365 Business Premium (Trial)

## Verification Status
- Tenant created
- Microsoft verification pending

## Admin Roles
- ga-setup: Global Administrator (setup-only)
- mdm-admin:
  - Intune Administrator
  - Endpoint Security Administrator


## Endpoint Manager
→ Devices
→ Device onboarding
→ Enrollment

Endpoint Manager
→ Devices
→ Configuration profiles
→ Create profile

LAB – Test Policy (Wrong Scope)

Policy intentionally assigned to wrong scope for learning purposes.

Device name

INTUNE-LAB

Devices
→ Configuration profiles
→ LAB – Test Policy (Wrong Scope)
→ Device status
