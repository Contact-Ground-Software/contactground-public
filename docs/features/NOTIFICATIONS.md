# Notifications

This manual explains how Contact Ground notifications are generated, delivered, and controlled.

## 1. Where Notifications Appear

### 1.1 Notification tray (top bar bell)
1. Shows notifications sorted from latest (at top) to earliest (at bottom).
2. Shows unread badge count.
3. Clicking a notification opens its linked page and marks it as read.

### 1.2 `Notifications` page
1. Open `/notifications` for full list view.
2. Filter by `All` or `Unread`.
3. Mark items as read manually.
4. Open each item's `View details` link to navigate to the relevant page.

### 1.3 Replying to an organization message
1. Organization message notifications (✉️) include a **Reply** button.
2. Click **Reply** to open the compose page where you can type and send a reply.
3. Your reply is recorded immediately. The original sender and original recipients are notified within the next notification cycle.
4. This lets members who opt out of email still participate in message threads.

## 2. How Notifications are Delivered

### 2.1 In-app
1. In-app delivery is always created for targeted recipients.
2. This means a notification can still appear in-app even if email/SMS/push methods are disabled.

### 2.2 Email
1. Sent only when `Email Notifications` is enabled on your profile.
2. Uses your account email address.
3. In-app notifications are still created even if email delivery fails.

### 2.3 SMS
SMS is sent only when all conditions are true:
1. Phone number exists on profile.
2. Phone number is verified.
3. The user accepts the SMS consent dialog when enabling SMS notifications.
4. `SMS Notifications` is checked.
5. SMS consent covers core platform notification types, including invoicing, organizational messaging, and flight operations alerts.
6. In-app notifications are still created even if SMS delivery fails.

Full disclosure: [`/policies/sms-consent.html`](/policies/sms-consent.html)

### 2.4 Push
1. The profile has a `Push Notifications` toggle. Push is sent when:
   - Push is enabled on profile.
   - The mobile app has registered an active device token.
   - APNs/FCM server credentials are configured correctly.
2. In-app notifications are still created even if push delivery fails.

## 3. Notification Categories

Category preferences are configured per organization in the profile `Notification Preferences` section:
1. Schedule updates
2. Weather changes
3. Instructor availability
4. Availability requests
5. News updates
6. Currency reminders
7. Preflight dispatch timing (lead time before a scheduled flight)

Other notification types can still be sent based on workflow and role, including:
1. Maintenance and squawk-related alerts
2. Organization messages and replies
3. Invoice notifications
4. Checklist assignment alerts when a checklist is newly attached to a resource
5. Checklist update alerts for assigned resources
6. Account/trial/system notices

`News Updates` controls notifications sent when a new entry is published in `News`. When available, email, push, and in-app links route directly to the exact news entry rather than just the top-level `News` page.

## 4. How To Configure Notifications

### 4.1 Configure delivery methods (account-level)
1. Go to `Profile`.
2. Set `Email Notifications`, `SMS Notifications`, and/or `Push Notifications`.
3. When enabling SMS notifications for the first time, accept the SMS consent dialog.
4. Click `Save` for method changes.

### 4.2 Configure category preferences (organization-level)
1. In `Profile`, open the `Notification Preferences` card.
2. Toggle categories on/off.
3. Choose your preflight dispatch lead time when available.
4. Category changes save immediately.
5. These settings apply to your current active organization only.

### 4.3 Configure preflight dispatch timing
Members can choose:
1. `At event time`
2. `15 minutes before`
3. `30 minutes before`
4. `45 minutes before`
5. `1 hour before`

Notes:
1. The default is `30 minutes before`.
2. This applies only when the organization is using `Automatic` flight operations mode.
3. If a flight is created after its ideal reminder time, Contact Ground still sends one catch-up preflight reminder while the event is still upcoming.

## 5. Troubleshooting

### 5.1 I am not receiving notifications
1. Check `/notifications` or the Notification tray (top bar bell) first to confirm in-app creation.
2. Confirm the relevant category is enabled for your active organization.
3. Confirm your delivery method (email/SMS) is enabled in profile.
4. For preflight dispatch reminders, confirm the organization is in `Automatic` flight operations mode.
5. For News alerts, confirm `News Updates` is enabled in `Notification Preferences`.
6. For checklist assignment alerts, confirm the checklist was newly added to the resource instead of already assigned.
7. For checklist update alerts, confirm the checklist is assigned to at least one resource. Unassigned checklist edits do not notify members.

Note:
If you change or assign a checklist, you yourself do not receive the notification.

### 5.2 SMS is not being delivered
1. Verify phone number status in profile.
2. Confirm SMS consent was accepted when enabling SMS notifications.
3. Confirm `SMS Notifications` is enabled.
4. Confirm your phone number is entered in valid international format.

Note:
SMS notifications can only be configured through the web site.

### 5.3 Email is not being delivered
1. Confirm `Email Notifications` is enabled.
2. Check spam/junk/quarantine.
3. Confirm your account email is correct.

### 5.4 Push notifications are not arriving
1. Confirm `Push Notifications` is enabled in profile.
2. Confirm the mobile app has registered a push token (sign in again if needed).
