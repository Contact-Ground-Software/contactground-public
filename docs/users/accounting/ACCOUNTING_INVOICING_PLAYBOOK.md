# Accounting Invoicing Playbook (Manual Invoicing)

This guide is for accounting users who run billing in Contact Ground with `Manual Invoicing` mode.

It covers:
- Flight operations data readiness
- Credit requests and credits
- Invoice generation and sending
- Payment tracking in Contact Ground
- Post-send corrections

## 1. Before You Start

### 1.1 Access and prerequisites
You should have an invoicing-capable role in your organization (`owner` or `accounting`). `Admin` alone does not grant invoice, credits, or credit-request review access.

Invoicing works only when both conditions are true:
1. Flight Operations Mode is `Manual` or `Automatic` (not `Off`).
2. Invoicing is enabled in organization settings.

### 1.2 Where key pages are
- Organization settings: left sidebar `Organization`
- Flight Ops time entry management: left sidebar `Flight Ops`
- Credit requests queue: left sidebar `Credit Requests`
- Submit credit request (member-facing): on `Credit Requests`, click `New Request`, then submit with `Submit Request`
- Invoices list: left sidebar `Invoices`
- Generate invoices: on `Invoices`, click `Generate Invoice`
- Credits management: on `Invoices`, click `Manage Credits`

## 2. One-Time Setup Checklist

Open `Organization` from the left sidebar and confirm:
1. Flight Operations Mode is `Manual` or `Automatic`.
2. `Enable Invoicing` is checked.
3. Invoicing Mode is `Manual Invoicing`.
4. `Notify members about invoices` is set the way your organization wants.
5. `Monthly Member Rate` is correct.
6. Optional: schedule future monthly rate changes if needed.

## 3. Monthly Billing Runbook

### 3.1 Close flight data first
Before generating invoices:
1. Review recent entries on `Flight Ops`.
2. Ensure all post-flight hours are present for the billing period.
3. Correct missing or incorrect entries:
   - Edit existing entries, or
   - Use `Add Manual Entry` for missing flights.

How flight ops mode affects this:
- `Manual` mode: operations team manually ensures entries are created and complete.
- `Automatic` mode: Contact Ground sends reminders and dispatch prompts, including notifications to Operations team when members do not comply in a timely manner. Accounting team should always do a final completeness review.

### 3.2 Process credit requests
Open `Credit Requests`:
1. Start with `Pending` filter.
2. For each request:
   - `Approve`: optionally adjust approved amount and add notes.
   - `Deny`: enter required reason.
3. On approval, Contact Ground creates an active reimbursement credit for the member.

### 3.3 Review direct credits
From `Invoices`, click `Manage Credits`:
1. Add one-time or monthly credits as needed.
2. Review existing active credits for accuracy.
3. Confirm expiration dates where applicable.

Notes:
- Credits are auto-applied to new invoices.
- Credits are applied oldest-first (FIFO).
- Active credits can be edited or deleted.

### 3.4 Generate draft invoices
From `Invoices`, click `Generate Invoice`:
1. Set billing period start and end.
2. Choose `All members` or selected members.
3. Generate invoices.
4. Contact Ground creates draft invoices and applies available credits automatically.

What Contact Ground includes:
- Monthly membership fee (if configured)
- Flight hours in the period
- Resource hourly rates
- Auto-applied credits

### 3.5 Review drafts before sending
Open `Invoices`:
1. `Draft` is the default filter.
2. Open each invoice detail to verify line items and credits.
3. Fix data issues before sending.


### 3.6 Send invoices
From `Invoices`:
1. While viewing invoice details, send a single invoice with `Send Invoice`, or
2. Send all drafts with `Send Draft Invoices`.

Contact Ground behavior:
- Marks sent invoices as `Sent`.
- Sends member notification with invoice details, amounts, and a direct invoice link (if notifications enabled).

### 3.7 Download invoice PDF
In manual mode, invoices can be downloaded as PDF:
1. From `Invoices`, click `Export PDF` on the invoice row, or
2. Open invoice details and click `Export PDF`.

## 4. Payments and Corrections (Manual Mode)

### 4.1 Track payments in Contact Ground
From `Invoices` or an invoice detail page:
1. `Mark Paid` when payment is received.
2. `Cancel Invoice` if invoice must be voided in Contact Ground.

### 4.2 Correct an invoice after sending
If an invoice is wrong after sending:
1. Cancel the incorrect invoice in Contact Ground.
2. Fix underlying flight data and credits as needed.
3. Generate a new invoice for that member and period.
4. Send the corrected invoice.

## 5. Credit Requests and Credits End-to-End

### 5.1 Credit Requested from Members
Members submit requests from `Credit Requests` by clicking `New Request`, then `Submit Request`, with:
- Amount
- Description
- Receipt image (required)
- Optional associated flight

### 5.2 Accounting review
In `Credit Requests`:
1. Review receipt and details.
2. Approve or deny.
3. Include notes (required for denial).

### 5.3 On approval
Contact Ground creates a member credit with type `reimbursement`.
- In manual mode, credit remains in Contact Ground and applies to invoices.

### 5.4 Active credit rules
- Only active credits can be edited.
- Active credits can be deleted if no longer needed.

## 6. Troubleshooting

### 6.1 Invoicing options disabled
Meaning:
- Flight ops mode is `Off`, or invoicing is disabled.

Action:
- Enable flight ops (`Manual` or `Automatic`) and invoicing in `Organization`.

### 6.2 Incorrect invoice totals
Common causes:
- Missing or late flight entries
- Incorrect hourly rate setup
- Unexpected credit application

Action:
1. Validate flight entries for the period.
2. Validate resource rates and monthly member settings.
3. Review active credits in `Manage Credits`.
4. Cancel and regenerate invoice if needed.

## 7. Recommended Month-End Checklist

### 7.1 Pre-send checklist
1. Flight entries are complete for period.
2. Pending credit requests are resolved.
3. Credits table reviewed.
4. Draft invoices generated and spot-checked.

### 7.2 Send checklist
1. Send drafts from `Invoices` using `Send Draft Invoices`.
2. Confirm send summary count.

### 7.3 Post-send checklist
1. Track incoming payments.
2. Mark invoices paid in Contact Ground.
