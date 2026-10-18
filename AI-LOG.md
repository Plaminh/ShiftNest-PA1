# AI Usage Log — ShiftNest PA#1

## 2026-10-17 — 01. Review the approval screen

**Tool:** Figma Agents

**Asked for:** Identify the selected screen and review unnecessary UI against the Functional Requirements Specification.

**Kept:** The request ID, sender and receiver, shift date/time, status, and Approve/Reject actions.

**Changed:** No design edits at this step. The review identified the screen as the transfer approval dialog and suggested clearer labels and approval checks.

**Rejected:** The review recommended removing healthcare, payroll, overtime and roster-audit details because they were outside the MVP.

**By hand:** The team selected the screen and supplied the requirements.

## 2026-10-17 — 02. Simplify the approval screen

**Tool:** Figma Agents

**Asked for:** Apply the approval-screen recommendations.

**Kept:** The screen structure, core transfer information and Approve/Reject actions.

**Changed:** The agent reported removing unrelated content, replacing “Swap” with “Transfer”, and adding receiver acceptance, account status, shift timing, overlap checks, availability/opening-hours warnings and an optional rejection reason.

**Rejected:** The out-of-scope content identified in entry 01.

**By hand:** No manual design edits were recorded. These changes describe a static wireframe, not working validation.

## 2026-10-17 — 03. Use a consistent coffee-shop example

**Tool:** Figma Agents

**Asked for:** Replace the nursing scenario with a coffee shop and use Nguyet, Hoang and Minh as the sample users.

**Kept:** Nguyet as sender, Hoang as receiver and Minh as the independent Shift Leader reviewing the request.

**Changed:** The agent reported updating names, initials, signed-in users and coffee-shop content across the three screens. Position and qualification details were simplified further in entry 07.

**Rejected:** Hospital terminology and the original sample names because they did not match the chosen scenario.

**By hand:** The team chose the scenario and replacement names.

## 2026-10-17 — 04. Review labels and transfer rules

**Tool:** Figma Agents

**Asked for:** Check preview labels, missing information and transfer rules against the requirements.

**Kept:** Suggestions to clarify shift selection, the optional transfer reason, request statuses and approval safeguards. The sender remains assigned until approval; unresolved requests expire when the shift starts.

**Changed:** No design edits at this step. The agent also suggested additional states, which the team narrowed in entry 05.

**Rejected:** The review flagged fixed 24-hour expiry, the undefined PENDING_B status, manager-only approval wording and “Marketplace” as inconsistent with the requirements.

**By hand:** The team supplied the review questions.

## 2026-10-17 — 05. Keep three screens with one state each

**Tool:** Figma Agents

**Asked for:** Focus on the three main states and remove wireframe-only labels and extra previews.

**Kept:** Nguyet preparing a request, Hoang responding to it and Minh reviewing the accepted request.

**Changed:** The agent reported removing preview/specification labels, post-action panels, specification footers and dimension labels.

**Rejected:** Adding every possible state or showing an actionable form and its completed result together.

**By hand:** The team set the three-screen scope.

## 2026-10-17 — 06. Check the three screens against the requirements

**Tool:** Codex with Figma tools

**Asked for:** Review the three existing screens for missing or unclear information.

**Kept:** Suggestions to show the store name and notifications, clarify where the sender selects a shift, and explain that receiver acceptance only sends the request for approval.

**Changed:** The review stayed within the three selected screens.

**Rejected:** Requiring all application pages or every request state for these wireframes.

**By hand:** No manual design edits were recorded in this review.

## 2026-10-17 — 07. Update the wireframes in Figma

**Tool:** Codex with Figma tools and browser UI control

**Asked for:** Apply the proposed clarifications and remove details beyond the MVP.

**Kept:** The three-screen structure and one state per screen.

**Changed:** Added “My Store”, notification icons, Back to My Schedule, the acceptance explanation, approval checks and the transfer reason on the review screen. Separated the shift note from the transfer reason, identified Minh as a Shift Leader and converted work-area/position details into a free-text note. Codex visually checked the three screens.

**Rejected:** Qualification checks and break-duration details because they were outside the requirements.

**By hand:** No manual design edits were recorded; Codex applied the Figma changes.

## 2026-10-17 — 08. Draft screen explanations and a scoped self-assessment

**Tool:** Codex

**Asked for:** Review the three-screen flow, screen explanations and AI log; clarify rejection reasons; then remove the companion README.

**Kept:** The three wireframes and their shared example. Static wireframes were accepted as a valid submission format.

**Changed:** Codex drafted screen explanations and a self-assessment covering three criteria, clarified rejection reasons, then deleted the README and removed its evidence references at the team's request. The assessment was later expanded to all five criteria in entry 09.

**Rejected:** Requiring clickability or additional screens for this milestone.

**By hand:** The team set the review scope and requested removal of the README. Codex made the document edits.

## 2026-10-18 — 09. Align the proposal and self-assessment

**Tool:** ChatGPT / Codex

**Asked for:** Synchronize the proposal with the wireframes and assess all five rubric criteria.

**Kept:** The idea, MVP scope and transfer flow using Nguyet, Hoang and Minh for the shift on 24 October 2026, 07:00–15:30.

**Changed:** Updated the proposal's sample details and image paths, explained the History destination, and completed the five-row self-assessment with evidence references. Names and student IDs remained placeholders pending the team's details.

**Rejected:** Inventing personal information, adding features or screens, and deducting marks for user research or a flow diagram that the rubric did not require.

**By hand:** The team supplied the requested corrections. Codex revised the documents.
