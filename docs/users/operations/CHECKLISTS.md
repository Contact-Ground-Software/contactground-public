# Checklists

This manual covers the checklist features that are currently implemented in Contact Ground.

## 1. What Checklists Do

Checklists are organization-managed templates that can be assigned to resources.

Implemented checklist capabilities:
1. Create and manage checklist templates (`pre-flight` or `post-flight`).
2. Add, reorder, edit, and delete checklist items.
3. Assign one or more checklists to a resource.
4. Include assigned checklist items in flight-ops reminder emails for that resource.
5. Notify members when a checklist is newly assigned to a resource.
6. Notify members when an assigned checklist's contents change.

## 2. Access and Pages

### 2.1 Who can manage checklists
Checklist management requires an operations-capable role:
1. `owner`
2. `admin`
3. `operations`

### 2.2 Where to manage
1. Checklist templates: left sidebar `Checklists`
2. Resource assignments: left sidebar `Resources` -> open a resource -> edit

## 3. Creating and Updating Checklists

From `Checklists`:
1. Click `Create Checklist`.
2. Enter a name.
3. Choose `Pre-Flight` or `Post-Flight`.
4. Add checklist items.
5. Save.

For existing templates:
1. Use the edit action to update name, type, and items.
2. Use the delete action to remove a checklist template.

## 4. Assigning Checklists to Resources

From a resource edit page:
1. Open `Pre- and Post-flight Checklists`.
2. Select the checklists to attach.
3. Save resource changes.

Notes:
1. A resource can have multiple checklist templates assigned.
2. Assignments are organization-specific.

## 5. How Checklists Are Used Today

Current behavior in the product:
1. Assigned checklist items are included in pre-flight and post-flight reminder emails.
2. Checklist templates are managed centrally by operations/admin users.
3. When a checklist is newly assigned to a resource, members receive a checklist assignment notification.
4. If a checklist is assigned to at least one resource, content changes trigger a checklist update notification to other members in the organization.

Important:
1. Do not rely on an in-app "member checkbox completion" flow for checklists.
2. Use flight-ops reporting and squawk workflows for post-flight reporting/compliance.

## 6. Best Practices

1. Keep checklist names specific (for example, by aircraft type/model).
2. Keep items short, clear, and action-oriented.
3. Review checklist templates when procedures or equipment change.
4. Coordinate checklist updates with operations training.

## 7. Troubleshooting

### 7.1 Cannot access `Checklists`
Cause: your role does not include checklist-management permissions.

Action: ask an admin/owner to confirm your role.

### 7.2 Checklist is not showing in reminders
Possible causes:
1. No checklist is assigned to that resource.
2. Resource assignment was changed but not saved.

Action:
1. Re-open the resource and confirm checklist assignment.
2. Save and retry on the next reminder cycle.

## 8. Related Manuals

1. Resource setup and assignment:
   `docs/users/administration/RESOURCE_MANAGEMENT.md`
2. Flight operations workflow:
   `docs/users/operations/FLIGHT_OPERATIONS.md`
3. Maintenance and squawks:
   `docs/users/operations/MAINTENANCE.md`
