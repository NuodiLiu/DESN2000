# Participant-level findings and evidence

## Evidence scope

These seven findings were accepted for Section 3.3.3 of the report. The wording
below paraphrases the observation notes; it is not presented as a verbatim
participant quotation. Each image is a post-session recreation made from the
tested HTML prototype at the participant's viewport. Static screenshots show
the relevant interface state, while keyboard behaviour and the absence of
post-action feedback are also supported by interaction and DOM-state checks.
The roster-dialog, conversation-switching and Save draft observations were
supplementary checks made during the named task sessions, so they do not revise
the report's aggregate task results.

## Finding summary

| Participant | Task | Finding | Consequence | Evidence |
| --- | --- | --- | --- | --- |
| User A | T5 | Keyboard focus moved outside the Create roster dialog. Escape did not close it, and focus was not returned to the opening control after closing. | The participant lost the interaction context and required assistance. | [UserA-T5-roster-modal-focus.png](UserA-T5-roster-modal-focus.png) |
| User B | T2 | The Discover tabs did not respond to Left/Right Arrow keys, and the selected state relied mainly on colour and a thin underline. | The participant completed the task with a pointer, but keyboard navigation and the selected state were unclear. | [UserB-T2-tab-keyboard-selected-state.png](UserB-T2-tab-keyboard-selected-state.png) |
| User C | T4 | The privacy warning appeared after contact details were entered, but the relationship between the warning and the icon-only contact-sharing action was unclear. | The participant paused for more than 30 seconds and continued after one facilitator hint. | [UserC-T4-contact-block-clarity.png](UserC-T4-contact-block-clarity.png) |
| User C | T5 | Selecting Chinese translated the rule content while surrounding headings, labels and actions remained in English. | The mixed-language state reduced content clarity and made the language setting appear incomplete. | [UserC-T5-mixed-language.png](UserC-T5-mixed-language.png) |
| User D | T4 | At 390 by 844 pixels, the conversation list and New message control were hidden with no visible mobile replacement. | This restricted mobile conversation management because the participant could not select Daniel or begin a new conversation. | [UserD-T4-mobile-conversation-controls.png](UserD-T4-mobile-conversation-controls.png) |
| User E | T5 | Selecting Save draft produced no visible confirmation, navigation or control-state change. | The participant selected the control twice and assumed it was not working. | [UserE-T5-save-draft-no-feedback.png](UserE-T5-save-draft-no-feedback.png) |
| User E | T5 | Approval progress was displayed separately from the activation condition and was not sufficiently prominent. | The participant requested clarification and did not complete the task independently. | [UserE-T5-mobile-approval-status.png](UserE-T5-mobile-approval-status.png) |

## Evidence descriptions

### User A — T5 — Create roster dialog keyboard behaviour

![The Create roster dialog remains open after keyboard focus has left the dialog](UserA-T5-roster-modal-focus.png)

The image records the open dialog at the iPad viewport of 1180 by 820 pixels.
During the recreation, repeated Tab presses moved `document.activeElement` to
the page body, outside the dialog. Escape left the dialog visible, and closing
it left focus on the body instead of the Create roster button. The static image
shows the dialog state; the focus-escape and focus-return conclusions depend on
the accompanying interaction and DOM observations.

Recommended change: trap focus within the active dialog, close the top-most
dialog with Escape, make the background inert and restore focus to the control
that opened it.

### User B — T2 — Discover tab keyboard and selected state

![Discover tabs with Housemates selected](UserB-T2-tab-keyboard-selected-state.png)

The image records the Housemates tab selected at the MacBook viewport. During
the recreation, pressing Right Arrow did not move selection to Reviews. The
controls also lacked tab roles and `aria-selected`, while the visible selected
state depended mainly on green text and a thin underline.

Recommended change: implement the tab keyboard pattern and programmatic
selected state, then add a stronger non-colour indicator such as weight, shape
or an explicit selected label.

### User C — T4 — Contact-detail warning clarity

![A blocked phone-number message with the privacy warning and icon-only sharing control](UserC-T4-contact-block-clarity.png)

The image records the blocked phone-number message at 1366 by 768 pixels. The
warning explains that personal details were not sent, but the required
"mutual contact sharing" action is separated from it and represented by an
unlabelled-looking icon. This supports the observation that the participant
saw the warning but did not understand the next action.

Recommended change: place a labelled contact-sharing action in or immediately
beside the warning and state what will happen after it is selected.

### User C — T5 — Mixed-language interface

![Chinese house-rule content surrounded by English headings and controls](UserC-T5-mixed-language.png)

The image records the language control set to Simplified Chinese. Rule titles
and descriptions are translated, while headings and actions such as
"House rules", "Language" and "Propose rule" remain in English.

Recommended change: apply the selected language consistently to the complete
task flow and expose the correct page or section language metadata to assistive
technology.

### User D — T4 — Mobile conversation controls

![The mobile Messages screen shows one conversation without a conversation picker or New message control](UserD-T4-mobile-conversation-controls.png)

At the iPhone viewport of 390 by 844 pixels, only the active Emily conversation
is available. The desktop conversation list, Daniel conversation control and
New message control are hidden, and no mobile replacement is shown.

Recommended change: provide a mobile conversation picker or back-to-list
pattern and retain a labelled New message action.

### User E — T5 — Save draft feedback

![The mobile Save draft control remains unchanged after activation](UserE-T5-save-draft-no-feedback.png)

The image records the Samsung viewport immediately after Save draft was
selected. The URL, control label, enabled state and visible page content were
unchanged, and no confirmation text appeared. This evidence supports a lack of
visible feedback; it does not by itself establish whether data was persisted.

Recommended change: show an in-page or live-region confirmation, update the
draft status and provide a clear route back to the saved item.

### User E — T5 — Approval and activation status

![A mobile house-rule proposal with one of three approvals](UserE-T5-mobile-approval-status.png)

The image records one completed approval, two remaining responses and an
"Awaiting approval" label at 360 by 800 pixels. The count is present, but the
activation condition is distributed across the card and proposal explanation,
which supports improving its prominence rather than claiming it is absent.

Recommended change: combine the count and condition in one persistent status,
for example, "1 of 3 approved — activates automatically after all 3 approve."
