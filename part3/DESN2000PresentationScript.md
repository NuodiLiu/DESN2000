# RoomMate Haven — DESN2000 Design Presentation Script

Target duration: approximately **9 minutes 10 seconds**, leaving a buffer below the 10-minute limit.

## Slide 1 — RoomMate Haven

**Speaker: Liam — 15 seconds**

Good morning. We are presenting RoomMate Haven, a student-focused shared-housing platform. Our goal is to help students choose the room, understand the people, and agree how to live before they make a commitment.

**Transition:** To understand why this matters, we need to look at the decision students actually face.

## Slide 2 — A good room can still become the wrong home

**Speaker: Liam — 35 seconds**

When students search for shared housing, they are making more than a property decision. They must decide whether a listing is genuine, whether a potential housemate is compatible, and whether shared expectations around bills, chores, guests and privacy will be respected.

This creates our design question: how might we help students choose a safe, trustworthy and compatible shared-living arrangement before they move in?

**Transition:** Our primary research shows that this is not an isolated concern.

## Slide 3 — Trust and compatibility shape the housing decision

**Speaker: Liam — 35 seconds**

We surveyed 16 international students currently studying in Australia. Every respondent reported some concern about rental scams. Housemate compatibility received an average importance rating of 4.44 out of 5, and 68.75 percent had experienced housemate conflict.

These findings show that the design must address trust before contact and conflict before move-in.

**Transition:** Existing platforms solve parts of this problem, but not the connected journey.

## Slide 4 — Existing tools solve stages, not the whole journey

**Speaker: Nicky — 35 seconds**

Property portals provide detailed listings and inspections, but they focus mainly on the property. Social groups offer reach and informal contact, but verification can be weak. Housemate platforms provide profiles, while household apps manage bills and chores after people have already moved in.

The opportunity is to connect trust, preference-based fit and shared expectations before commitment.

**Transition:** We generated three concepts to close this gap and selected them systematically.

## Slide 5 — Compatibility leads; trust and agreement complete it

**Speaker: Nicky — 45 seconds**

We compared three concepts using a weighted decision matrix based on research fit, user value, feasibility, testability, innovation and privacy.

The trust-flow concept scored 4.15 out of 5. Compatibility matching scored the highest at 4.45, while the co-living agreement concept scored 4.35.

We therefore selected compatibility matching as the core, then added lightweight trust indicators and an early agreement feature. This produced one focused and testable product journey rather than three disconnected products.

**Transition:** The selected direction becomes a five-step decision journey.

## Slide 6 — Five connected decisions reduce risk

**Speaker: Nicky — 45 seconds**

The user first finds a suitable home, then checks verification indicators for the property and people. Next, they compare lifestyle preferences, communicate safely through guided messages, and agree on shared expectations before commitment.

An important design principle is that trust and fit are different signals. Verification reduces uncertainty, while a compatibility score supports conversation. It is not a guarantee of identity or safety.

**Transition:** We will now demonstrate this connected journey in the deployed prototype.

## Slide 7 — Recorded prototype demonstration

**Speaker: Dylan — 75 seconds**

We developed an interactive HTML prototype and deployed it online, so it can be tested directly in a web browser.

In the recording, the user begins by searching for a property and checking verification cues. They then open a potential housemate profile and review the compatibility explanation. The interface shows preference-based matches and areas that should be discussed.

The user can continue through guided in-app messaging without sharing personal contact details too early. Finally, the user reviews a proposed house rule and its approval state before moving in.

This demonstrates that the Sprint journey is connected, interactive and testable rather than being only a set of static screens.

**Transition:** Behind this journey are modular subsystems that can be validated separately.

## Slide 8 — Connected subsystems make the concept feasible

**Speaker: Dylan — 50 seconds**

The interface connects profile data, the compatibility engine, guided messaging and the agreement builder. Verification supports profile and listing trust, while privacy controls manage consent, warnings and blocked contact details.

This modular structure allows each part to be developed and tested independently. During iteration, the most important technical issues were search recovery, the meaning of the compatibility score, and clear status feedback.

**Transition:** We therefore tested whether users understood these system states, not only whether they could click through the flow.

## Slide 9 — Trust cues worked, but meaning gaps remained

**Speaker: Dylan — 55 seconds**

The final usability testing involved five participants across two iterations using tablet, laptop and mobile devices.

Verification cues were the strongest result: five out of five participants completed the task independently without assistance. However, compatibility meaning remained partial. Only two out of five correctly explained that the score came from preferences without treating it as evidence of safety.

Rule activation also remained unclear, so acceptance criterion AC-US10-02 failed. In contrast, the contact-detail warning improved from fail to pass after the second iteration.

**Transition:** The detailed results show where the redesign worked and where more development is still required.

## Slide 10 — Two iterations produced measurable changes

**Speaker: Dylan — 60 seconds**

For search recovery, four out of five participants completed the targeted task independently, with a median time of 44 seconds. Verification remained successful. Compatibility interpretation still fell below the required threshold, and the rule-activation condition remained unclear.

We also conducted a wider Playwright review, which recorded 18 independent findings: eight functional or test-infrastructure issues, nine accessibility issues, and one responsive-layout issue.

These results do not show that every part of the system is complete. They show which parts are supported by evidence and define the next priorities: explaining the limits of compatibility and clarifying rule activation.

**Transition:** These findings also clarify what is genuinely innovative about the final design.

## Slide 11 — RoomMate Haven connects a fragmented journey

**Speaker: Pranav — 50 seconds**

The innovation is not that every individual feature is completely new. The innovation is their integration and timing.

The current experience often requires students to search on one platform, communicate on another, share personal contact details, and resolve conflict after moving in.

RoomMate Haven connects verification, preference-based comparison, safe communication and early agreements in one journey before commitment.

**Transition:** This leads to the final value of the project.

## Slide 12 — Trust, fit and clarity

**Speaker: Pranav — 45 seconds**

Students should be able to choose not only where they live, but who they live with and how they will live together.

RoomMate Haven addresses this decision through three connected values: trust in the available information, fit between people’s living preferences, and clarity around shared expectations.

Our research defined the problem, our concept selection justified the direction, and our deployed prototype and final testing demonstrated both feasibility and remaining limitations.

Thank you. We welcome your questions.

## Demo setup and delivery checklist

- Insert one **60–75 second MP4** over the three browser frames on Slide 7.
- Set the video to **play automatically** in Slide Show mode.
- Keep the three existing frames as the visual backup if the video does not start.
- Use the embedded recording if classroom Wi-Fi or the deployed site is unavailable.
- Rehearse the full presentation to approximately **9:10–9:30**.
- Each speaker should practise the handover sentence into the next section.
