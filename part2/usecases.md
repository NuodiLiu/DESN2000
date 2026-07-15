# Use Cases

Each user story has a stable `US-xx` ID. Each goal-level use case has a stable `UC-xx` ID. Scope is stored in a separate column so that changing a sprint or priority does not change the ID.

## User Story–Use Case Mapping

| User Story ID | Use Case ID | Use Case | Primary Actor | Successful Outcome | Scope |
|---|---|---|---|---|---|
| US-01 | UC-01 | Set up and manage chore roster | Domestic student / shared-house resident | The user can create, assign and rotate chores among housemates and track completion history. | MVP |
| US-02 | UC-02 | View and manage household rules | International student / shared-house resident | The user can view all household rules and expectations in their preferred language in a single location. | MVP |
| US-03 | UC-03 | Propose and approve chore system | Domestic student | All housemates have reviewed and approved a structured chore system before it becomes active. | MVP |
| US-04 | UC-04 | Log and split shared expenses | Shared-house resident | The user can log a shared expense and the system automatically calculates and assigns each housemate's share. | MVP |
| US-05 | UC-05 | Track outstanding balances | International student / shared-house resident | The user can view a real-time summary of who owes what and mark balances as settled. | MVP |
| US-06 | UC-06 | Split utility bills | International student / shared-house resident | The user can input a utility bill and split it equally or by usage among selected housemates. | MVP |
| US-07 | UC-07 | Post and view household notices | Shared-house resident | The user can post a notice visible to all housemates on a dedicated noticeboard separate from general messaging. | MVP |
| US-08 | UC-08 | Raise anonymous household issues | Domestic student / shared-house resident | A household issue is posted to the shared space without revealing the submitter's identity if the anonymous option is selected. | MVP |
| US-09 | UC-09 | Send secure in-app messages | International student / shared-house resident | The user can send and receive messages without either party's personal contact details being visible. | MVP |
| US-10 | UC-10 | Set and view agreed house rules | Shared-house resident | All housemates have acknowledged a proposed house rule before it becomes active and can reference it during disputes. | MVP |
| US-11 | UC-11 | View verified housemate profiles | International student / accommodation seeker | The user can view verified profiles with identity badges and filter search results to show only verified profiles. | MVP |
| US-12 | UC-12 | Filter housemates by lifestyle preferences | Shared-house resident / accommodation seeker | The user can set lifestyle preference filters and view a compatibility score and summary for each potential housemate. | MVP |
| US-13 | UC-13 | Search and filter property listings | Domestic student / accommodation seeker | The user can search for listings by university proximity and apply filters for rent, distance, bedrooms and move-in date. | MVP |
| US-14 | UC-14 | Receive overdue chore and expense reminders | Shared-house resident | The user receives automatic in-app reminders when a chore or expense payment is overdue. | Extension |
| US-15 | UC-15 | Read and submit housemate reviews | Shared-house resident / accommodation seeker | The user can read reviews left by previous housemates and submit a review after a confirmed tenancy ends. | Extension |
| US-16 | UC-16 | Track rent and send reminders | Property manager | Rent status is recorded per tenant and overdue tenants receive automatic reminders. | Secondary |
| US-17 | UC-17 | Create and manage property listings | Property manager | A complete property listing is published and visible to students searching for accommodation. | Secondary |
| US-18 | UC-18 | Send tenant announcements | Property manager | An announcement is delivered to all tenants of a selected property with read receipt tracking. | Secondary |

## Supporting Use Cases

Supporting use cases enable several user goals and therefore do not map to one primary user story.

| Supporting ID | Supporting Use Case | Primary Actor | Successful Outcome |
|---|---|---|---|
| SUP-01 | Manage account and role access | Any registered user | The user is authenticated and receives the correct student, resident, or property-manager permissions. |
| SUP-02 | Establish active household or tenancy membership | Resident / property manager / selected tenant | Membership is activated only after a household invitation or tenancy is confirmed. |
| SUP-03 | Deliver push notifications | System | Chore reminders, expense reminders, announcement deliveries, and issue notifications can reach users outside the active app. |
| SUP-04 | Manage verification evidence and status | User / property manager / system | Evidence is stored and the related profile receives a pending, verified, or rejected status. |

## Supporting Prototype Data

| Data ID | Data Source | Purpose |
|---|---|---|
| DATA-01 | Seeded property listings | Provides published sample listings when the MVP prototype does not implement the secondary property-listing workflow. |
| DATA-02 | Seeded housemate profiles | Provides sample verified and unverified profiles for compatibility matching and verification testing in the MVP prototype. |

## Mapping Decisions

- `UC-03` requires `UC-01` to be completed first; a chore system cannot be activated without an existing roster structure.
- `UC-05` and `UC-06` depend on `UC-04`; balances and bill splitting require at least one logged expense to function.
- `UC-08` depends on `UC-10`; anonymous issues are more meaningful when house rules exist to reference during disputes.
- `UC-09` flags unverified users within the messaging interface, creating a dependency on `UC-11` for full functionality.
- `UC-12` requires `UC-11`; compatibility matching is only meaningful between verified profiles to ensure trust.
- `SUP-02` requires a confirmed tenancy or accepted household invitation. A match produced by `UC-12` does not grant household or tenant access by itself.
- `SUP-03` supports `UC-14`, `UC-16`, `UC-18` and all reminder-based user stories.
