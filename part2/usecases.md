# Use Cases

Each user story has a stable `US-xx` ID. Each goal-level use case has a stable `UC-xx` ID. Scope is stored in a separate column so that changing a sprint or priority does not change the ID.

## User Story–Use Case Mapping

| User Story ID | Use Case ID | Use Case | Primary Actor | Successful Outcome | Scope |
|---|---|---|---|---|---|
| US-01 | UC-01 | Browse and view property listings | Student / accommodation seeker | The user can review the details of a published property. | MVP |
| US-02 | UC-02 | Check verification status | Student / accommodation seeker | The user can see the verification status of a listing, landlord, or housemate. | MVP |
| US-03 | UC-03 | Create and update a lifestyle profile | Student / housemate | The user's shared-living preferences are stored in a structured profile. | MVP |
| US-04 | UC-04 | Find and compare housemate compatibility | Student / housemate | The user can discover candidate profiles and compare relevant living preferences. | MVP |
| US-05 | UC-05 | Access rental and language guidance | International student | The user can read rental guidance in plain language and a selected language. | MVP |
| US-06 | UC-06 | Send in-app messages | Student / housemate | The user can contact a landlord or housemate without sharing personal contact details. | MVP |
| US-07 | UC-07 | Use guided message prompts | Student / housemate | The user can add a relevant guided question to an in-app conversation. | MVP |
| US-08 | UC-08 | Request and confirm a property inspection | Student / accommodation seeker | The user and property manager confirm an available video or in-person inspection time. | MVP |
| US-09 | UC-09 | Create, review, and confirm a co-living agreement | Future housemates | All invited participants can review and accept the shared-living expectations. | MVP |
| US-10 | UC-10 | Save and compare options | Student | The user can review saved listings and housemate matches in one place. | Extension |
| US-11 | UC-11 | Report suspicious activity | Any user | A report is recorded with the related listing, profile, or conversation. | Extension |
| US-12 | UC-12 | Manage household chores | Shared-house resident | Household members can assign, rotate, and track chores. | Extension |
| US-13 | UC-13 | Manage shared expenses | Shared-house resident | Household members can record costs, shares, due dates, and payment status. | Extension |
| US-14 | UC-14 | Raise an anonymous household issue | Shared-house resident | The issue is shared with the household without showing the reporter's name to other residents. | Extension |
| US-15 | UC-15 | Create and manage a property listing | Property manager | A complete property listing is saved and can be published. | Secondary |
| US-16 | UC-16 | Complete and submit a rental application | Student applicant | A complete application is linked to the selected property and submitted for review. | Secondary |
| US-17 | UC-17 | Review rental applications | Property manager | The property manager can inspect application details and record a review decision. | Secondary |
| US-18 | UC-18 | Manage property enquiries | Property manager | The property manager can view and answer listing-related enquiries in one place. | Secondary |
| US-19 | UC-19 | Send tenant announcements | Property manager | An announcement is delivered to the current tenants of a property. | Secondary |
| US-20 | UC-20 | Match applicants to properties | Property manager | Submitted applicants can be compared with the property's requirements. | Secondary |
| US-21 | UC-21 | Track rent and send reminders | Property manager | Rent status is recorded and overdue tenants can receive reminders. | Secondary |

## Supporting Use Cases

Supporting use cases enable several user goals and therefore do not map to one primary user story.

| Supporting ID | Supporting Use Case | Primary Actor | Successful Outcome |
|---|---|---|---|
| SUP-01 | Manage account and role access | Any registered user | The user is authenticated and receives the correct student, resident, or property-manager permissions. |
| SUP-02 | Establish active household or tenancy membership | Resident / property manager / selected tenant | Membership is activated only after a household invitation or tenancy is confirmed. |
| SUP-03 | Deliver push notifications | System | Inspection confirmations, chore reminders, payment reminders, and announcements can reach users outside the active app. |
| SUP-04 | Manage verification evidence and status | User / property manager / system | Evidence is stored and the related listing or profile receives a pending, verified, or rejected status. |

## Supporting Prototype Data

| Data ID | Data Source | Purpose |
|---|---|---|
| DATA-01 | Seeded property listings | Provides published sample listings when the MVP prototype does not implement the secondary property-listing workflow. |

## Mapping Decisions

- `UC-04` includes discovering candidate housemate profiles because messaging, saving, verification, and reporting need a selected housemate context.
- `UC-08` includes inspection availability and property-manager confirmation; selecting a time does not confirm a booking by itself.
- `UC-09` includes inviting participants, reviewing the agreement, and recording acceptance; one user cannot confirm an agreement for everyone.
- `UC-16` collects the required applicant details. A lifestyle profile may prefill preferences, but it does not replace identity, contact, or rental-history information.
- `SUP-02` requires a confirmed tenancy or accepted household invitation. A match produced by `UC-20` does not grant household or tenant access by itself.
