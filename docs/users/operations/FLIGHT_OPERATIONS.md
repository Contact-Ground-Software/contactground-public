# Flight Operations

This manual is for operations users managing daily flight activity in Contact Ground.

It covers:
- Daily flight operations and board monitoring
- What the `Flight Ops` page shows
- Flight operations workflows in `Manual` and `Automatic` modes
- Missing data follow-up and correction
- Operational notifications and escalation
- End-of-day and month-end operations checks

## 1. Before You Start

### 1.1 Access and prerequisites
You should have an operations-capable role in your organization (typically owner, admin, leadership, or operations).

Flight operations tools are available when Flight Operations Mode is set to:
1. `Manual`, or
2. `Automatic`

If Flight Operations Mode is `Off`, operations workflows and downstream invoicing inputs are limited.

### 1.2 Where key pages are
- Organization settings: left sidebar `Organization`
- Flight operations list and edits: left sidebar `Flight Ops`
- Calendar and reservations: left sidebar `Calendar`
- Invoices (for billing impact checks): left sidebar `Invoices`
- Member alerts and status: `Notifications`

## 2. What Flight Operations Shows

The `Flight Ops` page is the operations team's central board for tracking submitted flight activity, reviewing post-flight reports, correcting data, and confirming that flight records are ready for billing.

Each entry can include:
1. Member
2. Resource
3. Event date/time
4. Hours flown
5. Tach hours (current)
6. Hobbs hours, if enabled
7. Oil added
8. Squawks
9. PIREPs or notes
10. Open and closed squawk counts for the resource

Use this view to identify missing reports, review reported discrepancies, and confirm recorded hours are complete before maintenance and billing workflows rely on them.

## 3. One-Time Setup Checklist

Open `Organization` and confirm:
1. Flight Operations Mode is `Manual` or `Automatic`.
2. Notification settings match your operating policy.
3. Resource rates and member billing settings are current (so post-flight data flows cleanly into billing).
4. Operations users know escalation rules for overdue reports and squawks.

## 4. Daily Operations Runbook

### 4.1 Start-of-day checks
At start of operations:
1. Review today's reservations in `Calendar`.
2. Check resource status for maintenance restrictions or unresolved squawks.
3. Review recent `Notifications` for operational exceptions.
4. Open `Flight Ops` and review entries from the prior operating period.

### 4.2 Flight monitoring during active operations
During the day:
1. Monitor expected departures and returns from the board/calendar.
2. Watch for overdue activity and missing post-flight updates.
3. Coordinate with members when required updates are not submitted on time.

### 4.3 Identifying missing reports
In `Manual` mode:
- Entries appear only when members submit reports.
- If a flight occurred but no entry exists, operations must follow up and obtain the missing data.

In `Automatic` mode:
- The system sends reminder and compliance emails.
- Operations should still monitor exceptions and verify that reminders resulted in complete entries.

### 4.4 Post-flight completeness checks
For completed flights, verify:
1. Hobbs/tach (or equivalent) values were provided.
2. Oil usage entries are present when applicable.
3. Squawks were reported when needed.
4. Entries were associated with the correct member and resource.

Why this matters:
- These records drive maintenance visibility and invoice line-item generation.

## 5. Manual vs Automatic Flight Operations

### 5.1 Manual mode expectations
In `Manual` mode, operations staff are responsible for enforcing completeness:
1. Follow up on missing entries.
2. Add or correct entries when required.
3. Resolve data quality issues before billing windows close.

### 5.2 Automatic mode expectations
In `Automatic` mode, Contact Ground sends reminder and compliance emails, but operations still own final quality:
1. Monitor exceptions surfaced by notifications.
2. Confirm that automation produced complete, accurate entries.
3. Apply manual corrections where automation cannot infer real-world conditions.
4. If the organization enables **Associated Event Members**, event creators can include additional members on a reservation so another instructor, dispatcher, or member sees the event as shared. In `Automatic` mode, those included members are also copied on the same automatic reminders.
5. Included recipients also see that reservation on their own calendars as a shared event. The calendar link in the notification opens that scheduled event directly instead of sending them to a generic calendar view.

Member reminder timing:
1. Each member can choose when to receive their preflight brief.
2. Supported lead times are at event time, 15 minutes, 30 minutes, 45 minutes, or 1 hour before departure.
3. If a reservation is created after the ideal reminder time has passed, Contact Ground still sends one catch-up preflight brief while the event remains upcoming.
4. Extra copied recipients receive the same automatic reminder sequence for that event, subject to their own notification preferences.
5. Contact Ground now creates separate notification types for:
   - someone being added to an event
   - an included event being changed
   - an event being created on someone else's behalf

