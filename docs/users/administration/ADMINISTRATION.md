# Administration

This manual is for organization admins who run day-to-day operations in Contact Ground.

It explains how to use the application in practical terms, including:
- Inviting and managing members
- Adding and managing resources
- Setting organization options
- Keeping operations, scheduling, and billing settings aligned

## 1. What an Admin Is Responsible For

Admins typically handle:
1. Member access and role assignment
2. Resource setup and availability
3. Organization settings (operations, scheduling, invoicing, messaging)
4. Ongoing data quality for smooth flight ops and billing

If your organization has an owner role, owners usually handle subscription and top-level account decisions, while admins handle daily configuration and execution. Financial workflows such as invoices, credits, and credit-request review require `owner` or `accounting` access; `admin` alone is not enough.

## 2. First-Time Admin Setup Checklist

Use this checklist when you are new to an organization:
1. Open `Organization` and verify organization name, home base, and logo.
2. Open `Invite` and send invites for core roles (operations, accounting, instructors, members).
3. Open `People` and confirm each person has the correct role(s).
4. Open `Resource` and add all active aircraft/resources.
5. Confirm flight operations mode and invoicing mode match your club process.
6. Enable only the messaging and scheduling options your team will actively use.

## 3. Inviting Members

Go to `Invite` and complete:
1. Member email
2. One or more roles
3. Send Invite

Pending invites appear below the form so you can track who has not accepted yet.

### 3.1 Invite roles and when to use them

1. `Owner`:
Use for top-level organization control and subscription authority.
2. `Admin`:
Use for trusted staff who will configure settings and manage operations. This role does not grant invoicing or credit-review access unless the person also has `Accounting`.
3. `Operations`:
Use for dispatch, resource readiness, maintenance coordination, and flight ops workflows.
4. `Accounting`:
Use for invoicing, credits, statements, and billing workflows.
5. `CFI` / `CFII` / `DPE`:
Use for training, check ride, and instructor-specific workflows.
6. `Member`:
Use for standard scheduling and member activity.

### 3.2 Role capability quick reference

This table is intentionally high-level. Members can hold more than one role, and combined roles get the union of those permissions.

| Role | Can do | Cannot do |
| --- | --- | --- |
| `Owner` | Full organization control, subscription/billing authority, invite any role, assign protected roles like `owner` and `accounting`, manage members, resources, maintenance, flight ops, checklists, check rides, club events, audit log, scheduling on behalf, invoicing and credits | No role-based restriction inside the organization |
| `Admin` | Manage members, invite most roles, configure organization settings, manage resources, maintenance, flight ops, checklists, club events, audit log, scheduling on behalf | Cannot assign or invite `owner`; cannot assign or modify `accounting`; does not get invoicing or credit-review access unless they also have `accounting` |
| `Operations` | Manage dispatch/flight ops, maintenance workflows, resources, checklists, club events, view audit log, send invitations when `Member Invitations` is enabled, invite non-owner/non-accounting roles | Cannot manage member roles, cannot access invoicing/credits, cannot assign protected roles, cannot schedule on behalf unless another role grants it |
| `Accounting` | Manage invoices, statements, credits, credit-request review, send invitations when `Member Invitations` is enabled, invite non-owner/non-accounting roles | Cannot manage members, resources, maintenance, flight ops, or checklists; cannot invite or assign `owner` or `accounting`; no special scheduling-on-behalf access by itself |
| `CFI` | Instructor workflows, endorsements, check rides, schedule on behalf when enabled, send invitations when `Member Invitations` is enabled, invite non-owner/non-accounting roles | Cannot manage members, organization settings, invoicing, flight ops, resources, maintenance, or checklists unless another role grants it |
| `CFII` | Same practical access pattern as `CFI`, including instructor workflows, endorsements, check rides, and scheduling on behalf when enabled | Same limitations as `CFI` |
| `DPE` | Examiner/check-ride workflows, endorsements, scheduling on behalf when enabled, send invitations when `Member Invitations` is enabled, invite non-owner/non-accounting roles | Cannot manage members, organization settings, invoicing, flight ops, resources, maintenance, or checklists unless another role grants it |
| `Member` | Standard scheduling, personal profile/preferences, submit flight updates and credit requests, invite `member` users when `Member Invitations` is enabled | Cannot manage members, organization settings, audit log, resources, maintenance, flight ops, checklists, invoicing, or schedule on behalf |

### 3.3 Multi-role invitations

Invitations can include more than one role when a member needs combined access (for example `Member` + `CFI`, or `Operations` + `Accounting`).

Important rules:
1. Only `Owner` can invite another `Owner`.
2. Privileged inviters can assign multiple non-owner roles in one invitation.
3. If `Member Invitations` is enabled, standard members can invite only `Member` role users.

### 3.4 Invitation control option

In `Organization` -> `Invitations`:
- `Member Invitations`:
When enabled, members can invite others. Keep this off if your club wants only admin/owner-controlled invites.

## 4. Managing Members After They Join

Use `People` to maintain user access:
1. Review member list
2. Open a member profile
3. Update roles as responsibilities change
4. Add or remove endorsements when needed

Good practice:
1. Avoid giving broad admin access when a focused role works better.
2. Use `Accounting` for billing permissions instead of relying on `Admin`.
3. Review roles monthly so access stays current.

