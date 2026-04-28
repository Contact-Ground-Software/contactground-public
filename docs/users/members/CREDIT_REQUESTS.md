# Credit Requests

This manual explains how members submit credit requests and how accounting staff review and process them.

A credit request is a formal submission asking your organization to reimburse an expense you paid on the organization's behalf—typically fuel, oil, or supplies you purchased for an aircraft.

## 1. Before You Start

### 1.1 Access
All members can submit and track their own credit requests. Accounting-capable roles (`owner` or `accounting`) can review and approve or deny organization requests. `Admin` alone does not grant finance review access.

### 1.2 Where key pages are
- Submit a new request: left sidebar `Credit Requests` → `New Request`
- View your requests: left sidebar `Credit Requests`
- Review requests (accounting): left sidebar `Credit Requests` (shows all organization requests)

## 2. Submitting a Credit Request (Members)

### 2.1 When to submit a credit request
Submit a credit request when you paid for an organization expense out of pocket, such as:
- Fuel purchased during a flight
- Oil or supplies you added to an aircraft
- Other approved reimbursable expenses

Always check with your organization about what expenses qualify before purchasing.

### 2.2 How to submit

1. Navigate to `Credit Requests` from the left sidebar.
2. Click `New Request`.
3. Complete the form:
   - `Amount`: The dollar amount you are requesting.
   - `Description`: A clear description of what the expense was and why it qualifies (for example, "10 gallons 100LL at OXR during cross-country on 2/15").
   - `Receipt Image`: Upload a photo or scan of your receipt. **This is required.**
   - `Associated Flight` (optional): Link the request to a specific flight if the expense was for that flight.
4. Click `Submit Request`.

### 2.3 What happens after you submit
1. Your request moves to `Pending` status.
2. Your accounting team receives notification and reviews the request.
3. You will be notified when the request is approved or denied.
4. If approved, the credit appears on your next invoice automatically.

### 2.4 Tips for getting approved quickly
- Submit requests promptly after the expense (same day or next day).
- Upload a clear, readable receipt image.
- Write a detailed description so the reviewer understands what was purchased and why.
- Match the amount on your receipt exactly.
- Link the request to the associated flight when applicable.

## 3. Tracking Your Credit Requests

Open `Credit Requests` from the sidebar to view your submitted requests.

Each request shows:
- Amount requested
- Description
- Status (`Pending`, `Approved`, or `Denied`)
- Submission date
- Review date and reviewer notes (once reviewed)
- Approved amount (if different from requested)

Click `View Receipt` on any request to see the receipt image you submitted.

### 3.1 Request statuses

| Status | Meaning |
|--------|---------|
| `Pending` | Submitted and awaiting accounting review |
| `Approved` | Approved and credit added to your account |
| `Denied` | Not approved; see reviewer notes for reason |

### 3.2 How approved credits apply to invoices
- Approved credits are added to your account automatically.
- Credits are applied to your next invoice when it is generated.
- Credits are applied oldest-first. If you have multiple credits, the earliest one is used first.
- Applied credits appear as a line item on your invoice.

## 4. Reviewing Credit Requests (Accounting Staff)

### 4.1 Access
You need a credit-management role to approve or deny requests (`owner` or `accounting`).

### 4.2 Finding pending requests
1. Open `Credit Requests` from the sidebar.
2. The default view shows `Pending` requests.
3. Use the filter buttons (`Pending`, `Approved`, `Denied`, `All`) to switch views.

### 4.3 Reviewing a request
For each pending request, you can:
- View the member's description.
- Click `View Receipt` to open the receipt image.
- See the requested amount.

### 4.4 Approving a request
1. Click `Approve` on a pending request.
2. In the approval dialog:
   - Review the requested amount.
   - Adjust the `Approved Amount` if the actual reimbursable amount differs from what was requested (for example, your organization only reimburses up to a certain fuel price).
   - Optionally add review notes.
3. Click `Approve Request`.

On approval, Contact Ground creates a `reimbursement` credit for the member. The credit is automatically applied to their next invoice.

### 4.5 Denying a request
1. Click `Deny` on a pending request.
2. Enter a clear reason in the `Reason for Denial` field. **This is required.**
3. Click `Deny Request`.

The member receives notification of the denial including your reason. Denial does not add any credit to the member's account.

### 4.6 Best practices for accounting staff
1. Review requests promptly, ideally within a few days of submission.
2. Always view the receipt before approving.
3. Provide clear denial reasons so members understand what went wrong.
4. Process pending requests before generating invoices each month.
5. Use the `Pending` filter as your daily working queue.

## 5. How Credits Appear on Invoices

When an invoice is generated for a member, all active credits are applied automatically:
- Credits reduce the invoice total.
- Each applied credit appears as a line item.
- Credits are applied oldest-first until the invoice balance reaches zero or credits are exhausted.

If credits exceed the invoice total, the remaining credit balance carries forward to future invoices.

## 6. Troubleshooting

### 6.1 Cannot submit a credit request
Possible causes:
1. Receipt image not uploaded.
2. Amount is missing or invalid.
3. Description is missing.

Action: Confirm all required fields are complete. The receipt image is required—no receipt means the request cannot be submitted.

### 6.2 Credit request was approved but credit not showing on invoice
Possible causes:
1. The invoice was generated before the request was approved.
2. The credit was applied to a different invoice.

Action:
1. Check your invoice line items for an applied credit.
2. Contact accounting to confirm credit status and ask them to check `Invoices` → `Manage Credits`.

### 6.3 Approved amount differs from requested amount
Your accounting team may adjust the amount to match your organization's reimbursement policy. The approval notification and request detail show the approved amount. Contact accounting if you believe the adjustment was incorrect.

### 6.4 Did not receive notification of approval or denial
Possible causes:
1. Notification delivery method is disabled.
2. Email went to spam folder.

Action:
1. Check `Profile` → `Notification Methods` to confirm notifications are enabled.
2. Check your spam or junk folder.
3. On mobile, approval and denial notifications open the in-app `Credit Requests` screen.

## 7. Related Manuals

1. Invoicing and billing:
   `docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK.md`
2. Member profile and notifications:
   `docs/users/members/MEMBER_PROFILE.md`
3. Pilot scheduling guide (includes credit request summary):
   `docs/users/members/PILOT_SCHEDULING_GUIDE.md`
