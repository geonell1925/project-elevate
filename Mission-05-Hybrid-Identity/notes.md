# Mission 5 – Hybrid Identity

## Introduction

Mission 5 focused on understanding how identities move from an on-premises Active Directory environment into Microsoft Entra ID using Microsoft Entra Connect. The emphasis was not only on synchronization, but on understanding the complete identity lifecycle from account creation to authentication, authorization, and enterprise application access.

Throughout this mission, I learned to distinguish between object synchronization, Password Hash Synchronization (PHS), authentication, and authorization while applying a structured troubleshooting methodology to Hybrid Identity scenarios.

---

# Hybrid Identity

Hybrid Identity allows organizations to maintain identities in Active Directory while extending authentication and identity services to Microsoft Entra ID and Microsoft 365.

The identity flow generally follows this process:

- User created in Active Directory
- Microsoft Entra Connect synchronizes the object
- Password Hash Synchronization transfers the password hash
- Microsoft Entra ID authenticates cloud access
- Enterprise Applications authorize access based on assigned permissions

Understanding each stage is essential because a failure at one stage does not necessarily indicate a failure at another.

---

# Microsoft Entra Connect

Microsoft Entra Connect is responsible for synchronizing identity information from Active Directory to Microsoft Entra ID.

Important validation points include:

- Connector health
- Last successful synchronization
- Delta synchronization
- Full synchronization
- Synchronization errors
- Synchronization filtering
- Organizational Unit filtering

If existing users synchronize successfully while newly created users do not, the investigation should focus on the onboarding process rather than assuming a Microsoft Entra Connect failure.

---

# Password Hash Synchronization

Password Hash Synchronization is separate from object synchronization.

A user object may successfully synchronize to Microsoft Entra ID while the updated password hash has not yet synchronized.

When troubleshooting password-related issues, administrators should verify:

- Password changed successfully in Active Directory
- Password Hash Synchronization status
- Synchronization timing
- Delta synchronization completion

---

# Organizational Unit Synchronization

OU placement plays an important role in Hybrid Identity.

Administrators should verify:

- The user exists in the correct OU.
- The OU is included within Microsoft Entra Connect synchronization.
- No filtering rules exclude the object.

Incorrect OU placement is a common cause of newly created users failing to appear in Microsoft Entra ID.

---

# User Lifecycle Management

Identity lifecycle events frequently introduce synchronization and authorization issues.

Examples include:

- User onboarding
- Promotions
- Department transfers
- Role changes
- Employee termination

A consistent troubleshooting habit developed during this mission was asking:

**"What changed before the issue occurred?"**

This question often identifies the root cause quickly.

---

# Enterprise Applications

Hybrid Identity extends beyond Microsoft 365.

Enterprise Applications rely on Microsoft Entra ID for:

- Authentication
- Authorization
- Group assignments
- Provisioning
- SAML claims
- Single Sign-On

Successful Microsoft 365 authentication does not guarantee successful application authorization.

---

# Conditional Access

Conditional Access evaluates authentication conditions such as:

- User identity
- Device compliance
- Named Locations
- Network location
- Risk level
- Multi-Factor Authentication requirements

Authentication failures occurring only from specific locations should prompt administrators to review Conditional Access policies before investigating synchronization.

---

# Audit Logs and Sign-in Logs

Logs provide evidence during Hybrid Identity investigations.

Useful log sources include:

- Microsoft Entra Sign-in Logs
- Audit Logs
- Microsoft Entra Connect Synchronization Logs
- Enterprise Application Logs

Evidence should always guide troubleshooting rather than assumptions.

---

# Engineering Mindset

Mission 5 reinforced several engineering principles:

- Separate object synchronization from password synchronization.
- Separate authentication from authorization.
- Always identify the scope.
- Determine what changed before the incident.
- Compare with a known working user.
- Gather evidence before making changes.
- Contain security risks before continuing technical investigation.
- Validate the solution before closing the incident.
