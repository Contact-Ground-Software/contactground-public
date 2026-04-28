# Maintenance

This manual is for operations users managing aircraft/resource health in Contact Ground.

It covers:
- Squawk intake and triage
- Resource status behavior in scheduling
- Maintenance due/reminder configuration
- Predicted due dates for hour-based maintenance items
- Maintenance events on the calendar
- How maintenance status is calculated in reports and booking checks

> **See also:** [Maintenance Reminders and Calendar](../../features/MAINTENANCE_REMINDERS.md) for a detailed reference on predicted due dates, reminder notifications, and calendar display.

## 1. Before You Start

### 1.1 Access and prerequisites
You should have a maintenance-capable role (typically `owner`, `admin`, or `operations`) to:
1. Edit resource status.
2. Add/edit/delete maintenance items.
3. Close squawks.

Any authenticated member can report a squawk. Maintenance-capable roles manage closure and readiness decisions.

### 1.2 Where key pages are
- Resource details and maintenance item setup: left sidebar `Resource`
- Squawk reporting and closure workflow: `Reports` -> `Squawks`
- Maintenance due dashboard: `Reports` -> `Maintenance`
- Availability and maintenance blocks: left sidebar `Calendar`

## 2. Squawk Workflow

Standard squawk lifecycle:
1. `Open` - issue reported and awaiting review
2. `Closed` - issue corrected and closed by maintenance-capable staff

Important:
1. Squawks are created as `Open` and can be transitioned to `Closed`.
2. Use notes and operational communication channels for work-in-progress context and status updates.

## 3. Resource Statuses and Scheduling Rules

Resource statuses are set on the `Resource` page:
1. `Available`:
Resource can be booked normally, subject to endorsement/currency/overlap rules.
2. `Unavailable`:
Resource cannot be booked by any user.
3. `Maintenance`:
Resource can only be booked by maintenance-capable roles (`owner`, `admin`, `operations`).

Additional booking guardrails:
1. If any maintenance item is overdue (hours or date), booking is blocked for non-maintenance roles.
2. Maintenance-capable roles can still schedule when overdue items exist.
3. `maintenance`/`wash` calendar blocks created by maintenance-capable roles can cancel overlapping non-maintenance reservations.

## 4. Maintenance Reminder Configuration

Maintenance reminders are configured per resource under `Maintenance Items`.

For each maintenance item, set:
1. `Description`
2. `Hours Interval`
3. `Due at Hours`
4. `Date Interval (days)`
5. `Due Date`
6. `Reminder (days before due)` — how many days before the due date (or predicted due date for hour-based items) the operations team should be notified. Set to `0` to disable.

Configuration model:
1. Each maintenance item uses exactly one tracking mode: hours or date.
2. Hours tracking is active when both `Hours Interval > 0` and `Due at Hours > 0`.
3. Date tracking is active when both `Date Interval > 0` and `Due Date` is set.
4. If you need to track both hours and date thresholds for the same task, create two separate maintenance items (one hours-based and one date-based).

For hour-based items, Contact Ground calculates a **predicted due date** based on the resource's average weekly usage over the past three months. This predicted date is shown in the resource detail view and on the calendar. See [Maintenance Reminders and Calendar](../../features/MAINTENANCE_REMINDERS.md) for calculation details.

## 5. How Maintenance Reminders Work

Maintenance status is calculated from:
1. Resource current hours
2. Maintenance item due thresholds
3. Current date

Reminder status categories:
1. **Due**: Maintenance is now required
   - Hours: When aircraft has reached or passed the due hours
   - Date: When the due date has arrived or passed

2. **Upcoming**: Maintenance needed soon
   - Hours: When within approximately 10% of the interval
   - Date: When within 30 days of the due date

3. **OK**: No immediate action required

Where you see maintenance status:
1. Maintenance reports show all items with their status
2. Resource views display nearest due item and progress
3. Calendar booking checks enforce overdue restrictions
4. Calendar shows upcoming maintenance as read-only informational events (see below)

Important notes:
1. Status updates automatically as aircraft hours accumulate from flight operations
2. After completing maintenance work, manually update the due value for that item's tracking mode

## 5a. Upcoming Maintenance on the Calendar

Maintenance items appear on the calendar as **read-only** events that are visible to all users but do not block booking:

- **Date-based items**: Shown as an all-day orange event on the due date.
- **Hour-based items**: Shown with a dashed yellow border on the statistically predicted due date, labelled as "Prediction".

To change a due date or interval, edit the maintenance item directly on the `Resource` page. Calendar events for maintenance cannot be edited from the calendar view.

## 6. Daily Maintenance Runbook

1. Review `Reports` -> `Squawks` filtered to `Open`.
2. Confirm dispatch impact and set resource status (`Available`/`Unavailable`/`Maintenance`) as needed.
3. Review `Reports` -> `Maintenance` for `Due` and `Upcoming` items.
4. Close squawks only after corrective action is complete.
5. Update maintenance item due thresholds when work completion resets the cycle.

## 7. End-of-Day Maintenance Checklist

1. New squawks are triaged.
2. `Open` squawks have a documented next action.
3. Closed squawks are confirmed resolved.
4. Resource status reflects real dispatch readiness.
5. Due/upcoming maintenance items have an action plan.

## 8. Month-End Maintenance Checklist

1. Review unresolved squawks by age and severity.
2. Identify repeat-failure patterns and root causes.
3. Validate maintenance item due values still reflect real next due thresholds.
4. Share operational risk summary with leadership.

## 9. Troubleshooting

### 9.1 Squawk not visible to the right team
Action:
1. Confirm organization and resource context.
2. Check status and role visibility.
3. Re-post/update entry with clear details.

### 9.2 Resource still appears unavailable after fix
Action:
1. Confirm resource `Status` is not set to `Unavailable` or `Maintenance`.
2. Confirm overdue maintenance items are resolved or intentionally allowed by role.
3. Confirm blocking calendar events are cleared.
4. Re-check availability after refresh.

### 9.3 Repeated issue with similar symptoms
Action:
1. Compare notes across prior squawks.
2. Document suspected root cause.
3. Escalate to deeper inspection and track as recurring maintenance risk.
