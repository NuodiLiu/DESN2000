# Prototype Test Plan

Each test maps to Sprint 1 user stories (US IDs from `userstories.md`) and to specific acceptance criteria (AC IDs from the group report Section 6 / Jira tickets), so a passed test is direct evidence that the corresponding criteria hold in the prototype. Method: moderated usability test on the low-fidelity clickable HTML prototype, 5 participants per test, think-aloud protocol. Each task scenario starts from the prototype screen recorded in the prototype-to-user-story traceability table.

## Test Overview

| Test | Goal | Stories | Acceptance criteria | Responsible |
|---|---|---|---|---|
| T1 | Lifestyle preference profile setup | US-12 | AC-US12-04, AC-US12-05 | Pranav |
| T2 | Verification trust signals on listings and profiles | US-11, US-13 | AC-US11-02, AC-US11-03, AC-US13-03 | Nicky |
| T3 | Compatibility comparison and match choice | US-12 | AC-US12-01, AC-US12-02, AC-US12-06 | Liam |
| T4 | Guided safe first contact | US-09 | AC-US09-01, AC-US09-04, AC-US09-06 | Dylan |
| T5 | House rule proposal and acknowledgement | US-10, US-02 | AC-US10-01, AC-US10-02, AC-US10-04, AC-US02-01 | Liam |

## Test Details

| # | Test Goal | Stories | ACs | Target User | Task Scenario | Success Criteria | Expected Errors | Data to Collect | Responsible |
|---|-----------|---------|-----|-------------|---------------|------------------|-----------------|-----------------|-------------|
| T1 | Verify users can complete the lifestyle preference profile without guidance | US-12 | AC-US12-04, AC-US12-05 | Student new to shared housing | "You just signed up. Set up your lifestyle preferences (cleanliness, sleep schedule, noise, guests, smoking)." | ≥4/5 users complete the profile in ≤3 min with no facilitator help; all required fields filled; an incomplete submission triggers the completion prompt (AC-US12-04); contradictory selections trigger the conflict flag (AC-US12-05) | Users skip required fields thinking they are optional; users cannot find where profile setup starts; unclear field labels | Task completion rate; time on task; fields left blank; points where users ask for help | Pranav |
| T2 | Verify users can find a listing's key details and correctly read the verification status | US-11, US-13 | AC-US11-02, AC-US11-03, AC-US13-03 | Student searching for a room | "Find a room under $350/week, check whether the listing and the profile behind it are verified, and open the property details." | ≥4/5 users correctly state the verification status; key details (rent, fees, location, photos) found in ≤2 min; verified-only filter or badge identified (AC-US11-02); unverified warning noticed and explained (AC-US11-03); affordability details located (AC-US13-03) | Users miss the verification badge; users confuse listing verification with profile verification; users cannot explain what "verified" means | Verification status identification accuracy; time to locate details; user's stated meaning of the badge | Nicky |
| T3 | Verify users can compare housemate compatibility and identify the better match | US-12 | AC-US12-01, AC-US12-02, AC-US12-06 | Student choosing between candidate housemates | "Compare two housemate profiles against your own preferences and pick the better match. Explain your choice." | ≥4/5 users pick the higher-compatibility profile and cite at least one specific mismatch from the compatibility summary (AC-US12-02); users correctly interpret the ranked results (AC-US12-01); when a zero-result filter is applied, users notice the broadening suggestion (AC-US12-06) | Users misread the comparison layout; users judge by photo instead of preference data; comparison entry point not found | Match selection accuracy; reasons given for choice; misclick count on comparison screen | Liam |
| T4 | Verify users can send a guided first message without sharing personal contact details | US-09 | AC-US09-01, AC-US09-04, AC-US09-06 | International student making first contact | "You want to ask about this listing. Send a first message using the app." | ≥4/5 users send a message using at least one guided prompt in ≤2 min with no contact details visible to either party (AC-US09-01); 0 users successfully type personal contact details without seeing the warning (AC-US09-04); users understand the unverified sender warning (AC-US09-06) | Users ignore prompts and write free text; users look for a phone number instead of in-app chat; prompt wording unclear to non-native speakers | Prompt usage rate; task completion rate; whether users attempt to share contact details; comprehension issues noted in think-aloud | Dylan |
| T5 | Verify users can propose a house rule and reach an acknowledged agreement | US-10, US-02 | AC-US10-01, AC-US10-02, AC-US10-04, AC-US02-01 | Student moving in with new housemates | "Propose a house rule about quiet hours, have your housemates acknowledge it, then find it in the household rules list." | ≥4/5 users propose a rule with title, description and category so that housemates are notified (AC-US10-01) and reach the acknowledged state in ≤3 min (AC-US10-02); a submission with missing fields triggers the completion prompt (AC-US10-04); the active rule is then found in the rules list (AC-US02-01) | Users cannot find the proposal entry point; users confuse a proposed rule with an active rule; users miss the acknowledgement step | Task completion rate; time on task; drop-offs at the acknowledgement step; comprehension notes from think-aloud | Liam |

## After Testing

- Compile results in one summary: completion rates, common errors, quotes from think-aloud.
- Rank issues by severity (blocks task > causes confusion > cosmetic) and feed into the next prototype iteration.
- Record which AC IDs failed, so the retest after iteration targets exactly those criteria.
