# Maintenance Reminders and Calendar

This manual explains how Contact Ground tracks maintenance due dates, sends proactive reminders to the operations team, and surfaces upcoming maintenance events directly on the calendar.

## 1. Overview

Aircraft maintenance intervals are typically determined either by flight hours or by calendar dates. Maintenance items in Contact Ground can be tracked by one or the other, but not both. If you need both thresholds for the same task, create two maintenance items. For each item you can configure a **reminder lead-time** (in days) so the operations team is notified before the work is due.

Upcoming maintenance is automatically shown on the calendar as **read-only, informational events**.  These events are visible to all users but cannot be edited from the calendar; they do not block members from booking the resource.

## 2. Reminder Days Field

Each maintenance item has a **Reminder (days before due)** field.  When set to a value greater than zero, the notification service sends a `maintenance` notification to all operations-capable roles (`owner`, `admin`, `operations`) on:

| Item type | Reminder sent on |
|-----------|-----------------|
| Date-based | `Due Date` − **Reminder (days before due)** |
| Hour-based | `Predicted Due Date` − **Reminder (days before due)** |

**Example:** If the due date is September 30 and Reminder Days is 14, the reminder is sent on September 16.

Set **Reminder (days before due)** to `0` to disable reminders for an item.

## 3. Predicted Due Dates (Hour-Based Items)

When an item is tracked by hours (i.e., both `Hours Interval` and `Due at Hours` are set), Contact Ground calculates a **predicted calendar date** for when the resource will reach the due threshold.

### How the prediction works

1. The system looks at the resource's flight-hours records from the past **three months** (90 days).
2. If fewer than three months of data exist, all available records are used.
3. The **average weekly usage** (hours flown per week) is calculated from those records.
4. The predicted due date is computed as:

   ```
   Predicted Due Date = Today + (Hours Remaining / Average Weekly Hours) weeks
   ```

   where `Hours Remaining = Due at Hours − Current Hours`.

5. If there is no usage history, or the item is already overdue, no prediction is shown.

The predicted rate is recalculated each time data is loaded; it is not stored in the database.

## 4. Calendar Display

Upcoming maintenance appears on the calendar in two forms:

| Form | Appearance | Condition |
|------|-----------|-----------|
| **Maintenance Due** | Solid orange all-day event on the due date | Date-based items with a `Due Date` |
| **Maintenance Prediction** | Dashed yellow event on the predicted date | Hour-based items with a calculable prediction |

These events:
- Are **read-only** — they cannot be clicked to edit.
- Do **not** block members from making reservations.
- Appear across all calendar views (day, week, resource).

To change due dates or intervals, navigate to `Resource` → select the resource → edit the maintenance item directly.

## 5. Maintenance Blocks vs. Maintenance Reminders

| Feature | Maintenance Block | Maintenance Reminder |
|---------|-------------------|---------------------|
| Purpose | Reserve downtime on the calendar | Alert ops team before work is due |
| Blocks booking? | Yes | No |
| Created by | Operations role via calendar | Automatic (from maintenance item config) |
| Editable from calendar? | Yes | No |

## 6. Setting Up Reminders

1. Open `Resource` from the left sidebar.
2. Select the resource to configure.
3. Under **Maintenance Items**, click **Add Maintenance Item** or **Edit** an existing item.
4. Fill in:
   - `Description`
   - Either `Hours Interval` and `Due at Hours` (hour-based) or `Date Interval (days)` and `Due Date` (date-based)
   - `Reminder (days before due)` — enter the number of days in advance to notify the operations team
5. Save.

The notification service checks for reminders on every cycle (approximately every 5 minutes) and sends notifications when the trigger date matches today.

## 7. Viewing Predictions in the Resource Detail

When viewing a resource, the maintenance item list shows:

- Current hours status (overdue, due soon, or OK)
- For hour-based items: the **predicted due date** and the estimated weekly usage rate used for the calculation
- The configured reminder lead-time

## 8. Best Practices

1. Set reminder lead-times to match your maintenance planning cycle (e.g., 14 days for 100-hour inspections, 30 days for annual inspections).
2. Review predicted dates periodically — high-utilisation weeks or reduced flying will shift predictions.
3. After completing maintenance, update the due value for that item's tracking mode to reset the cycle.
4. Use maintenance blocks on the calendar to reserve downtime once the actual work is scheduled.
