# ShiftNest - PA#1 Project Proposal

## 1. Team

| Full name | Student ID |
| --- | --- |
| Phan Lê Anh Minh | 24127082 |
| Hồ Phan Như Nguyệt |  24127211 |
| Huỳnh Thái Hoàng | 24127171 |

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

The main flow transfers one future shift from Employee A (Nguyet), the sender, to Employee B (Hoang), the receiver. Shift Leader (Minh) is the sample independent approver. An authorized Shift Leader or Manager may approve a transfer provided they are neither the sender nor the receiver.

1. **Request:** Employee A selects an assigned future shift, chooses Employee B and submits a transfer request. Its status becomes **Waiting for receiver**, and Employee A remains assigned.
2. **Response:** Employee B selects **Accept** or **Decline**. Acceptance moves the request to **Waiting for approval** without changing the shift assignment. Declining ends the request.
3. **Approval:** An authorized Shift Leader or Manager reviews the request and rechecks eligibility and scheduling conflicts. **Approve transfer** assigns the shift to Employee B; **Reject** leaves it assigned to Employee A.

The sender can cancel a pending request without changing the shift assignment. A shift can have only one pending transfer request. Changing its date, time or assignee, or cancelling the shift, ends the pending request. An unresolved request expires when the shift starts and its status is next checked. The shift is reassigned only after approval.

## 5. Scope

The implementation priorities are shift scheduling, availability management and controlled shift transfers.

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

The three wireframes follow the same request from the sender, receiver and reviewer perspectives. The shared example is a shift on 24 October 2026, 07:00-15:30, sent by Nguyet to Hoang and reviewed by Minh, a Shift Leader. The shift remains assigned to Nguyet until approval.

### Screen 1 - Send Transfer Request

**Image:** `wireframes/01-send-transfer-request.png`

Nguyet wants Hoang to cover the shift. My Schedule shows the selected shift and a transfer form for selecting an active Employee or Shift Leader as receiver, with an optional reason. **Send request** records the request, shows confirmation and notifies Hoang, who next opens screen 2. Nguyet remains assigned. **Cancel** closes the unsent form and returns to the schedule. Sending is blocked if the shift is ineligible or already has a pending request.

### Screen 2 - Respond to Transfer Request

**Image:** `wireframes/02-respond-to-request.png`

Hoang wants to decide whether to cover Nguyet's shift. The received request shows Nguyet, the shift date/time, reason and status. **Accept** displays **Waiting for approval** and sends the request to Minh in screen 3; Nguyet remains assigned. **Decline** ends the request and displays the result without changing the schedule. The request remains in the list with its history, and response actions become unavailable once Hoang has responded.

### Screen 3 - Review Transfer Request

**Image:** `wireframes/03-review-and-approve.png`

Minh, an independent Shift Leader, wants to approve or reject the accepted request. The screen shows Nguyet, Hoang, the shift, Hoang's acceptance, availability and any overlapping shifts. **Approve transfer** rechecks the conditions and displays **Approved**, with Hoang as the new assignee. **Reject**, with an optional reason, displays **Rejected** and keeps Nguyet assigned. Errors block approval; warnings require confirmation. The result stays on this screen, further actions are disabled, and both employees are notified.

### Supporting navigation

| Destination, if shown | Purpose |
| --- | --- |
| Dashboard | Role-specific summary of shifts and requests. |
| My Schedule | Personal calendar and shift details. |
| My Availability | Dated availability editor. |
| Team Schedule | Staff calendar for Leaders and Managers. |
| Shift Requests | Sent/received requests and the authorized approval queue; selecting a request opens its details. The sender can cancel a pending request here. |
| My Profile / profile control | The signed-in name or profile icon opens personal details, avatar and password settings. |
| Notifications | The header bell opens updates that link to the related shift or request. |
| History | A filtered view associated with Shift Requests, showing the signed-in user's completed or ended requests (approved, rejected, declined, cancelled or expired). Selecting an entry opens the related request details in read-only form. |
| Back to My Schedule / Cancel (screen 1) | **Back to My Schedule** returns to the personal schedule. **Cancel** closes the unsent transfer form and returns there without creating a request. |
