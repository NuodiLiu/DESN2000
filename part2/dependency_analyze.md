# Use Case Dependency Analysis

## Dependency Rules

- **Required** means the dependent use case cannot proceed without the prerequisite.
- **Data** means the dependent use case needs data created or maintained by the prerequisite.
- **Context (OR)** means any one of the listed contexts is enough.
- **Extend / Optional** means the relationship adds support but is not required for the main success path.

## Dependency Table

| Dependent Use Case | Depends On | Type | Reason |
|---|---|---|---|
| UC-01 Browse and view property listings | UC-15 Manage property listing **OR** DATA-01 Seeded property listings | Required data (OR) | At least one published listing must exist before a student can browse it. |
| UC-02 Check verification status | SUP-04 Verification evidence and status | Required data | The system needs a stored status before it can display pending, verified, or rejected. |
| UC-02 Check verification status | UC-01 listing context **OR** UC-04 housemate context | Required context (OR) | The user must select the listing, landlord, or housemate whose status will be checked. |
| UC-04 Find and compare housemate compatibility | UC-03 Lifestyle profiles | Required data | The system needs enough preference data for both users before it can compare them. |
| UC-06 Send in-app messages | UC-01 listing context **OR** UC-04 housemate context | Required context (OR) | A conversation needs a valid landlord, property, or housemate recipient. |
| UC-07 Use guided message prompts | UC-06 In-app messaging | Extend | Guided prompts are an optional action inside a conversation. |
| UC-08 Request and confirm a property inspection | UC-01 Property listing | Required | The request needs a selected property; `UC-08` also handles available times and property-manager confirmation. |
| UC-08 Request and confirm a property inspection | SUP-03 Push notifications | Optional | Push notifications deliver the confirmation, change, or reminder outside the active app. |
| UC-09 Create, review, and confirm a co-living agreement | SUP-01 access for two or more identified participants | Required | Every participant must be identified and must review or accept the agreement for themselves. |
| UC-09 Create, review, and confirm a co-living agreement | UC-03 profile, UC-04 comparison, or UC-06 conversation | Optional context / prefill | Profile data, comparison results, or a conversation may start or prefill an agreement, but none is mandatory. |
| UC-10 Save and compare options | UC-01 listing context **OR** UC-04 housemate context | Required context (OR) | The saved option must be a listing or housemate result. |
| UC-11 Report suspicious activity | UC-01 listing **OR** UC-04 housemate **OR** UC-06 conversation | Required context (OR) | A report must identify its target. |
| UC-12 Manage household chores | SUP-02 Active household membership | Required | Only authorised members of the household can view or change its chores. |
| UC-12 Manage household chores | UC-09 Co-living agreement | Optional data | Accepted chore expectations may prefill the chore setup. |
| UC-12 Manage household chores | SUP-03 Push notifications | Optional | Push notifications can remind residents about assigned or overdue chores. |
| UC-13 Manage shared expenses | SUP-02 Active household membership | Required | Expenses and payment status must belong to an authorised household. |
| UC-13 Manage shared expenses | UC-09 Co-living agreement | Optional data | Accepted bill rules may prefill expense settings. |
| UC-13 Manage shared expenses | SUP-03 Push notifications | Optional | Push notifications can remind residents about due or overdue payments. |
| UC-14 Raise an anonymous household issue | SUP-02 Active household membership | Required | The issue must belong to the reporter's household while hiding the reporter's name from other residents. |
| UC-15 Create and manage a property listing | SUP-04 Verification evidence and status | Conditional | Verification is required only before a verified badge is shown; an unverified or pending listing may still be saved unless a verified-only policy is adopted. |
| UC-16 Complete and submit a rental application | UC-15 Active property listing | Required data | The application must be linked to a property that accepts applications. |
| UC-16 Complete and submit a rental application | UC-03 Lifestyle profile | Optional data | Existing lifestyle preferences may prefill matching fields, but the application still collects its own identity, contact, and rental details. |
| UC-17 Review rental applications | UC-16 Submitted application | Required | The property manager needs a complete submitted application before recording a review. |
| UC-18 Manage property enquiries | UC-15 Property listing **AND** UC-06 Messaging | Required data / shared capability (AND) | A listing-related enquiry needs both a property context and the in-app messaging capability. |
| UC-19 Send tenant announcements | SUP-02 Active tenancy membership | Required | The system needs a confirmed current-tenant audience; selecting an applicant is not enough. |
| UC-19 Send tenant announcements | SUP-03 Push notifications | Optional | Push notifications deliver the announcement outside the active app. |
| UC-20 Match applicants to properties | UC-15 Active property listing **AND** UC-16 Submitted applications | Required data (AND) | Matching needs property requirements and submitted applicant data; application review remains a separate workflow. |
| UC-21 Track rent and send reminders | SUP-02 Active tenancy membership | Required | Rent tracking needs a confirmed tenant-property relationship. |
| UC-21 Track rent and send reminders | SUP-03 Push notifications | Optional | Push notifications deliver due-date and overdue reminders outside the active app. |

