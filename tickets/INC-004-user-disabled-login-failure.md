# INC-004 — User Unable to Sign In (Account Disabled)

## Summary
**User impact:** User is unable to sign in to Microsoft 365 services  
**Service/app:** Microsoft Entra ID / Microsoft 365  
**Priority:** Medium  
**Status:** Resolved

## Reported Symptoms
- User reports being unable to sign in
- Login attempt fails immediately

## Environment
- Tenant: Arcadia408 Microsoft Entra ID test tenant
- User: itp-user01
- Groups involved: IT-Test-Users
- Licensing involved: Microsoft 365 (group-based licensing)

## Investigation Timeline
1. Verified sign-in failure occurs immediately
2. Reviewed user account status in Entra ID
3. Confirmed user account is disabled
4. No license or group misconfiguration identified

## Evidence
- User account confirmed disabled in Microsoft Entra ID  
  [Account disabled screenshot](../evidence/screenshots/users/itp-user01-account-disabled.png)
- Authentication fails immediately; the sign-in process loops and does not complete  
  [Disabled sign-in behavior screenshot](../evidence/screenshots/sign-in-logs/itp-user01-disabled-signin.png)
- Successful authentication observed after account re-enabled  
  [Sign-in restored screenshot](../evidence/screenshots/sign-in-logs/itp-user01-signin-restored.png)


## Root Cause
- User account was disabled, preventing authentication to Microsoft 365 services.

## Resolution
- Re-enabled user account in Microsoft Entra ID after confirming no security or policy restrictions were in place.

## Verification
- Confirmed user account enabled
- Verified successful authentication to Microsoft 365 services

## Preventive / Follow-up
- Validate account status before initiating password resets
- Review administrative disablement reasons before re-enabling accounts
- Document account status changes for audit purposes
