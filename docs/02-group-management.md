# Group Management

## Group Types Used
This environment uses **Security Groups** for identity and access management.

Security groups are used to:
- Control access to applications and services
- Assign licenses through group-based licensing
- Simplify user onboarding and offboarding

Microsoft 365 groups are not used in this lab.

---

## Membership Model
All groups use **Assigned membership**.

Reasons:
- Predictable access control
- Clear auditability
- Immediate visibility into group membership
- Avoids unintended access through dynamic rules

---

## Group Purpose Separation
Groups are designed with **single responsibility** in mind.

| Group Purpose | Example | Notes |
|--------------|--------|-------|
| User grouping | IT-Test-Users | General user grouping |
| License assignment | IT-Test-Users | Used for group-based licensing |
| Application access | (Future) | Used to grant app permissions |

While some groups may temporarily serve multiple purposes in a test environment, production environments should separate license and access groups where possible.

---

## Group Lifecycle Management
Common administrative actions include:
- Creating security groups
- Adding and removing members
- Reviewing group membership during access issues
- Deleting unused groups after validation

Group membership changes are validated through:
- User group membership view
- Application access testing
- License assignment confirmation

---

## Validation Checks
When troubleshooting group-related issues, the following checks are performed:
- Confirm correct group membership
- Verify group purpose and configuration
- Validate license assignment (if applicable)
- Allow time for propagation before making changes

---

## Evidence
- Group overview and membership  
  (`evidence/screenshots/groups/IT-Test-Users-overview.png`)