## 5. Adding Resources

Go to `Resource` -> `New Resource`.

### 5.1 Resource fields and what they mean

1. `Resource Name`:
Display name (tail number, call name, simulator name, etc.).
2. `Description`:
Optional notes that help members identify the resource.
3. `Resource Type`:
Choose the best category (airplane, helicopter, simulator, etc.).
4. `Current Hours`:
Current tach value used for tracking and maintenance context.
5. `Hobbs Hours`:
Shown only when Hobbs tracking is enabled at org level.
6. `Hourly Rate`:
Used for scheduling/invoicing calculations.
7. `Status`:
- `Available`: normal scheduling
- `Unavailable`: block all booking
- `Maintenance`: restrict booking to maintenance-capable roles
8. `Requires Endorsement`:
Limits scheduling to members who hold selected endorsements.
9. `Pre- and Post-flight Checklists`:
Assign checklists that should be shown in flight workflows for this resource.

### 5.2 Resource setup tips

1. Set realistic current hours before first use.
2. Use `Unavailable` for temporary admin blocks (not maintenance scheduling strategy).
3. Use `Maintenance` when the resource is under maintenance control.
4. Add required endorsements for complex/high-performance resources.

## 6. Organization Settings: Option Guide

Use `Organization` for these settings.

## 6.1 Profile and branding

1. `Organization Name`:
Member-facing organization identity.
2. `Home base (ICAO Airport ID)`:
Primary airport context used across the app.
3. `Organization Logo`:
Branding shown in UI and generated documents.

## 6.2 Availability and reminders

1. `Availability Event Type`:
Enables instructor availability workflows.
2. `Currency Reminders`:
Enables organization-defined and member-defined reminder tracking with expiration notifications.
3. `Manage Currency Reminders`:
Where you configure reminder definitions once enabled.

## 6.3 Schedule controls

1. `Enable Schedule Limit`:
Turns on future-booking caps.
2. `Maximum future events`:
Defines each member’s booking cap.
3. `Enforce limit for instructors and DPEs`:
When off, CFI/CFII/DPE roles are exempt.

## 6.4 Resource hours tracking

1. `Enable Hobbs Hours`:
Tracks Tach and Hobbs separately.
2. If disabled:
The app uses a single hours model.

## 6.4a Reserve on Behalf

1. `Enable Reserve on Behalf`:
Allows owners, admins, and flight instructors (CFI/CFII/DPE) to create, edit, or delete reservations for other members. When disabled, each member can only manage their own events. See `docs/users/instructors/SCHEDULING_ON_BEHALF.md` for full details.

## 6.5 Flight operations mode

1. `Manual`:
Team-driven post-flight process.
2. `Automatic`:
System-driven reminder prompts plus team oversight.
3. `Off`:
Disables flight operations tracking; invoicing options are limited/disabled.

## 6.6 Invoicing options

1. `Enable Invoicing`:
Turns on invoice and credit workflows.
2. `Invoicing Mode`:
- `Manual Invoicing`: manage invoices directly in Contact Ground
- `QuickBooks Integration`: sync accounting workflows with QuickBooks Online
3. `Invoice Hour Type` (when Hobbs is enabled):
- `Tach Time` or `Hobbs Time` for flight-hour billing basis
4. `Notify members about invoices`:
Sends member invoice emails when enabled.
5. `Monthly Member Rate`:
Current monthly recurring member charge.
6. `Schedule Monthly Rate Change`:
Set a future effective date for a new monthly rate.

## 6.7 Organizational messaging

Choose audience targeting modes:
1. `Individuals`
2. `Roles`
3. `Endorsements`
4. `Entire Organization`

If none are selected, messaging is hidden in the UI.

## 7. Suggested Admin Operating Rhythm

### 7.1 Daily
1. Review critical notifications.
2. Confirm resources are in correct status.
3. Check for open operational blockers (squawks, overdue items, missing updates).

### 7.2 Weekly
1. Review pending invites and role assignments.
2. Validate resource rates and availability status.
3. Confirm settings still match real operating policy.

### 7.3 Monthly
1. Review invoicing configuration before billing run.
2. Review schedule limit behavior and role exceptions.
3. Clean up stale roles/permissions.

## 8. Common Admin Mistakes To Avoid

1. Enabling features without assigning staff ownership.
2. Leaving resources in incorrect status after changes.
3. Over-assigning admin-level roles.
4. Enabling invoicing while flight ops process is incomplete.
5. Forgetting to communicate setting changes to operations/accounting teams.

## 9. Related Manuals

1. Owner setup and subscription:
`docs/users/owners/OWNER_CONFIGURATION.md`
2. Manual invoicing:
`docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK.md`
3. QuickBooks invoicing:
`docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK_QUICKBOOKS.md`
4. Flight operations:
`docs/users/operations/FLIGHT_OPERATIONS.md`
5. Maintenance:
`docs/users/operations/MAINTENANCE.md`
6. Instructor guidance:
`docs/users/instructors/INSTRUCTOR_AVAILABILITY_AND_RATES.md`
7. Audit log:
`docs/users/administration/AUDIT_LOG.md`
8. Organizational messaging:
`docs/features/ORGANIZATIONAL_MESSAGING.md`
9. Blog entries:
`docs/features/BLOG_ENTRIES.md`
