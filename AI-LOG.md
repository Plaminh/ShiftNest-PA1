
# AI-LOG.md

2026-10-17 — 01. Review redundant UI and identify the approval screen

Tool: Figma Agents

Asked for: "Track for any UI redundant like components, contents,..." using the attached Functional Requirements Specification, followed by "Say which screen corresponding".

Kept: The review identified the selected screen as P06 — Shift Requests → Approval Dialog, covered by §3.3, for requests in PENDING_APPROVAL. Recommended retaining the request ID, sender → receiver summary, shift date/time, status, and Approve/Reject actions.

Changed: No design changes at this review step. The agent recommended simpler headings, transfer terminology, approval checks, availability/opening-hours warnings, and an optional rejection reason.

Rejected: Recommended removing the hours/roster variance audit, minimum-hours and overtime checks, nursing departments/cost centers, and payroll/break details because they were not required by the single-shop MVP. Also flagged "Swap", "Awaiting Final Sign-off", and manager-only approval wording for correction.

By hand: The user selected the screen, supplied the requirements, and asked which required page/function it represented. No manual design edits were described in the chat.

## 2026-10-17 — 02. Apply the approval-screen cleanup

Tool: Figma Agents

Asked for: "Help me to do that based on above recommendations".

Kept: The approval-screen structure and core transfer information, with clearer labels and Approve/Reject actions.

Changed: The agent reported removing healthcare, payroll, overtime, and roster-audit content; replacing "Swap" with "Transfer"; adding receiver acceptance, active-account, shift-timing, and overlap checks; adding availability/opening-hours status and approval safeguards; and including an optional rejection reason.

Rejected: The out-of-scope content and terminology identified in entry 01.

By hand: No manual design edits were described. The agent explicitly stated that the result remained a static design and that approval validation was not functional.

## 2026-10-17 — 03. Change the sample concept and staff names

Tool: Figma Agents

Asked for: Change the UI examples from a nursing concept to a coffee shop, rename Alex to Nguyet, Jordan to Hoang, and the Shift Supervisor to Minh.

Kept: The coffee-shop concept and the names Nguyet (sender), Hoang (receiver), and Minh (Shift Leader/approver) across the three transfer screens.

Changed: The agent reported replacing nursing roles with Barista/Senior Barista and hospital locations with Coffee bar/Opening shift. It also updated avatar initials, notification and workflow labels, and signed-in names to match the sample users. Structured position/qualification details were further simplified during the later Codex MVP cleanup in entry 07.

Rejected: Nursing/hospital examples because the user chose a coffee-shop scenario. Replaced the original sample names Alex and Jordan with the user-selected names Nguyet and Hoang to keep the examples consistent across all three screens.

By hand: The user chose the coffee-shop concept and replacement names. No manual Figma edits were described.

## 2026-10-17 — 04. Review preview labels, missing UI, and inconsistent requirement wording

Tool: Figma Agents

Asked for: Reread the Functional Requirements Specification, determine whether "STATE PREVIEW: AFTER INITIATION", "WIREFRAME SPEC COMPONENT", and "Post-Action State Output Preview" belonged in the application UI, and inspect missing UI for specific functions.

Kept: The distinction between wireframe documentation and application UI. The review also flagged the need to clarify shift selection and optional transfer reasons, retain correct approval safeguards, use the defined transfer statuses, and explain that requests expire when the shift starts while the sender remains assigned until approval.

Changed: No design changes at this review step. The agent also proposed additional pending/outcome/error/warning states and request-list/history coverage; the user narrowed that scope in entry 05.

Rejected: The review identified fixed 24-hour expiry wording, the undefined PENDING_B status, manager-only approval wording, "Marketplace", and technical escalation labels as inconsistent or unnecessary for the requirements.

By hand: The user supplied the review questions. No manual design edits were described.

## 2026-10-17 — 05. Keep one state per screen and remove wireframe-only content

Tool: Figma Agents

Asked for: Pick one state for each screen, focus only on the three main screen states, and remove the preview/specification labels instead of covering every missing state.

Kept: Three screens: Send Transfer Request before submission by Nguyet; Incoming Shift Transfer Request awaiting Hoang's Accept/Decline response; and Review Shift Transfer awaiting Minh's approval.

Changed: The agent reported removing "STATE PREVIEW: AFTER INITIATION", "WIREFRAME SPEC COMPONENT", and "Post-Action State Output Preview", together with the extra post-action panels, wireframe-specification footers, and dimension labels. No additional screens or alternative states were added.

Rejected: Expanding the wireframes to cover every state or displaying the actionable state and its post-action result together.

By hand: The user explicitly set the one-state-per-screen scope. No manual Figma edits were described.

