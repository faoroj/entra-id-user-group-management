# INC-001 — User Can’t Access Application

## Summary
**User impact:** User is unable to access Microsoft 365 applications after account creation 
**Service/app:** Microsoft 365 / Microsoft Entra ID 
**Priority:** Medium 
**Status:** Resolved

## Reported Symptoms
- User can authenticate successfully
- Microsoft 365 portal loads, but no core applications are available
- Banner message indicates missing or recently assigned license

## Environment
- Tenant: Arcadia408 Microsoft Entra ID test tenant
- User: itp-user01 (ITP User One)
- Groups involved: IT-Test-Users
- Licensing involved: Microsoft 365 (group-based licensing via Microsoft 365 Admin Center)

## Investigation Timeline
1. Verified user account exists and is enabled
2. Confirmed successful authentication to the Microsoft 365 portal
3. Verified no licenses assigned directly to the user
4. Reviewed group memberships and confirmed the user is not a member of any licensing groups

## Evidence
- User account enabled with no assigned licenses  
  [User overview screenshot](../evidence/screenshots/users/itp-user01-overview.png)
- Licensing group contained no assigned licenses  
  [Group licensing screenshot](../evidence/screenshots/licensing/IT-Test-Users-license.png)
- Microsoft 365 license assigned to the IT-Test-Users group  
  [License assignment screenshot](../evidence/screenshots/licensing/IT-Test-Users-license-assigned.png)
- License successfully applied to the user  
  [User license state screenshot](../evidence/screenshots/licensing/itp-user01-license-applied.png)
- User can access Microsoft 365 apps after re-authentication  
  [User access restored screenshot](../evidence/screenshots/sign-in-logs/itp-user01-access-restored.png)



## Root Cause
- User was not added to the security group responsible for Microsoft 365 license assignment.

## Resolution
- Assigned a Microsoft 365 license to the IT-Test-Users security group using the Microsoft 365 Admin Center, allowing the affected user to receive the license through group-based assignment.


## Verification
- Confirmed Microsoft 365 license applied to itp-user01 via group membership
- Verified Microsoft 365 applications were accessible after user re-authentication

## Preventive / Follow-up
- Standardize the use of licensed security groups for user onboarding
- Validate license assignment during user creation to prevent access delays
