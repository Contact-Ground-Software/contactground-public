# Accounting Invoicing Playbook (QuickBooks Integration)

This guide is for accounting users who run billing in Contact Ground with `QuickBooks Integration` mode.

It covers:
- Flight operations data readiness
- QuickBooks connection and mapping requirements
- Invoice generation and send behavior
- Sync locks and correction workflow
- Payment tracking via QuickBooks

## 1. Before You Start

### 1.1 Access and prerequisites
You should have an invoicing-capable role in your organization (`owner` or `accounting`). `Admin` alone does not grant invoice, credits, or credit-request review access.

Invoicing works only when both conditions are true:
1. Flight Operations Mode is `Manual` or `Automatic` (not `Off`).
2. Invoicing is enabled in organization settings.

### 1.2 Where key pages are
- Organization settings: left sidebar `Organization`
- QuickBooks setup and mappings: on the `Organization` page, in the QuickBooks card click `Connect to QuickBooks`, then click `Configure Mappings`
- Flight Ops time entry management: left sidebar `Flight Ops`
- Credit requests queue: left sidebar `Credit Requests`
- Invoices list: left sidebar `Invoices`
- Generate invoices: on `Invoices`, click `Generate Invoice`
- Credits management: on `Invoices`, click `Manage Credits`

## 2. One-Time Setup Checklist

### 2.1 Flight operations and invoicing settings
Open `Organization` from the left sidebar and confirm:
1. Flight Operations Mode is `Manual` or `Automatic`.
2. `Enable Invoicing` is checked.
3. Invoicing Mode is `QuickBooks Integration`.
4. `Notify members about invoices` is set the way your organization wants.
5. `Monthly Member Rate` is correct.
6. Optional: schedule future monthly rate changes if needed.

### 2.2 Complete QuickBooks integration setup
From `Organization`, use the QuickBooks card buttons and complete:
1. Click `Connect to QuickBooks`.
2. After connection succeeds, click `Configure Mappings`.
3. Member to Customer Mapping:
   - Map every Contact Ground member that will be invoiced to a QuickBooks Online customer.
4. Line Item to Item Mapping:
   - Map Contact Ground line item types to QuickBooks Online items (`flight_time`, `monthly_fee`, `instructor_fee`, `other`).
5. Confirm connection is active and mappings are complete before month-end sends.

Important:
- Incomplete mapping is the most common reason for failed syncs.

## 3. Monthly Billing Runbook

### 3.1 Close flight data first
Before generating invoices:
1. Review recent entries on `Flight Ops`.
2. Ensure all post-flight hours are present for the billing period.
3. Correct missing or incorrect entries:
   - Edit existing entries, or
   - Use `Add Manual Entry` for missing flights.

### 3.2 Process credit requests
Open `Credit Requests`:
1. Start with `Pending` filter.
2. For each request:
   - `Approve`: optionally adjust approved amount and add notes.
   - `Deny`: enter required reason.
3. On approval, Contact Ground creates an active reimbursement credit for the member.

### 3.3 Review direct credits and credit memos
From `Invoices`, click `Manage Credits`:
1. Add one-time or monthly credits as needed.
2. Review existing active credits for accuracy.
3. Confirm expiration dates where applicable.

Notes:
- Credits are auto-applied to new invoices.
- Credits are applied oldest-first (FIFO).
- In QB mode, synced credits are locked until deleted in QuickBooks Online.

### 3.4 Generate draft invoices
From `Invoices`, click `Generate Invoice`:
1. Set billing period start and end.
2. Choose `All members` or selected members.
3. Generate invoices.
4. Contact Ground creates draft invoices and applies available credits automatically.

### 3.5 Review drafts before sending
Open `Invoices`:
1. `Draft` is the default filter.
2. Open each invoice detail to verify line items and credits.
3. Fix data issues before sending.

### 3.6 Send Behavior with QuickBooks
From `Invoices`, sending drafts starts in Contact Ground, then each invoice is automatically synced to QuickBooks Online.

What to expect:
- Individual invoices sync to QuickBooks Online automatically
- Large batches may take a minute or more to complete
- Members receive notification when an invoice is sent
- QuickBooks Online may apply adjustments after sync

## 4. QuickBooks Sync and Corrections

### 4.1 Understanding Synced Invoices
Once an invoice is synced to QuickBooks Online:
- The invoice is locked in Contact Ground
- You cannot edit or delete it directly in Contact Ground
- All changes must be made through the correction process

To unlock a synced invoice:
- Delete the invoice in QuickBooks Online
- The system will automatically unlock it in Contact Ground
- You can then edit and re-sync

### 4.2 Recording Payments
Payment status is managed through QuickBooks Online:
1. Record all payments in QuickBooks Online
2. Payment status automatically updates in Contact Ground
3. Invoice shows as paid when QuickBooks Online balance is zero

Note: In most cases, do not manually mark synced invoices as paid in Contact Ground. Let QuickBooks sync handle the status.

### 4.3 Correcting a Synced Invoice
If a synced invoice needs changes:
1. Delete the invoice in QuickBooks Online
2. Wait for the system to unlock it (usually immediate)
3. In Contact Ground, cancel and replace the invoice as needed
4. Correct underlying data (flight entries, credits)
5. Generate and send a new invoice.

### 4.4 Correct a synced credit memo
If a synced credit memo needs changes:
1. Delete the credit memo in QuickBooks Online.
    * Find the credit memo and go to Edit
    * On the bottom edge click More and then Delete.
2. Wait for webhook processing to unlock it in Contact Ground. Typically this occurs nearly immediately.
3. In `Invoices` -> `Manage Credits`, edit or delete the credit in Contact Ground.
4. After edit and approved/active, Contact Ground syncs updated values as a new QuickBooks Online credit memo.

## 5. Troubleshooting

### 5.1 "Already synced to QuickBooks" message
Meaning:
- Record is locked because it already synced.

Action:
1. Delete that invoice or credit memo in QuickBooks Online.
2. Wait for the data to sync up (~10 seconds).
3. Retry the adjustment and resend flow in Contact Ground.

### 5.2 "Sync already in progress" message
Meaning:
- A sync job is currently pending.

Action:
- Wait and retry after job completion.

### 5.3 Invoice or credit created in Contact Ground but not in QuickBooks Online
Common causes:
- Missing customer mapping
- Missing or incorrect item mapping
- QuickBooks Online connection or token issues

Action:
1. Open `Organization`, check the QuickBooks card connection status, then click `Configure Mappings`.
2. Verify member and item mappings.
3. Retry from an unlocked state.

### 5.4 Invoicing options disabled
Meaning:
- Flight ops mode is `Off`, or invoicing is disabled.

Action:
- Enable flight ops (`Manual` or `Automatic`) and invoicing in `Organization`.

## 6. Recommended Month-End Checklist

### 6.1 Pre-send checklist
1. Flight entries are complete for period.
2. Pending credit requests are resolved.
3. Credits table reviewed.
4. Draft invoices generated and spot-checked.
5. QuickBooks mappings and connection are healthy.

### 6.2 Send checklist
1. Send drafts from `Invoices` using `Send Draft Invoices`.
2. Confirm send summary (sent vs failed count).
3. Monitor for sync errors.

### 6.3 Post-send checklist
1. Record payments in QuickBooks Online.
2. Confirm webhook-driven paid status updates in Contact Ground.
