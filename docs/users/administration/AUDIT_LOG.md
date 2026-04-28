# Audit Log (Administration)

This manual explains how admins and operations staff use the Audit Log to review organization activity.

## 1. Who Can Use Audit Log

Audit Log access is intended for administrative roles:
1. Owner
2. Admin
3. Operations

If you do not see `Audit Log` in the sidebar, your current role does not have access.

## 2. Opening Audit Log

1. Open the left sidebar.
2. Select `Audit Log`.
3. Use the filter panel to narrow results when needed.

## 3. What You See In Each Entry

Each row shows:
1. `Timestamp`: when the change happened.
2. `User`: who made the change (or `System` for automated actions).
3. `Action`: the operation, such as created, updated, deleted, or notification/email events.
4. `Entity Type`: what was changed (resource, calendar event, member, blog entry, etc.).
5. `Entity`: label and/or ID, with a direct link when available.
6. `Details`: before/after values and metadata (for example recipient info on sent messages).

## 4. Filtering Audit History

Use `Filter` to narrow by:
1. Start date
2. End date
3. Entity type
4. Action

Use `Apply Filters` to run the search, or `Clear` to reset.

## 5. Understanding Change Details

For updates, many entries include side-by-side `Before` and `After` values so you can quickly see exactly what changed.

For notification and messaging records, details can include message metadata such as subject, recipient information, and delivery context.

## 6. Common Admin Use Cases

1. Confirm who changed resource settings or status.
2. Trace who updated a member, endorsement, or organization setting.
3. Verify when a message or notification was sent.
4. Investigate unexpected schedule or billing-related changes.

## 7. Best Practices

1. Apply filters first when investigating a specific issue.
2. Use entity links to jump directly into the affected record.
3. Include timestamp, user, and entity ID when sharing findings with your team.
4. Review high-impact changes regularly (resources, members, invoicing, organization settings).
