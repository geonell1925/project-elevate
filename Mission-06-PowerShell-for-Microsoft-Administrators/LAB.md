# Mission 6 – PowerShell for Microsoft Administrators

## Lab Objective

Develop an automation-first mindset by applying PowerShell administration concepts to realistic Microsoft Entra ID and Microsoft 365 operational scenarios. The focus was placed on planning, validation, automation, governance, reporting, and operational safety rather than PowerShell syntax.

---

# Scenario 1 – Bulk User Onboarding

HR submitted a CSV containing 250 new employees requiring Microsoft Entra ID accounts, Microsoft 365 licenses, group memberships, and enterprise application access.

## Investigation

- Validated CSV data.
- Reviewed duplicate identities.
- Planned bulk automation.
- Considered logging and rollback.
- Identified failed records through logging.

## Lesson Learned

Automation should always begin with validated data before executing bulk onboarding.

---

# Scenario 2 – Bulk License Correction

Six hundred employees received the wrong Microsoft 365 license.

## Investigation

- Validated CSV.
- Determined whether licensing was direct or group-based.
- Planned rollback.
- Corrected licensing through automation.
- Logged failed records.

## Lesson Learned

Group-based licensing should be investigated before modifying individual user licenses.

---

# Scenario 3 – Department Transfer

One hundred eighty employees changed departments, including twenty-five privileged administrators.

## Investigation

- Validated identity information.
- Planned separate processing for privileged users.
- Reviewed RBAC and PIM assignments.
- Updated group memberships.
- Verified department changes.

## Lesson Learned

Privileged identities require additional validation and separate change management procedures.

---

# Scenario 4 – Security Incident Response

Forty user accounts were compromised during a phishing incident.

## Investigation

- Contained affected accounts.
- Revoked active sessions.
- Planned password resets.
- Required MFA re-registration.
- Generated completion reports.
- Coordinated post-incident review.

## Lesson Learned

Containment should always occur before automation during security incidents.

---

# Scenario 5 – Audit Reporting

Finance requested a report of users belonging to a security group.

## Investigation

- Generated CSV report.
- Identified terminated employees.
- Reviewed offboarding process.
- Recommended automation improvements.

## Lesson Learned

Reporting often exposes governance weaknesses that should be corrected through process improvement.

---

# Scenario 6 – MFA Compliance Audit

Compliance requested a report of active employees without MFA.

## Investigation

- Filtered disabled accounts.
- Removed guest identities.
- Excluded service accounts.
- Identified active users without MFA.
- Prioritized privileged administrators.

## Lesson Learned

Security remediation should follow risk-based prioritization.

---

# Scenario 7 – Enterprise Migration

Eight hundred fifty employees from an acquired company required migration into Microsoft Entra ID.

## Investigation

- Validated migration data.
- Coordinated with acquisition teams.
- Planned automation.
- Managed duplicate UPN failures.
- Continued successful migration while remediating failed accounts.

## Lesson Learned

Successful migrations depend on preparation, validation, communication, and controlled recovery rather than expecting zero failures.

---

# Scenario 8 – Enterprise Application Emergency

A critical vulnerability required immediate removal of enterprise application access.

## Investigation

- Restricted access through group assignments.
- Preserved Cybersecurity team access.
- Revoked application access.
- Generated completion reports.
- Participated in post-incident review.

## Lesson Learned

Group-based administration enables rapid, secure response during enterprise security incidents.

---

# Overall Lab Reflection

Mission 6 demonstrated that PowerShell is far more than scripting. It is an operational tool that enables administrators to automate repetitive work safely while improving governance, reporting, compliance, and identity lifecycle management. Every scenario reinforced the importance of validation, logging, rollback planning, verification, and documentation before introducing automation into production environments.
