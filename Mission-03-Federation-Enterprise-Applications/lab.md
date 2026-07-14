# Mission 3 Lab

## Objective

Apply Microsoft Entra ID federation concepts to real-world enterprise scenarios and develop a structured troubleshooting methodology for authentication and authorization issues.

---

## Scenario 1 – Understanding Single Sign-On

A CEO accesses Salesforce by clicking **Sign in with Microsoft**. Microsoft Entra ID authenticates the user and issues a security token. Salesforce trusts Microsoft Entra as the Identity Provider and validates the token instead of asking for another username and password.

**Lesson Learned**

One authentication allows access to multiple trusted applications through Single Sign-On (SSO).

---

## Scenario 2 – Federation

Explored why organizations use federation instead of maintaining separate credentials for every application.

**Findings**

- Centralized identity management
- Easier onboarding and offboarding
- Simplified user lifecycle management
- Reduced administrative overhead
- Improved user experience through Single Sign-On

---

## Scenario 3 – Tokens and Claims

Learned that Microsoft Entra issues a security token after successful authentication.

The token contains claims such as:

- Display Name
- Email Address
- Department
- Group Membership
- Role
- Employee ID

Enterprise Applications validate these claims to determine what the authenticated user is authorized to access.

---

## Scenario 4 – User Removed from an Administrative Group

A CEO was removed from the IT Admin group but continued to have administrator access.

**Root Cause**

The application continued trusting an existing valid token containing the previous claims.

**Resolution**

Revoke active sessions or wait for token expiration so that Microsoft Entra issues a new token reflecting the updated group membership.

---

## Scenario 5 – Salesforce Authentication Outage

More than 400 users were unable to access Salesforce while Microsoft 365 services remained operational.

**Investigation**

- Confirm business impact
- Verify Microsoft 365 authentication
- Review Enterprise Application configuration
- Review audit logs
- Investigate SAML certificate expiration
- Coordinate with the Salesforce application team
- Review recent deployments and configuration changes

---

## Scenario 6 – Blank Dashboard After Successful Sign-In

The CFO authenticated successfully but only received a blank dashboard inside Salesforce.

**Investigation**

Since authentication succeeded, the investigation shifted toward authorization.

Areas reviewed included:

- Enterprise Application assignments
- Application roles
- Group membership
- Claims
- Provisioning
- Audit logs
- Recent application changes

---

## Skills Developed

- Identity troubleshooting
- Authentication versus Authorization
- Federation concepts
- Enterprise Application troubleshooting
- Root cause analysis
- Business impact assessment
- Vendor coordination
- Identity Engineering methodology
