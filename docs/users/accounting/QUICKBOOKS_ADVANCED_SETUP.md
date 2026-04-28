# QuickBooks Advanced Setup

This manual explains how to complete QuickBooks Online integration configuration in Contact Ground, including customer mappings, item mappings, and custom field setup.

This guide supplements the main QuickBooks invoicing workflow:
`docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK_QUICKBOOKS.md`

## 1. Before You Start

### 1.1 Access and prerequisites
You need an owner or admin role to configure QuickBooks integration.

Complete these steps before mapping:
1. Confirm QuickBooks integration mode is selected in `Organization` → invoicing settings.
2. Connect your QuickBooks Online account using `Connect to QuickBooks` in the organization settings.
3. Confirm the connection is active before attempting to map customers or items.

### 1.2 Where key pages are
- QuickBooks configuration: `Organization` → QuickBooks card → `Configure Mappings`
- Connection status: `Organization` → QuickBooks connection card

## 2. Connecting to QuickBooks Online

1. Open `Organization` from the sidebar.
2. In the QuickBooks card, click `Connect to QuickBooks`.
3. You will be redirected to QuickBooks Online to authorize the connection.
4. After authorization, you are returned to Contact Ground.
5. The QuickBooks card displays the connection status.

**Important:** The connection uses OAuth tokens. If the connection becomes stale or you revoke access in QuickBooks, you must reconnect.

## 3. Member to Customer Mapping

Every Contact Ground member who will receive invoices must be mapped to a matching QuickBooks Online customer. Unmapped members cannot have their invoices synchronized to QuickBooks.

### 3.1 Opening the mapping page
1. Open `Organization`.
2. In the QuickBooks card, click `Configure Mappings`.
3. Select the `Member to Customer Mapping` section.

### 3.2 Mapping a member
1. Find the Contact Ground member in the table.
2. In the `QuickBooks Customer` column, select the matching QuickBooks Online customer from the dropdown.
3. Click `Save Mapping`.
4. The row status updates to `Mapped`.

Members with a `Mapped` status are ready for invoice sync. Members with `Not Mapped` status will be skipped during sync and their invoices will not transfer to QuickBooks.

### 3.3 Changing a mapping
1. Find the mapped member in the table.
2. Click `Change`.
3. Select the correct QuickBooks Online customer.
4. Click `Update Mapping`.

### 3.4 Removing a mapping
1. Find the mapped member in the table.
2. Click `Remove`.

The member's invoices will no longer sync to QuickBooks after the mapping is removed.

### 3.5 Mapping rules
- Each Contact Ground member can be mapped to only one QuickBooks customer.
- Each QuickBooks customer can be mapped to only one Contact Ground member.
- Customers already mapped to another member are marked `(already mapped)` in the dropdown and cannot be selected.

### 3.6 When there are no QuickBooks customers in the dropdown
This means your QuickBooks Online account does not have customers yet, or the connection is stale.

Action:
1. Confirm your QuickBooks connection is active.
2. Verify that customers exist in your QuickBooks Online account.
3. Use the `Refresh` button to reload the customer list.
4. Reconnect to QuickBooks if needed.

## 4. Line Item to Item Mapping

Contact Ground generates invoices with four line item types. Each type must be mapped to a corresponding QuickBooks Online item so revenue is categorized correctly in your chart of accounts.

### 4.1 The four line item types

| Contact Ground Line Type | Label | What it represents |
|------------------------|-------|-------------------|
| `flight_time` | Flight Time (Hourly) | Aircraft usage billed by the hour |
| `monthly_fee` | Monthly Membership Fee | Recurring monthly member charge |
| `instructor_fee` | Instructor Fee | Instructor service charges |
| `other` | Other Charges | Any miscellaneous charges |

### 4.2 Setting up item mappings

1. Open `Organization` → QuickBooks card → `Configure Mappings`.
2. Select the `Line Item to Item Mapping` section.
3. For each line item type:
   - Select the matching QuickBooks Online item from the dropdown.
   - Click `Save Mapping`.
4. Repeat for all four line types.

All four line types should be mapped before syncing invoices. If a line type that appears on an invoice is not mapped, that line may fail to sync.

### 4.3 Choosing the right QuickBooks items
Match each line type to an appropriate Service or Non-Inventory item in QuickBooks:

1. **flight_time** → A service item representing aircraft rental or flight time (for example, "Airplane Rental").
2. **monthly_fee** → A service item representing monthly dues (for example, "Club Dues").
3. **instructor_fee** → A service item representing instruction (for example, "Flight Instruction").
4. **other** → A catch-all service item for miscellaneous charges.

If you don't have these items in QuickBooks yet, create them in QuickBooks Online first, then return to Contact Ground to complete the mapping.

### 4.4 Changing an item mapping
1. Find the line type in the table.
2. Click `Change`.
3. Select the new QuickBooks item.
4. Click `Update Mapping`.

## 5. Custom Field Configuration

If your QuickBooks Online account uses custom fields on invoices, Contact Ground may support mapping those fields.

For custom field configuration, open `Organization` → QuickBooks card → `Custom Fields`. The options available depend on your QuickBooks Online subscription and your organization's configuration.

## 6. Verifying Your Configuration

Before your first invoice sync, verify:
- [ ] QuickBooks connection is active (green status in organization settings)
- [ ] All members who will be invoiced are mapped to QuickBooks customers
- [ ] All four line item types are mapped to QuickBooks items
- [ ] QuickBooks items exist in your chart of accounts and are the correct type (Service or Non-Inventory)

## 7. Troubleshooting

### 7.1 Invoices created in Contact Ground but not appearing in QuickBooks
Common causes:
1. Member is not mapped to a QuickBooks customer.
2. A required line item type is not mapped to a QuickBooks item.
3. QuickBooks connection is stale or disconnected.

Action:
1. Open `Organization` → QuickBooks card. Check connection status.
2. Open `Configure Mappings` and verify member and item mappings are complete.
3. Reconnect to QuickBooks if connection status shows an error.
4. Retry the invoice sync from an unlocked state.

### 7.2 "Already synced to QuickBooks" message
The invoice or credit is locked because it has already been synced. To make changes:
1. Delete the invoice or credit memo in QuickBooks Online.
2. Wait for the system to unlock it in Contact Ground (usually immediate).
3. Make your corrections and resend.

### 7.3 No QuickBooks customers or items appear in dropdowns
Possible causes:
1. QuickBooks connection is not active.
2. The QuickBooks Online account has no customers or items.

Action:
1. Confirm connection status in `Organization`.
2. Add customers and items in QuickBooks Online if they don't exist.
3. Use the `Refresh` button to reload the data.
4. Reconnect to QuickBooks if needed.

### 7.4 QuickBooks customer is greyed out with "(already mapped)"
A customer can only be mapped to one Contact Ground member. If you see this, another member is already using that QuickBooks customer.

Action:
1. Remove the existing mapping if it is incorrect.
2. Create a new customer in QuickBooks Online for this member if needed.

## 8. Related Manuals

1. QuickBooks invoicing workflow:
   `docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK_QUICKBOOKS.md`
2. Manual invoicing (alternative to QuickBooks):
   `docs/users/accounting/ACCOUNTING_INVOICING_PLAYBOOK.md`
3. Organization settings:
   `docs/users/administration/ADMINISTRATION.md`
