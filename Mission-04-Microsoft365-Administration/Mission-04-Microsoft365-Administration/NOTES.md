# Mission 4 – Microsoft 365 Administration

## Introduction

Mission 4 focused on developing the mindset of a Microsoft 365 Administrator by solving realistic administrative and operational scenarios. Rather than learning where buttons are located in the Microsoft 365 Admin Center, this mission emphasized structured troubleshooting, evidence-based decision making, and understanding the relationship between Microsoft Entra ID, Microsoft 365 services, Exchange Online, Teams, SharePoint, and licensing.

A recurring lesson throughout the mission was that successful authentication does not always mean a user has access to every Microsoft 365 service. Administrators must determine whether an issue relates to authentication, licensing, provisioning, authorization, or service configuration before making changes.

---

## Microsoft 365 Troubleshooting Methodology

Every scenario throughout this mission followed the same engineering process.

1. Determine the business impact.
2. Identify whether the issue affects a single user or multiple users.
3. Eliminate services that are functioning correctly.
4. Identify the affected Microsoft 365 workload.
5. Verify configuration and permissions.
6. Compare the affected user with a known working user.
7. Review recent administrative changes.
8. Gather evidence before making changes.
9. Validate the resolution.
10. Document the incident.

This methodology prevents unnecessary configuration changes and helps identify the root cause more efficiently.

---

## Authentication versus Authorization

One of the most important lessons reinforced during this mission was separating authentication from authorization.

Authentication confirms the identity of the user. If the user can successfully sign in to Microsoft 365, authentication through Microsoft Entra ID has already succeeded.

Authorization determines what the authenticated user is allowed to access. Many Microsoft 365 issues are authorization problems rather than authentication problems. Understanding this distinction allows administrators to focus their investigation on the correct workload instead of repeatedly troubleshooting sign-in issues.

---

## Microsoft 365 Licensing

Licensing directly controls which Microsoft 365 workloads are available to a user.

When troubleshooting licensing issues, an administrator should verify:

- The correct Microsoft 365 license is assigned.
- Required service plans such as Exchange Online or Microsoft Teams are enabled.
- Group-based licensing has completed successfully.
- License provisioning has completed.
- Recent license changes appear in audit logs.

A user may successfully authenticate while still lacking access to Microsoft 365 workloads if licensing or provisioning is incomplete.

---

## Exchange Online Administration

Exchange Online scenarios demonstrated the importance of distinguishing mailbox availability from mailbox permissions.

Areas to verify include:

- Mailbox provisioning
- Shared mailbox permissions
- Full Access
- Send As
- Send on Behalf
- Calendar permissions
- Outlook synchronization

A mailbox existing does not automatically mean a user has permission to access it.

---

## Microsoft Teams Administration

A Microsoft Teams issue should first be classified before troubleshooting.

Possible categories include:

- Authentication
- Licensing
- Team membership
- Microsoft 365 Group membership
- Teams policy
- Client synchronization

One lesson learned was not to confuse Team membership with Teams meetings. A user unable to see a Team is usually experiencing a membership or authorization issue rather than a meeting configuration problem.

---

## SharePoint Online Administration

SharePoint access problems often relate to authorization rather than authentication.

Areas to investigate include:

- Site permissions
- Microsoft 365 Group membership
- Security Group membership
- Permission inheritance
- Sharing configuration
- Identity Governance approval processes
- Provisioning delays

The administrator should verify how permissions are intended to be assigned before making changes.

---

## User Lifecycle Management

Several scenarios demonstrated the importance of user lifecycle management.

Administrative activities include:

- User onboarding
- Department transfers
- License reassignment
- Group membership changes
- Offboarding
- Enterprise Application provisioning

Many incidents occur immediately after administrative changes, making it essential to ask:

**"What changed before the issue started?"**

This question became one of the most valuable troubleshooting habits developed during Mission 4.

---

## Audit Logs

Audit logs should be reviewed whenever unexpected administrative changes are suspected.

Examples include:

- License assignment changes
- Group membership changes
- Exchange permission changes
- Microsoft Teams membership changes
- SharePoint permission changes

Audit logs provide evidence rather than assumptions during troubleshooting.

---

## Baseline Comparison

One of the strongest troubleshooting techniques developed during this mission was comparing an affected user with a known working user.

Comparison areas include:

- License assignment
- Group membership
- Exchange permissions
- Teams membership
- SharePoint permissions
- Provisioning status

This approach quickly identifies configuration differences and reduces unnecessary troubleshooting.

---

## Engineering Mindset

Mission 4 reinforced several engineering principles that guided every investigation.

Always determine the scope before troubleshooting.

Always identify what changed.

Always eliminate healthy services before investigating the affected workload.

Always gather evidence before making changes.

Always validate the resolution before closing the incident.

This structured approach improves troubleshooting efficiency, reduces risk, and demonstrates professionalism during both real-world administration and technical interviews.
