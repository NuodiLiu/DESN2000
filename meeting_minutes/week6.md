1. Solution Ideation
use different ideation **technical** to show how to generate different **solution ideas**
solution ideas e.g.: verified listing platform, housemate compatibility matcher, co-living agreement + chores/bills tracker, safe guided messaging

2. Systematic concept selection (use Decition Metric):
suggested:
| Criteria                              |   Weight | Concept A: Trust Flow | Concept B: Compatibility Matching | Concept C: Co-Living Agreement |
| ------------------------------------- | -------: | --------------------: | --------------------------------: | -----------------------------: |
| Research evidence fit                 |      30% |                     5 |                                 5 |                              4 |
| User value / risk reduction           |      20% |                     5 |                                 4 |                              4 |
| Feasibility in 10-week prototype      |      20% |                     3 |                                 4 |                              5 |
| Prototype testability                 |      15% |                     4 |                                 5 |                              5 |
| Innovation beyond existing tools      |      10% |                     3 |                                 4 |                              4 |
| Accessibility / privacy manageability |       5% |                     3 |                                 4 |                              4 |
| **Weighted score**                    | **100%** |          **4.15 / 5** |                      **4.45 / 5** |                   **4.35 / 5** |

Tecnical problem selection Example:
Three technical concepts were generated from the research findings:
Concept A: Verified Accommodation & Housemate Trust Flow, focused on reducing scam and unsafe contact risk;
Concept B: Lifestyle Compatibility Matching & Comparison, focused on helping students compare daily habits before commitment;
Concept C: Pre-Move-In Co-Living Agreement & Responsibility Tracker, focused on making chores, bills, privacy and house rules explicit before conflict occurs.

A weighted decision matrix was used to rank the concepts based on research evidence fit, user value, feasibility, prototype testability, innovation and privacy/accessibility manageability. Concept B scored highest, but the selected design combines Concept B as the core flow with lightweight trust indicators from Concept A and a basic agreement setup from Concept C.

3. Subsystem analyze
a breakdown for the main technical problem.
E.g.: profile data structure, verification status logic, compatibility scoring, guided chat prompts, co-living agreement creation, notification/reminder logic, privacy controls

Also need to show how they link to each other, use a **diagram**

4. double check Epics @pranav
at least 2 epics, each has **user story**.
use standar format like: As a [user], I want [goal], so that [value]
check if related to **our problem solution**
user story has very strong acceptance criteria 
    -> use Given/When/Then acceptance criteria format
    -> shows success paths, error paths, and edge cases. For example, the verification flow needs to clearly state what trust signal the user sees and under what conditions the user cannot continue submitting.
    -> answers "whether it can be used as a testing skeleton" and "whether it is measurable and testable"
add **functional requirements** for each epic/story
add **non functional requirements** for each epic/story

5. Jira needs to link to Figma prototype

6. Dependency table for user story, shows which usecase(functionality) depends on which.

7. Story Map
Example:

| User Activity / User Stage | Profile Setup | Browse & Shortlist | Compare Compatibility | Safe Contact | Co-living Agreement |
| --- | --- | --- | --- | --- | --- |
| User task | Create personal/housemate profile | View listing or housemate profile | Compare whether living habits fit | Send safe messages | Confirm pre-move-in rules |
| Sprint 1 / MVP stories | As a student, I want to create a basic lifestyle profile so that others can understand my living habits. | As a student, I want to view verified profile/listing indicators so that I can judge whether an option is trustworthy. | As a student, I want to compare cleanliness, noise, guests, schedule and chores preferences so that I can identify lifestyle fit. | As a student, I want to send a guided message in-app so that I do not need to share personal contact details too early. | As a student, I want to generate a basic co-living expectation checklist so that bills, chores and boundaries are discussed before commitment. |
| Later Sprint stories | Add optional accessibility/language preferences | Save favourite listings/housemates | Show compatibility score explanation | Message templates based on mismatch areas | Convert agreement into chore/bill reminders |
| Backlog / nice-to-have | Full identity verification | Review system | AI-generated match recommendations | Report suspicious users | Full household dashboard |

8. low-fidelity Figma clickable prototype for Spritn 1

9. Week 3–7 technical development evolution
shows how our concept choice change over time (make up something)

10. what is our innovation comparing to existing system

11. prototype test plan: test goal, target user, task scenario, success criteria, expected errors, what data to collect
