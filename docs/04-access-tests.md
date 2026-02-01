# Access Validation Tests

## Access Validation Overview
Access validation ensures that identity, group, and licensing changes result in the expected user experience.

Validation is performed from both:
- The administrator perspective (Entra ID / Microsoft 365 Admin Center)
- The user perspective (Microsoft 365 sign-in and application access)

---

## User-Side Access Tests
User access is validated by signing in as the affected user and confirming access to Microsoft 365 services.

Common checks include:
- Successful authentication
- Visibility of Microsoft 365 applications
- Ability to launch applications such as Outlook or Word
- Absence of access or licensing error messages

User-side testing is performed using:
- Private/incognito browser sessions
- Fresh authentication after changes

---

## Admin-Side Validation Checks
After access-related changes, administrators verify:
- User account enabled status
- Correct group membership
- License assignment state
- License assignment path (Inherited vs Direct)
- Enabled service plans

These checks help confirm configuration correctness before escalating issues.

---

## Re-Authentication Requirements
Changes to identity, group membership, or licensing often require users to:
- Sign out and sign back in
- Wait for propagation to complete

Immediate access is not always expected due to service propagation behavior.

---

## Expected Delays
The following delays are considered normal:
- Group membership propagation
- License inheritance via groups
- Service provisioning (e.g., Exchange Online mailbox creation)

Access validation should account for these delays before corrective action is taken.

---

## Validation Outcomes
Access validation results in one of the following outcomes:
- Access confirmed and functioning as expected
- Access delayed due to propagation
- Access blocked due to misconfiguration or account state

Each outcome determines whether further investigation or action is required.

---

## Evidence
- User access restored after licensing and provisioning  
  (`evidence/screenshots/sign-in-logs/itp-user01-access-restored.png`)
