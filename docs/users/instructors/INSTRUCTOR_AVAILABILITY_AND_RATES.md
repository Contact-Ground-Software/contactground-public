# Instructor Availability and Rates

This manual is for instructors (CFI, CFII, DPE) who use Contact Ground to:
- Publish calendar availability
- Respond to member availability requests
- Manage instructor service rates

It focuses on the instructor workflow from opening availability to booking instruction and keeping rates current.

## 1. Before You Start

### 1.1 Access and prerequisites
You need an instructor role in your organization (`cfi`, `cfii`, or `dpe`).

Owner/admin configuration dependencies:
1. `Availability Event Type` must be enabled in `Organization`.
2. Your member profile should carry your instructor role(s).

### 1.2 Where key pages are
- Calendar availability and responses: left sidebar `Calendar`
- Instructor rate management: `People` -> open your member profile -> `Instructor Rates`
- Notifications: `Notifications` page and email links

## 2. Publishing Availability

### 2.1 Create an availability block
From `Calendar`:
1. Click an open timeslot.
2. Set event type to `Availability`.
3. Set start/end time.
4. Optional: select a resource (aircraft/equipment) for that block.
5. Save.

Important:
- Resource is optional for `Availability` events.
- Non-availability events require a resource.

### 2.2 Manage existing availability
You can edit or delete your own availability events at any time.

Role behavior:
- Event owners can edit/delete their own availability.
- Owner/admin can edit/delete any availability event.

## 3. Member Request Flow (Availability Process)

### 3.1 How members request your time
Members view availability on the calendar and submit a request with:
1. Purpose
2. Requested time window (within your availability block)

### 3.2 Notification and response
When a request is submitted, you receive notification (email and/or in-app based on preferences).

You can respond by:
1. `Accept`
2. `Decline` (with reason)

### 3.3 Accepting a request
On acceptance:
1. Confirm event details.
2. Choose required data (including resource when needed).
3. Submit acceptance.

System behavior:
- Accepted request creates the booked training/checkride event.
- Original availability block is split so remaining open time stays available.
- Request status is updated and the requester is notified.

Resource note:
- If the original availability block did not include a resource, acceptance may require selecting one.

### 3.4 Declining a request
On decline:
1. Provide a useful reason.
2. Submit.

System behavior:
- Request status changes to declined.
- Member receives response notification.

## 4. Instructor Rates

Instructor rates are maintained on your member profile and can be used for invoicing line items.

Open:
1. `People`
2. Select your member record
3. Scroll to `Instructor Rates`

### 4.1 Add a rate
In `Instructor Rates`, click `Add Rate` and set:
1. `Service Name` (required)
2. `Service Type` (required): `Hourly` or `Flat`
3. `Rate (USD)` (required)
4. Optional description
5. `Active` toggle

Examples:
- Flight Instruction (`Hourly`)
- Ground Instruction (`Hourly`)
- Check Ride Prep (`Flat`)

### 4.2 Edit or delete a rate
For any existing rate:
1. Edit to update name/type/rate/status/description.
2. Delete only when the rate should no longer be used.

Best practice:
- Mark old rates inactive instead of deleting when you need historical clarity.

### 4.3 Who can edit rates
Rate editing is allowed for:
1. The instructor themself
2. Owner/admin/leadership roles

## 5. Operational Best Practices

1. Publish availability in consistent blocks (for example, 2-4 hour windows).
2. Include clear purpose expectations in acceptance notes.
3. Keep rates current before month-end billing runs.
4. Inactivate obsolete rates when pricing changes.
5. Review pending requests daily so members are not blocked.

## 6. Troubleshooting

### 6.1 Members cannot request your availability
Check:
1. `Availability Event Type` enabled in `Organization`.
2. Your event is actually `Availability` type.
3. Requested time is inside your block.

### 6.2 Accept action fails
Common causes:
1. Requested time outside original availability block
2. Required resource not selected during acceptance
3. Time overlap conflict created by newer events

Action:
1. Refresh the request page.
2. Verify requested window and resource.
3. Re-submit response.

### 6.3 Rates not visible or editable
Check:
1. You are on the correct member profile.
2. Profile has instructor role (`cfi`, `cfii`, `dpe`).
3. You are the profile owner or have owner/admin/leadership role.

