# INC-001 — User Can’t Access Application

## Summary
**User impact:**  
**Service/app:**  
**Priority:** Low / Medium / High  
**Status:** Resolved

## Reported Symptoms
- User can authenticate successfully
- Microsoft 365 portal loads, but no core applications are available
- Banner message indicates missing or recently assigned license

## Environment
- Tenant:
- User:
- Groups involved:
- Licensing involved:

## Investigation Timeline
1. Verified user account exists and is enabled
2. Confirmed successful authentication to the Microsoft 365 portal
3. Verified no licenses assigned directly to the user
4. Reviewed group memberships and confirmed the user is not a member of any licensing groups

## Evidence
- User account enabled with no assigned licenses  
  (`evidence/screenshots/users/itp-user01-overview.png`)
- User sign-in successful, but no app access  
  (`evidence/screenshots/sign-in-logs/itp-user01-no-access.png`)

## Root Cause
- User was not added to the security group responsible for Microsoft 365 license assignment.

## Resolution
-

## Verification
- What you checked to confirm the fix: 

## Preventive / Follow-up
- 
