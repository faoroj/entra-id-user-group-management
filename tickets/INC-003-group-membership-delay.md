# INC-003 — Group Membership Change Not Reflected Immediately

## Summary
**User impact:** User is unable to access Microsoft 365 resources immediately after a group membership change  
**Service/app:** Microsoft Entra ID / Microsoft 365  
**Priority:** Low  
**Status:** Resolved

## Reported Symptoms
- User reports being added to a security group
- Expected access not immediately available 

## Environment
- Tenant: Arcadia408 Microsoft Entra ID test tenant
- User: itp-user01
- Groups involved: IT-Test-Users
- Licensing involved: Microsoft 365 (group-based licensing)

## Investigation Timeline
1. Verified user account is enabled
2. Confirmed user was added to the IT-Test-Users security group
3. Observed a delay between group membership change and effective access
4. Validated no configuration issues with group or licensing

## Evidence
- User successfully added to IT-Test-Users security group  
  (`evidence/screenshots/groups/itp-user01-group-added.png`)
- Microsoft 365 service access is not immediately available following a group membership change  
  (`evidence/screenshots/sign-in-logs/itp-user01-access-delay.png`)

## Root Cause
Group membership changes require time to propagate across Microsoft Entra ID and dependent Microsoft 365 services, resulting in a temporary delay before access becomes effective.


## Resolution
No configuration changes were required. Allowed time for group membership changes to propagate and monitored access until successful.


## Verification
- Confirmed group membership reflected correctly on the user object
- Verified access to Microsoft 365 resources after propagation


## Preventive / Follow-up
- Communicate expected group membership propagation delays to users
- Avoid repeated group changes during short timeframes
- Validate access after propagation before escalating
