# Week 4: requirements validation and prototyping

## Class focus

The Week 4 material connects research evidence to user stories, acceptance criteria and prototypes. The main point is that development should not begin from a vague feature idea. The team first needs a clear user story, observable completion conditions and a prototype that can test the important assumptions.

## Research and interview preparation notes

The lecture describes GenAI as a support tool during requirements elicitation, not as the owner of the research. It can help draft interview questions, summarise transcript notes, cluster themes and correct text. Human researchers remain responsible for:

- access to real users;
- observing real behaviour;
- domain judgement;
- ethics and evidence quality;
- validating themes against the original material;
- accepting or rejecting the final requirements.

Interview preparation should therefore begin with a clearly framed problem. Draft questions should be used to gather evidence that can validate, ground or constrain assumptions. AI-generated questions or themes remain provisional until checked by a person against the interview evidence.

### Interview-note workflow from the lecture

1. State the problem or assumption that the interview is intended to examine.
2. Draft questions that relate to user goals, context, data, constraints and error situations.
3. Record the user's evidence without replacing it with an AI interpretation.
4. Use AI only to create a first summary or theme grouping.
5. Compare the summary and themes with the original notes.
6. Retain human responsibility for the final insight and requirement.

## Requirements analysis notes

Acceptance criteria define when a user story is complete. Each criterion should have a clear pass/fail result and be measurable and testable. The criteria should cover functional and non-functional requirements.

Good acceptance criteria should be:

- written before development;
- achievable and not unnecessarily narrow;
- measurable without being too broad;
- expressed without unnecessary technical implementation details;
- agreed collaboratively;
- simple and concise;
- written in an active, user-centred voice;
- able to reveal negative, error and edge scenarios.

### Behaviour-driven format

- **Given**: the context or initial condition;
- **And**: additional context when required;
- **When**: the event or user action;
- **Then**: the observable outcome;
- **And**: another required outcome.

If a behaviour does not fit naturally into Given/When/Then, rule-oriented acceptance criteria can describe the system rules instead.

Acceptance criteria establish the boundary of a story, create a common language for the team and stakeholders, and provide a testing skeleton. Dependencies and relevant UX artefacts should also be linked to the story.

## Prototyping notes

A prototype is a simulation used for early testing of whether a design supports user goals. It should be grounded in product objectives, user research, scenarios, journey maps, problem statements, user stories and acceptance criteria.

- A horizontal prototype covers many functions at limited depth.
- A vertical prototype examines a smaller number of functions in greater depth.
- Low-fidelity prototypes are fast, collaborative and useful for checking terminology, flows and key interactions.
- High-fidelity prototypes are more realistic but cost more time and can create information overload if introduced too early.
- Fidelity includes visual, functional and content fidelity.
- Prototyping is iterative: define the vision, focus on key features, test and refine.

The prototype is an interim test artefact, not proof that a final production system is complete.

## Weekly record template

| Item | Note to record |
| --- | --- |
| Research question | What assumption or user goal is being examined? |
| Interview preparation | Which draft questions need human review? |
| Evidence | What was directly observed or stated? |
| Theme | What pattern appears after checking the original notes? |
| User story | Which role, goal and value are supported? |
| Acceptance criteria | What measurable Given/When/Then or rule conditions apply? |
| Functional requirement | What behaviour must occur? |
| Non-functional requirement | What quality, performance, accessibility or security condition applies? |
| Prototype implication | Which flow or state should be represented and tested? |