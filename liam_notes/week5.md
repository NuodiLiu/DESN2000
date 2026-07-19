# Week 5: turning research evidence into UX requirements

## Class focus

The Week 5 material places the work within an iterative process: empathise, define, ideate, prototype and test. User research, desk research, personas, scenarios and journey maps inform the problem definition. Themes from that evidence are then organised into initiatives, goals and features, which become epics, user stories and acceptance criteria.

## Research analysis notes

The lecture presents the following evidence chain:

1. **Research observation**: record what the evidence shows.
2. **Insight**: explain the underlying user problem or uncertainty.
3. **Requirement**: state what the system must enable or support.
4. **User story**: connect a role and goal to user value.
5. **Design implication**: identify what information, interaction or state the interface must expose.

The interface should not be justified by personal taste. A design decision should be traceable to evidence and an identified user need.

### Lecture example

The slides use scattered campus-event information as an example:

- **Observation**: new students miss events because information is spread across several channels.
- **Insight**: the underlying problem is poor discoverability and uncertainty about whether an event is suitable.
- **Requirement**: students need to discover events through relevant filters.
- **Design implication**: the interface should expose information such as location, time, cost, accessibility and commitment before registration.

This example demonstrates the analysis method; it is not project research evidence.

## Interview-note analysis

When analysing interview notes, the original observation should remain separate from the later interpretation. A participant statement should not be converted directly into a feature request. It should first be grouped with related evidence, interpreted as an insight and then assessed as a possible requirement.

Suggested analysis fields:

| Field | Purpose |
| --- | --- |
| Original observation | Preserve what was actually recorded. |
| Theme | Group related evidence without deleting differences. |
| Insight | Explain the user goal, difficulty or uncertainty. |
| Requirement | State the needed system capability. |
| User story | Identify role, goal and value. |
| Interaction consequence | Identify the screen state, feedback or recovery path implied by the requirement. |
| Validation needed | Record what still requires testing with users. |

## Acceptance criteria as a UX contract

The slides describe acceptance criteria as observable behaviours that users should experience. They should cover the normal path and the less visible but important states:

- loading;
- empty results;
- errors;
- confirmation;
- recovery.

Each acceptance criterion can imply a visible state and supporting microcopy. Functional criteria describe what the system does. Non-functional criteria add qualities such as response time, accessibility and reliability.

## UX requirement checks

Requirements and designs should support:

- an interface that is easy to explore and understand;
- clear, predictable navigation;
- user control and freedom, including an obvious exit or recovery path;
- consistency;
- a match between the system and the real world;
- visible feedback;
- aesthetic and minimalist design;
- recognition rather than recall;
- error prevention, diagnosis and recovery;
- help and documentation;
- accessibility.

Common design patterns can support familiar interactions, but dark patterns should be avoided because they mislead users or act against their interests.

## Weekly record template

| Evidence | Theme | Insight | Requirement | User story | Acceptance criteria / state | Validation |
| --- | --- | --- | --- | --- | --- | --- |
| Direct observation or research note | Evidence grouping | User problem or uncertainty | Required capability | Role, goal and value | Normal, loading, empty, error, confirmation and recovery behaviour | What must still be tested? |