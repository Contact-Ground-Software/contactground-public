# Member Profile and Personal Settings

This guide documents the profile features that are implemented in Contact Ground.

## 1. Profile Sections

Open `Profile` from the sidebar. Main sections:
1. `Profile` (name, email, phone)
2. `Notification Methods`
3. `Notification Preferences`
4. `Currency Tracking`
5. `Calendar Subscription`
6. `Delete Account` (danger zone at the bottom)

## 2. Personal Information

### 2.1 Name
1. Update first and last name.
2. Click `Save`.

### 2.2 Email
1. Email is shown as your account identifier.
2. Use `Verify Email` / `Resend Email` to send verification.

### 2.3 Phone
1. Enter your number.
2. Click `Verify Phone`.
3. Enter OTP and confirm.

SMS notifications are enabled only after phone verification.
SMS notifications also require explicit SMS consent.

## 3. Notification Methods

In `Notification Methods`, you can enable/disable:
1. Email notifications
2. SMS notifications
3. Push notifications

These method toggles are saved with the profile form (`Save`).

## 4. Notification Preferences (By Category)

Category preferences are organization-specific and are updated in the `Notification Preferences` section.

Common categories:
1. Schedule updates
2. Weather changes
3. Instructor availability
4. Availability requests
5. Currency reminders
6. Preflight dispatch timing

Category toggles save immediately.

### 4.1 Preflight dispatch timing

Members can choose when to receive their preflight dispatch reminder:
1. At event time
2. 15 minutes before
3. 30 minutes before
4. 45 minutes before
5. 1 hour before

Important:
1. The default is `30 minutes before`.
2. This setting is organization-specific.
3. It only affects organizations using `Automatic` flight operations mode.

## 5. Currency Tracking

`Currency Tracking` on profile shows your current reminder items and expiration dates.

Depending on organization setup, you may:
1. Update expiration dates for organization-level reminder types.
2. Create personal reminder types.
3. Delete personal reminder types.

If your org enforces a reminder type, expired status can block booking until updated.

## 6. Calendar Subscription

`Calendar Subscription` provides private `webcal://` and `https://` feed URLs.

You can:
1. Copy the subscription URL.
2. Add it to Apple/Google/Outlook.
3. Regenerate the token (invalidates old links).

## 7. Delete Account and User Data

You can self-serve account deletion directly in the app.

Where to find it:
1. Web: open `Profile`, then scroll to the bottom `Delete Account` section.
2. Mobile: open `Settings`, then scroll to the bottom `Delete Account` section.

Deletion flow:
1. Read the warning text in the danger zone.
2. Check the acknowledgement confirming you understand the deletion and retention notice.
3. Type `DELETE`.
4. Confirm the final `Delete Account` prompt.

After confirmation:
1. Your active sessions are revoked and you are signed out.
2. Login credentials and authentication methods are removed.
3. Personal identifiers are deleted or anonymized.
4. Certain records may be retained in anonymized form for legal, tax, or aviation-compliance requirements.

If you cannot complete self-service deletion, contact support: `support@contactground.com`.

## 8. Related Member Data

From sidebar pages:
1. `Invoices` - billing history/status
2. `Credit Requests` - reimbursement request status
3. `People` - view your endorsement badges on your member card

## 9. Troubleshooting

### 9.1 SMS toggle is disabled
Cause: phone not verified.

Action:
1. Verify phone first.
2. Enable `SMS Notifications` and accept the consent dialog.

### 9.2 Not receiving notifications
Check:
1. At least one notification method is enabled.
2. Relevant category preference is enabled.
3. Email verification/spam folder for email delivery.
4. For preflight dispatch reminders, confirm your organization is using `Automatic` flight operations mode.

### 9.3 Currency section missing
Cause: organization disabled currency reminders.

Action: ask an admin/owner to confirm organization settings.

### 9.4 Delete button is disabled
Check:
1. The acknowledgement checkbox is selected.
2. You typed `DELETE` exactly.
3. Your session is still active.

Action:
1. Re-authenticate if prompted.
2. Retry from the bottom `Delete Account` section.
3. Contact `support@contactground.com` if it still fails.

## 10. Related Manuals

1. Notification preferences:
   `docs/users/members/MEMBER_NOTIFICATION_PREFERENCES.md`
2. Currency reminders:
   `docs/features/CURRENCY_REMINDERS.md`
3. Endorsements:
   `docs/users/members/ENDORSEMENTS_AND_QUALIFICATIONS.md`
4. Privacy statement:
   `www/public/privacy.html`
