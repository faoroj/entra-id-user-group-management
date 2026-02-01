# User Management

## User Creation
Users are created via the Microsoft Entra Admin Center with the following defaults:
- User type: Member
- Password: Auto-generated
- Require password change at first sign-in: Enabled
- No licenses or groups assigned by default

This allows controlled access assignment via groups.

## Account State Management
Common actions performed:
- Account enable/disable
- Password reset
- User deletion (soft delete)
- User restoration from deleted users

## Validation Checks
When troubleshooting user issues, the following are verified:
- Account enabled status
- Sign-in eligibility
- Assigned licenses
- Group memberships

## Example User
- User: itp-user01
- State: Enabled
- Initial access: No licenses, no groups

**Evidence:**  
`evidence/screenshots/users/itp-user01-overview.png`
