# ShiftNest - PA#1 Project Proposal

## 1. Team

| Full name | Student ID |
| --- | --- |
| [Full name] | [Student ID] |
| [Full name] | [Student ID] |
| [Full name] | [Student ID] |

## 2. The problem

Small cafes and bakeries often arrange shifts and last-minute changes through chat messages. Leaders find it difficult to compare staff availability, avoid overlapping assignments and confirm who is responsible for a transferred shift. A colleague may agree to cover a shift before the leader has approved the change. ShiftNest gives one shop a shared schedule and a clear transfer process: an employee requests a transfer, the receiver responds, and a Shift Leader or Manager approves before the schedule changes.

## 3. Users

| User | Main goals |
| --- | --- |
| Employee | Declare availability, view personal shifts, request or respond to transfers, and track the outcome. |
| Shift Leader | View staff availability, manage the team schedule and review transfers. Leaders also have Employee permissions. |
| Manager | Manage staff accounts, store settings, schedules and transfer approvals. Managers are not assigned shifts and do not declare availability. |
| Signed-out staff member | Sign in or recover a password by email. There is no public registration. |

## 4. Main flow

The main flow transfers one future shift from A to B. The sender and receiver are active Employees or Shift Leaders. The reviewer is an authorized Shift Leader or Manager who is neither sender nor receiver.

1. **Request:** A selects an assigned shift in My Schedule, chooses B and sends a request. Its status becomes **Waiting for receiver**; A remains assigned.
2. **Response:** B opens the request and selects **Accept** or **Decline**. Accept sends it for approval; Decline ends the request. Acceptance alone does not change the assignment.
3. **Approval:** The reviewer checks the shift and B's eligibility. **Approve transfer** assigns the shift to B and marks the request approved together. **Reject** leaves A assigned. Both employees can see the outcome and updated schedule on refresh.

A can cancel while the request is pending; the shift remains assigned to A. A shift can have only one pending transfer. Changing its date, time or assignee, or cancelling it, ends the pending request. Requests still unresolved when the shift starts expire when checked.

## 5. Scope

### In scope

- A responsive website for one shop, with role-based access and dashboards.
- Staff login, initial-password change, email password recovery, profile updates and avatar upload. Managers create staff accounts.
- Dated availability, personal schedules and team schedules. Leaders and Managers can create, edit and cancel future shifts; each shift has one assignee.
- One-way shift transfers with receiver response, independent approval, cancellation, expiry, basic status history and in-app notifications.
- Staff account and role management, an editable store name and weekday opening hours. The store timezone is set at deployment.
- Scheduling checks: invalid times, started shifts, inactive assignees and overlapping shifts for the same assignee block changes. Outside or undeclared availability and opening-hours violations require confirmation. Approval rechecks these conditions.

### Not building

- Multiple shops or branches in one deployment, public registration or a setup wizard.
- Payroll, GPS/QR attendance, leave management, contracts, analytics or reports.
- Two-way shift swaps, AI scheduling, recurring weekly availability or overnight shifts.
- Chat, calendar integration, push/SMS notifications or realtime updates.
- Advanced audit logs, in-app timezone changes, split opening hours or holiday exceptions.
- A separate native mobile application.

## 6. Screens

The three wireframes follow the same request from the sender, receiver and reviewer perspectives. The shared example is a shift on 24 October 2026, 08:00-12:00, initially assigned to A.

### Screen 1 - Send Transfer Request

**Image:** `wireframes/01-send-request.png`

A wants a colleague to cover the shift. My Schedule shows the selected shift and a transfer form for selecting an active Employee or Shift Leader as receiver, with an optional reason. **Send request** records the request, shows confirmation and notifies B, who next opens screen 2. A remains assigned. **Cancel** closes the unsent form and returns to the schedule. Sending is blocked if the shift is ineligible or already has a pending request.

### Screen 2 - Respond to Transfer Request

**Image:** `wireframes/02-respond-request.png`

B wants to decide whether to cover A's shift. The received request shows A, the shift date/time, reason and status. **Accept** displays **Waiting for approval** and sends the request to the reviewer in screen 3; A remains assigned. **Decline** ends the request and displays the result without changing the schedule. The request remains in the list with its history, and response actions become unavailable once B has responded.

### Screen 3 - Review Transfer Request

**Image:** `wireframes/03-approve-request.png`

An independent Shift Leader or Manager wants to approve or reject the accepted request. The screen shows A, B, the shift, B's acceptance, availability and any overlapping shifts. **Approve transfer** rechecks the conditions and displays **Approved**, with B as the new assignee. **Reject**, with an optional reason, displays **Rejected** and keeps A assigned. Errors block approval; warnings require confirmation. The result stays on this screen, further actions are disabled, and both employees are notified.

### Supporting navigation

| Destination, if shown | Purpose |
| --- | --- |
| Dashboard | Role-specific summary of shifts and requests. |
| My Schedule | Personal calendar and shift details. |
| My Availability | Dated availability editor. |
| Team Schedule | Staff calendar for Leaders and Managers. |
| Shift Requests | Sent/received requests and the authorized approval queue; selecting a request opens its details. The sender can cancel a pending request here. |
| My Profile | Personal details, avatar and password settings. |
| Notifications | Updates linking to the related shift or request. |
