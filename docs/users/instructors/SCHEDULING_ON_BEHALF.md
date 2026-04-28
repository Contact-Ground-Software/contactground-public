# Scheduling Reservations on Behalf of a Member

Owners, admins, and flight instructors (CFI / CFII / DPE) can create, edit, or delete calendar reservations on behalf of another member. This is useful for scenarios such as scheduling checkout flights for new students who have not yet received their required endorsements.

## Enabling the Feature

Before anyone can use this feature, an **owner or admin** must enable it in the organization settings:

1. Navigate to **Org Settings** (the settings page for your organization).
2. Scroll to the **Reserve on Behalf** section.
3. Check **Enable Reserve on Behalf**.
4. Click **Save**.

Once enabled, eligible roles will see the "Book on behalf" panel when creating events.

## Who Can Use This Feature?

| Role | Can book on behalf? |
|------|---------------------|
| Owner | ✅ Yes |
| Admin | ✅ Yes |
| CFI | ✅ Yes |
| CFII | ✅ Yes |
| DPE | ✅ Yes |
| Operations | ❌ No |
| Member | ❌ No |

## Creating a Reservation on Behalf of a Member

### Web (Calendar)

1. Open the **Calendar** and click an open time slot (or navigate to **Create Event**).
2. Fill in the event details (resource, event type, start/end time) as usual.
3. A **"Book on behalf of a member"** panel appears at the bottom of the form (visible only to eligible roles when the feature is enabled).
4. Select the member's name from the drop-down. The **Reason** field becomes required.
5. Enter a reason/comment explaining why you are booking on their behalf (e.g., *"Scheduling checkout flight for new student who lacks endorsement"*).
6. If your organization enables **Associated Event Members**, you can also include other members on the reservation. These members see the event on their calendars and receive event-sharing notifications. If `Automatic` flight operations is also enabled, they receive the same pre-flight, 30-minute, and overdue reminders for that reservation.
7. Included members now also see the reservation on their personal calendar views as a **shared** event card. They can open it from the calendar or from the notification link, but they only get edit controls when their role already allows editing that event.
8. Click **Save**.

### Mobile (Schedule Screen)

1. Tap **+** to open the **New Event** editor.
2. Fill in event details as normal.
3. Scroll down to the **Book on behalf of a member** panel.
4. Tap the member's name chip to select them. The **Reason** field appears.
5. If your organization enables **Associated Event Members**, use the extra member selector to include other members on the reservation. If `Automatic` flight operations is also enabled, those members get the same automatic reminder sequence.
6. Included recipients see the reservation on their mobile schedule as a shared event and can open it directly from notifications.
7. Enter a reason and tap **Save**.

## Editing or Deleting Another Member's Reservation

When you open a reservation owned by another member and have the required role, an **Admin comment** field is shown at the bottom of the form. This comment is **required** before you can save or delete the event.

> The comment is recorded in the audit log and serves as an explanation for the change.

## Audit Log

All on-behalf actions are recorded in the organization's **Audit Log** with:
- The **acting user** (the admin or instructor who performed the action).
- An `onBehalfOf` field indicating the event owner (the member whose reservation was created/modified).
- The **reason comment** provided at the time of the action.

Members also receive event notifications that distinguish between:
- An event created on their behalf
- Being added to another member's event
- An included event being changed

Audit logs are accessible to owners, admins, and operations roles from the **Audit Log** section.

## Validation Bypasses

When a privileged user books on behalf of a member, the following checks are **skipped** for the target member (since the admin is taking explicit responsibility):

- Resource endorsement requirements.
- Enforced currency reminders.
- Organization schedule limits.
- Resource maintenance status checks.

Overlap detection remains active — you cannot double-book a resource regardless of the booking method.
