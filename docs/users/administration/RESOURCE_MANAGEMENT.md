# Resource Management

This manual is for administrators who add, configure, and maintain resources in Contact Ground.

Resources are the aircraft, simulators, or other equipment your organization makes available for scheduling. Keeping resource data accurate is essential for booking, billing, and maintenance tracking.

## 1. Before You Start

### 1.1 Access and prerequisites
You need one of these roles to manage resources:
1. `Owner`
2. `Admin`
3. `Operations`

Members can view resource details but cannot make changes.

### 1.2 Where key pages are
- Resource list: left sidebar `Resource`
- Add a new resource: `Resource` → `New Resource`
- Edit an existing resource: `Resource` → select a resource → edit form
- Hourly rate scheduling: resource detail page → `Hourly Rate` section
- Maintenance items: resource detail page → `Maintenance Items` section
- Checklists: left sidebar `Checklist`

## 2. Adding a New Resource

Go to `Resource` → `New Resource` and complete the form.

### 2.1 Required fields

1. `Resource Name`:
   - The display name used throughout the app (for example, tail number, call name, or simulator name).
   - Keep names short and consistent so members can identify resources quickly.

2. `Resource Type`:
   - Choose the category that best describes the resource.
   - Options: `Airplane`, `Seaplane`, `Helicopter`, `Glider`, `Balloon`, `Simulator`, `Boat`, `RV`, `Other`.

3. `Status`:
   - Set the initial status. Choose `Available` for most new resources.

### 2.2 Optional fields

1. `Description`:
   - Use this for notes that help members identify the resource (model, color, equipment notes).

2. `Current Hours (Tach)`:
   - Enter the current tachometer reading. This is used for maintenance tracking.
   - Set this accurately before the first use. Maintenance intervals calculate from this value.

3. `Hobbs Hours`:
   - Appears only when `Enable Hobbs Hours` is on in organization settings.
   - Enter the current Hobbs meter reading if your organization tracks both Tach and Hobbs.

4. `Requires Endorsement`:
   - Check this to restrict booking to members who hold specific endorsements.
   - When enabled, select which endorsement types are required.
   - Members missing any selected endorsement will not be able to book this resource.

5. `Pre- and Post-flight Checklists`:
   - Assign checklists that should be sent with this resource's flight reminder workflows.
   - Checklists are included in pre-flight and post-flight notification emails.
   - Create checklists first at `Checklist` before assigning them here.

## 3. Editing an Existing Resource

From `Resource`, select any resource to open its detail page, then use the edit form to update any field.

Changes take effect immediately. If you change a resource's status, the new status applies to all future booking attempts right away.

## 4. Resource Status

Resource status controls who can book a resource and how it appears on the calendar.

| Status | Who Can Book | Typical Use |
|--------|-------------|-------------|
| `Available` | All eligible members | Normal operating condition |
| `Unavailable` | Nobody | Admin hold, temporary withdrawal from service |
| `Maintenance` | Operations-capable roles only | Active maintenance in progress |

### 4.1 When to use each status

1. **Available:**
   - Use for any resource that is in normal flyable condition.
   - Overdue maintenance items will still block non-operations roles from booking even when status is `Available`.

2. **Unavailable:**
   - Use when you need to block all booking without putting the resource in active maintenance.
   - Useful for administrative holds, awaiting parts, or reserved periods.

3. **Maintenance:**
   - Use when the resource is actively under maintenance control.
   - Operations and admin roles can still book maintenance events.
   - Regular members cannot book the resource.

### 4.2 How overdue maintenance affects booking
When any maintenance item is overdue (hours or date), members without operations-level access cannot book the resource, even if its status is `Available`. Operations-capable roles can still schedule the resource.

## 5. Hourly Rate Management

Hourly rates are used when generating invoices for member flight time.

### 5.1 Setting the current hourly rate

From a resource's detail page, scroll to `Hourly Rate`:
1. Enter the hourly rate in USD.
2. Leave `Effective At` blank to apply the rate immediately.
3. Click `Schedule Change`.

### 5.2 Scheduling a future rate change

To change the rate at a specific date (for example, at the start of next month):
1. Enter the new hourly rate in USD.
2. Set the `Effective At` date.
3. Click `Schedule Change`.

The current rate stays in effect until the scheduled date. Upcoming rate changes appear in the schedule list so you can review or cancel planned changes.

### 5.3 Rate change tips

1. Set rates before month-end billing runs.
2. Schedule future changes in advance to avoid billing surprises.
3. Review the schedule list to confirm the right rate is active.
4. Contact accounting when rates change so they can verify upcoming invoices.

## 6. Maintenance Items

Maintenance items track scheduled inspections, time-limited airworthiness directives, and recurring service tasks.

For full maintenance management workflow, see:
`docs/users/operations/MAINTENANCE.md`

