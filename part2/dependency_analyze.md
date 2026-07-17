# Use Case Dependency Analysis

## Dependency Rules

- **Required** means the dependent use case cannot proceed without the prerequisite.
- **Required data** means the dependent use case needs data created or maintained by the prerequisite.
- **Context (OR)** means any one of the listed prerequisites is enough.
- **AND** means every listed prerequisite must be satisfied together.
- **Conditional** means the dependency applies only in a specific situation (e.g. showing a verified badge).
- **Extend / Optional** means the relationship adds support but is not required for the main success path.

## Dependency Table

| Dependent Use Case | Depends On | Type | Reason |
|---|---|---|---|
| UC-01 Set up and manage chore roster | SUP-02 Active household membership | Required | Only members of an active household can view or manage its chore roster. |
| UC-02 View and manage household rules | SUP-02 Active household membership | Required | Rules belong to a specific household; only members can view or manage them. |
| UC-02 View and manage household rules | UC-10 Set and view agreed house rules | Required data | Rules must be set and agreed before they can be displayed in a member's preferred language. |
| UC-03 Propose and approve chore system | UC-01 Chore roster | Required data | A structured chore system cannot be proposed or activated without an existing roster to build on. |
| UC-03 Propose and approve chore system | SUP-02 Active household membership | Required | All approving housemates must be identified members of the same household. |
| UC-04 Log and split shared expenses | SUP-02 Active household membership | Required | Expenses and each member's share must belong to an authorised household. |
| UC-05 Track outstanding balances | UC-04 Log and split shared expenses | Required data | Balances are computed from logged expenses; at least one expense must exist to show who owes what. |
| UC-06 Split utility bills | UC-04 Log and split shared expenses | Required (shared capability) | A utility bill is itself a shared expense; UC-06 reuses UC-04's logging and cost-splitting engine rather than any pre-existing expense data. |
| UC-07 Post and view household notices | SUP-02 Active household membership | Required | The noticeboard is scoped to a single household; only members can post or read notices. |
| UC-08 Raise anonymous household issues | SUP-02 Active household membership | Required | The issue must belong to the reporter's household while hiding their identity from other residents. |
| UC-08 Raise anonymous household issues | UC-10 Set and view agreed house rules | Optional data | Existing house rules give issues a shared reference point during disputes, but an issue can be raised without them. |
| UC-09 Send private in-app messages | SUP-01 Manage account and role access | Required | Messaging remains locked until the user signs in and completes phone verification. |
| UC-09 Send private in-app messages | UC-11 View verified housemate profiles | Extend / Optional | Private messaging works after sign-in and phone verification. UC-11 adds identity status without gating the messaging path. |
| UC-11 View verified housemate profiles | SUP-04 Verification evidence and status **OR** DATA-02 Seeded housemate profiles | Required data (OR) | A stored verified/pending/rejected status (or seeded sample profiles) must exist before a badge can be shown. |
| UC-12 Filter housemates by lifestyle preferences | UC-11 View verified housemate profiles | Extend / Optional | UC-11 adds identity status as trust context, but identity verification does not gate compatibility matching. |
| UC-13 Search and filter property listings | UC-17 Create and manage property listings **OR** DATA-01 Seeded property listings | Required data (OR) | At least one published listing (managed or seeded) must exist before a student can search it. |
| UC-14 Receive overdue chore and expense reminders | UC-01 Chore roster **OR** UC-04 Shared expenses | Required data (OR) | A reminder needs an overdue chore assignment or an overdue expense to reference. |
| UC-14 Receive overdue chore and expense reminders | SUP-03 Push notifications | Required | Automatic overdue reminders are delivered through the notification service. |
| UC-15 Read and submit housemate reviews | SUP-02 Active household or tenancy membership | Required | A review may only be submitted after a confirmed tenancy or shared-living arrangement has ended. |
| UC-16 Track rent and send reminders | SUP-02 Active tenancy membership | Required | Rent status needs a confirmed tenant-property relationship; selecting an applicant is not enough. |
| UC-16 Track rent and send reminders | SUP-03 Push notifications | Optional | Push notifications deliver due-date and overdue rent reminders outside the active app. |
| UC-17 Create and manage property listings | SUP-04 Verification evidence and status | Conditional | Verification is required only before a verified badge is shown; an unverified or pending listing may still be saved. |
| UC-18 Send tenant announcements | SUP-02 Active tenancy membership | Required | The system needs a confirmed current-tenant audience for the selected property. |
| UC-18 Send tenant announcements | SUP-03 Push notifications | Optional | Push notifications deliver the announcement outside the active app. |
