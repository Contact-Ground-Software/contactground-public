# Currency Reminders

This manual describes the implemented currency reminder system in Contact Ground.

## 1. Feature Overview

Currency reminders let organizations and members define reminder types, track expiration dates, and send reminder notifications.

Reminder types are generic. An organization or member may use them for qualifications, memberships, documents, trainings, or other expiring items.

There are two reminder scopes:
1. Organization-level reminder types (created by leadership).
2. Personal reminder types (created by individual members).

## 2. Where It Is Managed

### 2.1 Member view
Members use `Profile` -> `Currency Tracking` to:
1. View reminders.
2. Set/update expiration dates.
3. Manage personal reminder types.

### 2.2 Leadership view
Leadership uses `Organization Currency Reminders` (`/currency-reminders`) to:
1. Create organization-level reminder types.
2. Mark types as enforced/non-enforced.
3. Set default reminder lead time.
4. Open the organization currency status report.

## 3. Enforcement Behavior

If a reminder type is marked `Enforced` at the organization level:
1. Expired members can be blocked at booking time.
2. The booking error includes the expired enforced reminders.

Non-enforced reminders still notify but do not block booking.

## 4. Notifications

Currency reminders use member notification preferences:
1. Category toggle: `Currency Reminders`.
2. Delivery method: email/SMS/push from profile settings.

## 5. Data Model Behavior (User-Visible)

1. Organization-level reminder types are shared across all members.
2. Members cannot delete organization-level reminder types.
3. Members can create/delete personal reminder types.
4. Reminder lead time is tracked in days.
5. Contact Ground does not require reminder types to map to FAA or medical-specific categories.

## 6. Troubleshooting

### 6.1 Currency tracking not available
Cause: This feature is not enabled by default and the organization owner or an admin must turn it on.

Action: ask an owner/admin to enable it in organization settings.

### 6.2 Booking blocked by currency
Action:
1. Open `Profile` -> `Currency Tracking`.
2. Update expired enforced reminder dates.
3. Retry booking.

### 6.3 Not receiving currency reminder notifications
Check:
1. `Currency Reminders` category is enabled.
2. At least one delivery method is enabled.