## Dependency Graph

```mermaid
flowchart TB
    subgraph SUPPORT[Supporting Use Cases]
        SUP02["SUP-02 Active household or tenancy membership"]
        SUP03["SUP-03 Push notifications"]
        SUP04["SUP-04 Verification evidence and status"]
        DATA01["DATA-01 Seeded property listings"]
    end

    subgraph PROPERTY[Property Application and Management - Secondary]
        UC15["UC-15 Manage property listing"]
        UC16["UC-16 Submit rental application"]
        UC17["UC-17 Review applications"]
        UC18["UC-18 Manage enquiries"]
        UC19["UC-19 Send announcements"]
        UC20["UC-20 Match applicants to properties"]
        UC21["UC-21 Track rent and reminders"]
        AND18{"AND: listing and messaging"}
        AND20{"AND: listing and submitted applications"}
    end

    subgraph MVP[MVP - Search, Trust, Compatibility, and Agreement]
        UC01["UC-01 Browse and view listings"]
        UC02["UC-02 Check verification"]
        UC03["UC-03 Manage lifestyle profile"]
        UC04["UC-04 Find and compare compatibility"]
        UC05["UC-05 Rental and language guidance"]
        UC06["UC-06 In-app messaging"]
        UC07["UC-07 Guided prompts"]
        UC08["UC-08 Request and confirm inspection"]
        UC09["UC-09 Confirm co-living agreement"]
        SELECTED{"OR: selected listing or housemate"}
        LISTSOURCE{"OR: managed or seeded listing data"}
    end

    subgraph EXTENSION[Potential Extensions]
        UC10["UC-10 Save and compare options"]
        UC11["UC-11 Report suspicious activity"]
        UC12["UC-12 Manage chores"]
        UC13["UC-13 Manage expenses"]
        UC14["UC-14 Raise anonymous issue"]
        REPORTCTX{"OR: listing, housemate, or conversation"}
    end

    SUP04 -. "verified status only" .-> UC15
    UC15 -- "managed listings" --> LISTSOURCE
    DATA01 -- "prototype listings" --> LISTSOURCE
    LISTSOURCE --> UC01
    SUP04 --> UC02

    UC03 -- "data for both users" --> UC04
    UC01 -- "listing" --> SELECTED
    UC04 -- "housemate" --> SELECTED
    SELECTED --> UC02
    SELECTED --> UC06
    SELECTED --> UC10

    UC06 -. "extend" .-> UC07
    UC01 --> UC08
    SUP03 -. "confirmation or reminder" .-> UC08

    UC03 -. "profile prefill" .-> UC09
    UC04 -. "comparison context" .-> UC09
    UC06 -. "conversation entry" .-> UC09

    UC01 -- "listing" --> REPORTCTX
    UC04 -- "housemate" --> REPORTCTX
    UC06 -- "conversation" --> REPORTCTX
    REPORTCTX --> UC11

    SUP02 --> UC12
    SUP02 --> UC13
    SUP02 --> UC14
    UC09 -. "prefill chore rules" .-> UC12
    UC09 -. "prefill bill rules" .-> UC13
    SUP03 -. "reminder" .-> UC12
    SUP03 -. "reminder" .-> UC13

    UC15 --> UC16
    UC03 -. "preference prefill" .-> UC16
    UC16 --> UC17
    UC15 --> AND18
    UC06 --> AND18
    AND18 --> UC18
    UC15 --> AND20
    UC16 --> AND20
    AND20 --> UC20

    SUP02 --> UC19
    SUP02 --> UC21
    SUP03 -. "delivery" .-> UC19
    SUP03 -. "reminder" .-> UC21
```