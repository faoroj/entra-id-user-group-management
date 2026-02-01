# INC-002 — License assigned but not applying to the user

## Summary
**User impact:** User is unable to access Microsoft 365 applications after license assignment  
**Service/app:** Microsoft 365 / Microsoft Entra ID  
**Priority:** Medium  
**Status:** Resolved

## Reported Symptoms
- User reports being added to a licensed security group
- Microsoft 365 applications are still unavailable

## Environment
- Tenant: Arcadia408 Microsoft Entra ID test tenant
- User: itp-user01
- Groups involved: IT-Test-Users
- Licensing involved: Microsoft 365 (group-based licensing)

## Investigation Timeline
1. Verified user account is enabled and active
2. Confirmed user is a member of licensed security group (IT-Test-Users)
3. Reviewed license assignment status on the user object
4. Observed a delay between group membership change and license application


## Evidence
- License successfully applied via group-based licensing  
  [User license state screenshot](../evidence/screenshots/licensing/itp-user01-license-applied.png)


## Root Cause
- Microsoft 365 license assignment via group-based licensing was delayed due to normal propagation timing between Entra ID and Microsoft 365 services.


## Resolution
- No configuration changes were required. Allowed time for group-based licensing to propagate and monitored license assignment status until successful.


## Verification
- Confirmed Microsoft 365 license successfully applied to the user via group membership
- Verified user access to Microsoft 365 applications after re-authentication


## Preventive / Follow-up
- Educate users and service desk staff on expected group-based licensing propagation delays
- Avoid unnecessary direct license assignments during initial access delays

