# Group-Based Licensing

## Licensing Model Overview
Licensing in this environment is managed using **group-based licensing**.

Instead of assigning licenses directly to individual users, Microsoft 365 licenses are assigned to security groups. Users inherit licenses automatically based on group membership.

This approach provides:
- Consistent license assignment
- Easier onboarding and offboarding
- Reduced administrative overhead
- Improved auditability

---

## Where Licensing Is Managed
While user and group objects are managed in Microsoft Entra ID, **license assignment is performed in the Microsoft 365 Admin Center**.

This separation requires administrators to validate both:
- Group membership (Entra ID)
- License assignment state (Microsoft 365)

---

## License Assignment Flow
1. Security group is created
2. Microsoft 365 license is assigned to the group
3. User is added to the group
4. License is inherited by the user
5. Enabled service plans become available

License assignment is reflected on the user object as:
- **Assignment path:** Inherited (Group Name)

---

## Propagation Behavior
Group-based licensing does not apply instantly.

After group membership changes:
- License application may be delayed
- Service plans may appear inactive temporarily
- User access may not be immediately available

This behavior is expected and should be monitored before making changes.

---

## Validation Checks
When verifying licensing state, administrators confirm:
- User is a member of the correct licensing group
- License is assigned to the group
- License state on the user object is Active
- Assignment path indicates group inheritance
- User can access Microsoft 365 applications after re-authentication

---

## Common Misconfigurations
Examples of issues that can impact licensing:
- User added to a group without an assigned license
- License assigned directly to the user instead of a group
- Insufficient available licenses in the tenant
- Propagation delay misinterpreted as failure

---

## Evidence
- Group license assignment  
  (`evidence/screenshots/licensing/IT-Test-Users-license-assigned.png`)
- User license inherited via group  
  (`evidence/screenshots/licensing/itp-user01-license-applied.png`)
