# Mission 4 – Microsoft 365 Administration

## Lab Objective

Develop a structured Microsoft 365 administration troubleshooting methodology by investigating realistic enterprise support scenarios involving Microsoft Entra ID, Microsoft 365 licensing, Exchange Online, Microsoft Teams, SharePoint Online, and user lifecycle management.

Rather than memorizing portal navigation, every exercise focused on identifying business impact, narrowing the scope, gathering evidence, determining the root cause, and validating the resolution.

---

# Scenario 1 – New Employee Onboarding

## Situation

HR requested onboarding for five new employees before their first day.

Required services included:

- Microsoft 365
- Exchange Online
- Microsoft Teams
- OneDrive
- SharePoint
- Salesforce
- Multi-Factor Authentication

## Investigation

The onboarding process began by validating the information provided by HR, including the employee's department, job title, reporting manager, and required applications. User accounts were then created and assigned to the appropriate security or Microsoft 365 groups based on role.

Microsoft 365 licenses were assigned to provision Exchange Online, Teams, SharePoint, and OneDrive. Enterprise Application assignments were reviewed to ensure access to applications such as Salesforce. Provisioning was validated before enabling Multi-Factor Authentication and confirming that all required services were available.

## Lesson Learned

Successful onboarding requires more than account creation. Identity, licensing, provisioning, application assignments, and security controls must all be verified before handing the account to the user.

---

# Scenario 2 – Microsoft Teams Licensing

## Situation

A newly onboarded employee could sign in to Microsoft 365 and Outlook but received the message:

"You're not licensed for Microsoft Teams."

## Investigation

Authentication was immediately eliminated because the user successfully signed in to Microsoft 365. The investigation focused on Microsoft 365 licensing by verifying the assigned license, confirming that the Teams service plan was enabled, reviewing group-based licensing, and checking whether provisioning had completed successfully. The affected user was compared with a known working account to identify configuration differences.

## Lesson Learned

Authentication and licensing are separate components. A user may authenticate successfully while still lacking access to individual Microsoft 365 workloads.

---

# Scenario 3 – Exchange Online Mailbox

## Situation

A newly created user could open Outlook but all outgoing email remained in the Outbox.

## Investigation

Because Teams and OneDrive were functioning normally, Microsoft Entra authentication and general connectivity were eliminated. The investigation shifted to Exchange Online by verifying mailbox provisioning, Exchange licensing, Outlook synchronization, and mailbox status. Internal send and receive testing was used to determine whether the issue affected sending, receiving, or both.

## Lesson Learned

When only Exchange Online is affected, troubleshooting should remain focused on Exchange rather than unrelated Microsoft 365 services.

---

# Scenario 4 – SharePoint Online Access

## Situation

A newly hired employee received an "Access Denied" message when opening a SharePoint site while all other users accessed it successfully.

## Investigation

The issue was classified as an isolated authorization problem. Site permissions, Microsoft 365 Group membership, Security Group membership, sharing configuration, permission inheritance, and provisioning were reviewed. Identity Governance or approval workflows were also considered where applicable.

## Lesson Learned

SharePoint issues frequently relate to authorization rather than authentication. Administrators should understand how permissions are assigned before modifying access.

---

# Scenario 5 – Shared Mailbox Access

## Situation

One employee could no longer access a shared mailbox while the remainder of the department continued working normally.

## Investigation

The investigation focused on Exchange Online permissions by reviewing Full Access, Send As, Send on Behalf, mailbox delegation, group membership, and recent administrative changes recorded in audit logs. Configuration was compared with another employee who retained access.

## Lesson Learned

Always verify mailbox permissions before assuming a mailbox or Microsoft 365 service has failed.

---

# Scenario 6 – Microsoft Teams Membership

## Situation

A newly hired employee could successfully open Microsoft Teams but was unable to access the Sales Team.

## Investigation

Authentication and licensing were eliminated because Teams loaded successfully. Team membership, Microsoft 365 Group membership, dynamic membership rules, provisioning, and synchronization were reviewed to determine why the user had not been added to the Sales Team.

## Lesson Learned

Membership within a Microsoft Team differs from joining a Teams meeting. Team visibility is generally controlled through Microsoft 365 Groups and membership assignments.

---

# Scenario 7 – Department Transfer

## Situation

Following a department transfer, a user retained access to Microsoft 365 but immediately lost Exchange Online and Microsoft Teams.

## Investigation

The investigation focused on identifying what changed. Microsoft 365 licensing, group-based licensing, audit logs, provisioning status, and department-based automation were reviewed to determine whether the user had been removed from the appropriate licensing group during the transfer process.

## Lesson Learned

Many Microsoft 365 incidents begin immediately after administrative changes. Understanding what changed often leads directly to the root cause.

---

# Scenario 8 – Executive Calendar Access

## Situation

The CEO's assistant successfully accessed Microsoft 365 but could not open the CEO's shared calendar.

## Investigation

Authentication and licensing were eliminated. Calendar delegation, Exchange Online permissions, audit logs, mailbox delegation, and permission propagation were reviewed before validating whether the assigned permissions matched business requirements.

## Lesson Learned

Successful authentication does not guarantee authorization. Exchange Online permissions determine whether users can access delegated mailboxes and calendars.

---

# Overall Lab Reflection

Throughout Mission 4, every scenario reinforced the importance of structured troubleshooting rather than immediately changing settings. Each investigation followed the same engineering methodology:

Determine the business impact.

Identify the scope.

Eliminate healthy services.

Identify the affected Microsoft 365 workload.

Gather evidence.

Determine the root cause.

Validate the resolution.

Document the findings.

This methodology became the foundation for approaching Microsoft 365 administration and will continue to be applied throughout future missions involving Microsoft Entra ID, Azure, and Hybrid Identity.
