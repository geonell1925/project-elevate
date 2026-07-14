# Mission 5 – Hybrid Identity

## Lab Objective

Develop practical Hybrid Identity troubleshooting skills by investigating synchronization, authentication, Password Hash Synchronization, enterprise application integration, Conditional Access, and user lifecycle scenarios involving Active Directory and Microsoft Entra ID.

---

# Scenario 1 – New User Not Synchronizing

A newly created Active Directory user successfully authenticated to the domain but did not appear in Microsoft Entra ID.

## Investigation

- Confirmed issue affected only one user.
- Verified Microsoft Entra Connect health.
- Reviewed Organizational Unit placement.
- Checked synchronization timing.
- Considered manual Delta Synchronization.
- Verified synchronization status before making changes.

## Lesson Learned

Object synchronization should be investigated before authentication when users fail to appear in Microsoft Entra ID.

---

# Scenario 2 – Password Synchronization

A user changed their Active Directory password but Microsoft 365 continued accepting the old password.

## Investigation

- Confirmed password change in Active Directory.
- Verified Password Hash Synchronization.
- Considered synchronization delay.
- Reviewed Microsoft Entra Connect synchronization status.
- Considered manual Delta Synchronization.

## Lesson Learned

Object synchronization and Password Hash Synchronization are separate processes.

---

# Scenario 3 – User Exists but Cannot Authenticate

The user synchronized successfully into Microsoft Entra ID but authentication to Microsoft 365 failed.

## Investigation

- Confirmed object synchronization.
- Investigated Password Hash Synchronization.
- Verified account status.
- Reviewed synchronization logs.
- Confirmed authentication path before investigating security policies.

## Lesson Learned

Successful object synchronization does not guarantee successful authentication.

---

# Scenario 4 – Twenty New Employees Missing

Twenty newly created Active Directory users failed to synchronize while existing users synchronized successfully.

## Investigation

- Confirmed Microsoft Entra Connect health.
- Verified Organizational Unit placement.
- Reviewed synchronization filtering.
- Validated userPrincipalName values.
- Reviewed batch onboarding process.
- Examined synchronization logs.

## Lesson Learned

When only newly created users are affected, investigate the onboarding process before the synchronization platform.

---

# Scenario 5 – Terminated Employee Still Active

A disabled Active Directory account continued accessing Microsoft 365.

## Investigation

- Classified as a security incident.
- Revoked active sessions.
- Verified account disablement.
- Reviewed synchronization status.
- Initiated Delta Synchronization.
- Reviewed group memberships and application assignments.

## Lesson Learned

Contain security risks first, then investigate synchronization and identity lifecycle processes.

---

# Scenario 6 – Salesforce Authentication Failure

Several users authenticated to Microsoft 365 but failed to access Salesforce.

## Investigation

- Eliminated Microsoft 365 authentication.
- Reviewed Enterprise Application assignments.
- Verified group membership.
- Reviewed SAML claims.
- Examined provisioning.
- Reviewed audit logs and sign-in logs.

## Lesson Learned

Enterprise Application authorization should be investigated separately from Microsoft 365 authentication.

---

# Scenario 7 – Remote Authentication Failure

Users authenticated successfully inside the office but failed authentication while working remotely.

## Investigation

- Classified as a business-impacting incident.
- Reviewed Conditional Access.
- Examined Named Locations.
- Reviewed Microsoft Entra Sign-in Logs.
- Considered VPN requirements where applicable.
- Coordinated investigation across multiple IT teams.

## Lesson Learned

Location-specific authentication failures often indicate Conditional Access rather than synchronization issues.

---

# Scenario 8 – Finance Manager Promotion

A recently promoted Finance Manager successfully authenticated to Microsoft 365 but could not access the Finance application.

## Investigation

- Reviewed group membership.
- Compared with a working Finance Manager.
- Verified group-based provisioning.
- Reviewed SAML claims.
- Examined Enterprise Application logs.
- Considered Identity Governance approval workflows.

## Lesson Learned

Identity lifecycle events frequently introduce authorization issues within enterprise applications.

---

# Overall Lab Reflection

Mission 5 strengthened my ability to troubleshoot Hybrid Identity environments by separating synchronization, authentication, authorization, and provisioning into individual investigative stages. Throughout every scenario, I applied the same structured methodology:

Business Impact → Scope → Evidence → Root Cause → Validation → Documentation.

This engineering approach provides a consistent framework for troubleshooting Hybrid Identity environments in enterprise organizations.