## 6. Correcting Flight Ops Data

From `Flight Ops`:
1. Edit incorrect entries when values are wrong.
2. Use `Add Manual Entry` for missing records.
3. Re-check downstream effects in invoicing if changes are made after draft generation.

Recommended correction order:
1. Fix resource and time values first.
2. Fix member attribution second.
3. Check impact on invoicing last.

### 6.1 Editing an existing entry
Use this when a submitted report is present but contains incorrect information.

Update fields such as:
- `Hours Flown`
- `Current Hours (Tach)`
- `Hobbs Hours`
- `Oil Added`
- `Squawks`
- `PIREPs`

Corrected data affects resource hour tracking, maintenance visibility, and invoice generation. Verify changes before the billing period closes.

### 6.2 Adding a missing entry
Use `Add Manual Entry` only when a flight occurred but the member did not submit the report and operations has reliable data to complete it.

Confirm:
1. Member
2. Resource
3. Submitted At / flight date and time
4. Hours flown and meter readings
5. Oil added, squawks, and PIREPs where applicable

Manual entries should be the exception, not the default workflow.

### 6.3 Deleting an entry
Delete an entry only when it was created in error or duplicated.

Before deleting:
1. Confirm the entry should not exist at all.
2. Confirm no downstream billing or maintenance workflow is relying on it.
3. Re-check the affected resource's hour totals after deletion.

## 7. Coordination With Maintenance and Billing

### 7.1 Maintenance handoff
When squawks are reported:
1. Confirm squawk details are readable and actionable.
2. Ensure maintenance users are notified.
3. Track status changes until closed.

### 7.2 Billing handoff
Before invoices are generated:
1. Confirm period flight entries are complete.
2. Resolve obvious anomalies (duplicate or missing entries).
3. Coordinate with accounting on any late corrections.

### 7.3 Pre-billing verification checklist
Before accounting generates invoices:
1. Confirm entries exist for every expected flight in the billing period.
2. Verify hour readings are accurate and complete.
3. Correct zero-hour, duplicate, or implausible entries.
4. Add missing entries only when reliable source data is available.
5. Communicate data completeness or known exceptions to accounting before draft generation.

Why this matters:
- Invoice line items for flight time depend on the records in `Flight Ops`.
- Missing or incorrect entries create billing errors that are harder to unwind after invoices are sent.

## 8. End-of-Day Checklist

1. No unresolved overdue post-flight reports without documented follow-up.
2. Critical squawks are acknowledged by maintenance workflow.
3. Same-day corrections are complete in `Flight Ops`.
4. Operations notifications are reviewed and cleared or escalated.

## 9. Month-End Operations Checklist

1. Billing-period flight entries are complete and accurate.
2. Manual corrections are finalized before draft invoices are sent.
3. Known exceptions are communicated to accounting.
4. Repeat issues are documented for process improvement.

## 10. Troubleshooting

### 10.1 Cannot access Flight Ops
Common causes:
- Role does not include operations-capable access
- Flight Operations Mode is off for the organization

Action:
1. Confirm role assignment with an admin or owner.
2. Confirm the organization has Flight Operations Mode enabled.

### 10.2 Missing flight entries
Common causes:
- Member did not submit report
- Reservation mismatch
- Late submissions

Action:
1. Confirm reservation context.
2. Create or correct entry in `Flight Ops`.
3. Notify accounting if invoice drafts already exist.

### 10.3 Hour readings or reported data look wrong
Common causes:
- Member entered data incorrectly
- Tach and Hobbs values were swapped
- Wrong resource was used on the entry

Action:
1. Compare the entry against current resource values and prior activity.
2. Confirm actual readings with the member if needed.
3. Correct the entry before billing and maintenance workflows proceed.

### 10.4 Unexpected billing outcomes from operations data
Common causes:
- Wrong resource/rate association
- Missing or duplicate usage entries

Action:
1. Correct `Flight Ops` data first.
2. Regenerate affected drafts where needed.

## 11. Related Manuals

1. Maintenance and squawk management:
   `docs/users/operations/MAINTENANCE.md`
2. Invoicing and billing:
   `docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK.md`
3. Resource management:
   `docs/users/administration/RESOURCE_MANAGEMENT.md`
4. Member-facing post-flight workflow:
   `docs/users/members/PILOT_SCHEDULING_GUIDE.md`