### 6.1 Adding a maintenance item

From a resource's detail page, scroll to `Maintenance Items` → `Add Item`:
1. `Description`: What the maintenance task is (for example, `100-Hour Inspection`, `Annual`).
2. `Hours Interval`: How many tach hours between services (for example, `100`).
3. `Due at Hours`: The next due hours value (for example, `1250` if the resource is currently at 1150 hours and a 100-hour is coming due).
4. `Date Interval (days)`: Calendar-based interval in days (for example, `365` for annual).
5. `Due Date`: The next due date.

Each item must use one tracking mode:
1. Hours-based: fill `Hours Interval` and `Due at Hours`.
2. Date-based: fill `Date Interval (days)` and `Due Date`.
3. If you need both modes for the same maintenance task, create two separate maintenance items.

### 6.2 Updating after maintenance is completed

After maintenance is performed:
1. Update the due value for the item's tracking mode (`Due at Hours` or `Due Date`).
2. Confirm the resource status is set back to `Available` when it is ready for service.

## 7. Endorsement-Restricted Resources

Some resources require member qualifications before booking is allowed.

### 7.1 Configuring endorsement requirements

1. On the resource edit form, check `Requires Endorsement`.
2. Select all endorsement types a member must hold.
3. Save the resource.

From that point, only members with all selected endorsements can schedule the resource.

### 7.2 Managing endorsement types

Endorsement types are defined at the organization level in `Organization` → `Endorsements`. For full endorsement management, see:
`docs/features/ENDORSEMENTS.md`

## 8. Assigning Checklists to Resources

Checklists guide members through pre-flight and post-flight procedures.

### 8.1 Steps to assign a checklist

1. Create the checklist at `Checklist` first (see `docs/users/operations/CHECKLISTS.md`).
2. Open the resource edit form.
3. In the `Pre- and Post-flight Checklists` section, select the checklists to assign.
4. Save the resource.

You can assign multiple checklists to a single resource. Assigned checklists appear in member flight notification emails.

When an assigned checklist's contents change, Contact Ground also sends a checklist update notification so members know the guidance changed for that resource.
When a checklist is newly assigned to a resource, Contact Ground also sends a checklist assignment notification so members know the resource now carries that checklist.

## 9. Deleting a Resource

Deletion is permanent and removes the resource from all future scheduling.

Before deleting a resource:
1. Close any open squawks on the resource.
2. Confirm there are no future reservations that rely on it.
3. Ensure flight operations data is complete for all historical flights.

If a resource is no longer in service but has historical records you want to preserve, consider setting status to `Unavailable` instead of deleting.

## 10. Resource Management Best Practices

1. **Accurate hours from day one:** Set current hours correctly before the first booking. All maintenance intervals are calculated from this baseline.
2. **Status discipline:** Keep status current. Operations are blocked or allowed based on what the system shows.
3. **Proactive rate scheduling:** Schedule hourly rate changes in advance, not day-of.
4. **Link checklists:** Assign appropriate checklists to every resource so members receive consistent pre/post-flight guidance in notifications.
5. **Review monthly:** Check each resource's status, maintenance items, and upcoming rate changes at the start of every billing period.

## 11. Troubleshooting

### 11.1 Members cannot book an available resource
Possible causes:
1. Resource status is `Unavailable` or `Maintenance`.
2. A maintenance item is overdue.
3. Member is missing a required endorsement.
4. Member has expired enforced currency.
5. The member has outstanding overdue flight reports.

Action:
1. Confirm resource status on the resource detail page.
2. Check `Reports` → `Maintenance` for overdue items.
3. Review the member's endorsements in `People`.
4. Check the member's currency status in `Currency Reminders`.

### 11.2 Hourly rate not applying to invoices
Common causes:
1. The rate change was scheduled for a future date, not applied immediately.
2. A new rate was entered but not saved.

Action:
1. Check the `Hourly Rate` schedule on the resource detail page.
2. Confirm the correct rate is listed and that the effective date is in the past.
3. Regenerate the invoice if it was already drafted before the rate update.

### 11.3 Maintenance item status not updating
Common causes:
1. Current hours on the resource record have not been updated from flight operations data.
2. Due at Hours or Due Date fields were not updated after the last service.

Action:
1. Review the resource's current hours field.
2. Confirm that post-flight reports with correct meter readings have been submitted and processed.
3. Update the maintenance item due values to reflect the next service target.

## 12. Related Manuals

1. Maintenance workflow:
   `docs/users/operations/MAINTENANCE.md`
2. Checklist management:
   `docs/users/operations/CHECKLISTS.md`
3. Endorsements:
   `docs/features/ENDORSEMENTS.md`
4. Administration overview:
   `docs/users/administration/ADMINISTRATION.md`
5. Invoicing:
   `docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK.md`
