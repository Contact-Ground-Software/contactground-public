# Endorsements

This manual describes the implemented endorsement model in Contact Ground.

## 1. What Endorsements Control

Endorsements are qualification records used by the app to:
1. Restrict resource booking when resources require endorsements.
2. Grant selected non-scheduling permissions (for example, `Blog` posting access).

## 2. Member Experience

Members can view endorsements in `People` on their member card/profile.

During scheduling, endorsement checks are applied by booking logic. If required endorsements are missing, booking may be unavailable or fail validation depending on the scheduling flow.

## 3. Admin Experience

Admins/leadership manage endorsement types through the `Organization` page. Endorsements are assigned to members via the `People` page.

Typical actions:
1. Create or edit endorsement types.
2. Assign/remove endorsements on member records.
3. Configure resource endorsement requirements.

## 4. Resource Requirements

When a resource is configured with required endorsements:
1. Members must satisfy all required endorsements to book.
2. Changing endorsement assignments takes effect immediately for booking checks.

## 5. Blog Endorsement

`Blog` endorsement can be used to allow standard members to create/edit their own entries in `News` without granting admin roles.

## 6. Best Practices

1. Use standardized endorsement names.
2. Update endorsements as part of checkout/training completion.
3. Review assignments regularly.
