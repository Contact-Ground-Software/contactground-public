# Documents

The Documents module gives an organization a controlled place to store club files, required reading, and member-provided uploads. It is enabled per organization and appears in the app when document management is turned on.

## What the module supports

### Club documents

Club documents are reference files managed by administrators. They can be organization-wide or linked to a specific resource.

Common examples include:

- Operating rules
- Aircraft check-out packets
- Insurance summaries
- Hangar or airport procedures
- Resource-specific reference material

Members can open current club documents from the Documents page.

### Required reading

Required reading documents are club-managed files that members must review and agree to. Each uploaded version is immutable, and member agreement is tied to the active version.

When a required-reading document is updated, members need to accept the new current version.

### Required member documents

Administrators can define document requirements that members must upload. Requirements may be organization-wide or resource-specific.

Examples include:

- TSA badge
- Insurance acknowledgement
- Medical or training record copy
- Signed club waiver
- Airport access document

Requirements can be configured with expiration dates. Expired submissions return to an expired status until the member uploads a replacement and it is approved.

### Personal member documents

Members can upload personal documents for their own records. Personal member documents are visible only to the uploading member and authorized administrators where required by the workflow.

## Review and approval workflow

Required member documents use an approval workflow:

1. An administrator creates the requirement.
2. A member uploads a file, optionally with an expiration date.
3. Administrators review the submission.
4. The submission is approved, disapproved, or returned to pending.
5. Approved submissions show who approved them and when.

The review table shows document type, member, status, expiration date, view action, approval actions, approver, and approval time.

## Booking enforcement

Administrators can mark a required member document as booking-enforced. Enforced missing, rejected, pending, or expired submissions can prevent booking where the requirement applies.

Resource-linked requirements apply to the linked resource. Organization-wide requirements apply across the organization.

## File handling

Supported uploads include PDF and common image formats. Current public behavior supports:

- PDF
- PNG
- JPEG
- WebP

Administrators can archive outdated documents or upload replacement versions where the document type supports versioning.

## Related guides

- [Documents User Guide](/docs/users/administration/DOCUMENTS.md)
- [Administration](/docs/users/administration/ADMINISTRATION.md)
- [Pilot Scheduling Guide](/docs/users/members/PILOT_SCHEDULING_GUIDE.md)