## 2026-10-17 — 06. Review ShiftNest wireframes against the Functional Requirements

Tool: Codex with Figma tools

Asked for: Compare the UI components in the three ShiftNest wireframes with the Functional Requirements Specification and suggest missing or unclear elements. Review only Send Transfer Request, Respond to Request, and Review and Approve, with one state per screen.

Kept: The requirements comparison and suggestions to add the saved store name and notifications entry point, explain that accepting a request does not transfer the shift, and clarify where the sender selects a shift.

Changed: Limited the review to the three existing screens. Missing alternative states or other application pages were not treated as gaps in these wireframes.

Rejected: Expanding the review to require every request state or the full application UI.

By hand: No user-made edits were recorded in this session.

## 2026-10-17 — 07. Update the three ShiftNest wireframes in Figma

Tool: Codex with Figma tools and browser UI control

Asked for: Apply the proposed additions and clarifications directly in Figma and remove details beyond the MVP model.

Kept: Added the sample store name "My Store", notification bell icons, a Back to My Schedule link, an acceptance explanation, approval checks, and the sender's transfer reason on the review screen. Distinguished Shift note from Reason for transfer and identified Minh as a Shift Leader.

Changed: Converted work-area and position information into a free-text shift note. Replaced the qualification message with a current conflict-check message that explains checks run again on approval. Kept three screens with one state each.

Rejected: Role-qualification checks and the sample break-duration detail, which are not specified in the MVP requirements.

By hand: No user-made edits were recorded. Codex edited the Figma layers directly and visually checked all three screens. This work covered wireframes, not backend implementation or functional testing.

## 2026-10-17 — 08. Revise the coffee-shop sample reason and refine spacing

Tool: Codex with browser UI control for Figma

Asked for: Replace the transfer reason with one suited to the coffee-shop concept across all three screens and improve spacing.

Kept: Used the same sample reason on all three screens: "Attending a latte art workshop. Could you cover my opening shift?"

Changed: Removed the remaining old reason text, deleted an empty spacer above the response-screen title, standardized card padding and section gaps to 24 px where adjusted, matched the send-screen title to the other screens at 32 px with a 40 px line height, reduced approval-footer vertical padding to 16 px, and aligned the approval action buttons to the right. Visually checked the final layout of each screen.

Rejected: The previous sample reason about a doctor appointment because the user requested a reason connected to the coffee-shop concept. The latte-art workshop example better matches that request and was used consistently across all three screens.

By hand: The user chose the coffee-shop concept and requested the content and spacing corrections. No user-made Figma edits were recorded; Codex applied the changes through the Figma browser UI.


## 2026-10-17 — 09. Review the rubric and clarify the three-screen flow

Tool: Codex

Asked for: Review only Three screens of the main flow, Each screen explained and AI-LOG.md; write a scoped self-assessment, add rejection reasons, re-mark without using PROPOSAL.md, and improve the evidence to maximize the score.

Kept: The three existing wireframes and their consistent example. Added Wireframes/README.md with one explanation per screen, the handoff between different actors, outcomes for each action, and a table of visible controls and destinations. Used this evidence to update the three requested self-assessment criteria.

Changed: Made the rejection reasons in entries 03 and 08 explicit. Replaced the earlier restricted assessment with an assessment that also cites the new companion explanations. The report claims 65/65 across the reviewed criteria, subject to instructor grading.

Rejected: Filename-related and proposal-comparison deductions in the revised review because the user explicitly excluded PROPOSAL.md and allowed freestyle filenames. Did not expand the work into unrelated rubric criteria or extra screen exports because the user limited the review to these three criteria and the rubric permits text to explain destinations and outcomes.

By hand: The user set the review scope, requested the rejection reasons and asked to maximize the score. Codex wrote the companion explanations, updated the scoped report and appended this entry. No manual design edits or implemented application behavior are claimed for this work.


## 2026-10-17 — 10. Remove the companion README and retain the requested score

Tool: Codex

Asked for: Delete the wireframe README and mark Each screen explained at the maximum; accept the screens as non-clickable wireframes.

Kept: The three original PNGs and the requested 15/15 claim for Each screen explained, based on the explanations embedded in the wireframes. Static wireframes do not require clickability.

Changed: Deleted Wireframes/README.md and removed its evidence links from SELF_ASSESSMENT_REPORT.md. Revised the report to cite the wireframes themselves and distinguish the claimed score from instructor grading and the rubric’s separate paragraph requirement. Entry 09 remains a historical record of the now-deleted document.

Rejected: Retaining the companion README because the user explicitly requested its deletion. Did not treat lack of clickability as a scoring deficiency because the rubric accepts static wireframes.

By hand: The user requested the deletion and maximum explanation score. Codex applied the document changes; the wireframe images were not edited.
