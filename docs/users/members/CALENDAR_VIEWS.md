# Calendar Views and Filters

This manual explains the different calendar views in Contact Ground, how to filter by resource, how to navigate dates, and how to subscribe to your calendar in external applications.

## 1. Opening the Calendar

Open `Calendar` from the left sidebar. The calendar is your primary tool for viewing and creating reservations.

## 2. Calendar Views

Contact Ground provides three calendar views. Switch between them using the view selector in the calendar header.

### 2.1 Day View

Shows a single day as a vertical timeline with time slots from early morning to late evening.

**Best for:**
- Reviewing detailed scheduling for one specific day
- Making reservations when you know your exact date and time
- Checking what a day looks like before adding a booking

**How to use:**
- Each vertical lane represents a scheduled event
- Click an open time slot to start a new reservation
- Use the left and right arrow buttons to navigate to the previous or next day
- Click `Today` to jump back to the current day

### 2.2 Week View

Shows a full seven-day week with time slots across all days.

**Best for:**
- Planning several days ahead
- Finding open time across the week
- Comparing availability across multiple days at a glance

**How to use:**
- Days are shown as columns
- Events are displayed as blocks in the appropriate day and time slot
- Click an open slot to start a reservation
- Use the arrows to navigate to the previous or next week
- Click `Today` to return to the current week

### 2.3 Resource View

Shows all resources (aircraft/equipment) side by side for the current day.

**Best for:**
- Dispatchers and operations staff monitoring daily fleet activity
- Quickly seeing which resources are booked and which are available
- Identifying open aircraft when a member calls in with a question
- Viewing instructor availability alongside resource schedules

**How to use:**
- Each resource appears as a column
- Events are shown in the corresponding resource column
- Scroll left and right if more resources exist than fit on screen
- Use the date navigation arrows to move between days

## 3. Switching Between Views

On desktop, use the view selector dropdown in the upper right of the calendar header:
- `Day view`
- `Week view`
- `Resource view`

On mobile, use the compact view switcher (shows abbreviated view name) to switch between views.

## 4. Filtering by Resource

The calendar header includes a resource filter that limits the calendar to show only events for selected resources.

### 4.1 How to filter
1. Open `Calendar`.
2. Use the resource filter control in the header (typically a combobox or dropdown).
3. Select one or more resources to filter the view.
4. The calendar updates to show only events for those resources.

### 4.2 Clearing the filter
Remove the selected resource from the filter to return to the full calendar showing all resources.

## 5. Showing Instructor Availability

If your organization has `Availability Event Type` enabled:
1. A `Show Availability` toggle button appears in the calendar header.
2. Click it to show or hide instructor availability blocks alongside regular events.
3. When active, the button shows a checkmark and changes color.

Availability blocks show when instructors are available for training requests. Click a block to submit an availability request.

## 6. Navigating Dates

| Control | Action |
|---------|--------|
| Left arrow | Previous day (day view) or previous week (week view) |
| Right arrow | Next day or next week |
| `Today` button | Jump to current date |

## 7. Creating Events from the Calendar

Click any open time slot on the calendar to open the event creation dialog. See:
`docs/users/members/PILOT_SCHEDULING_GUIDE.md`

## 8. Event Types on the Calendar

Events are color-coded and labeled by type:
- **Flight** – Standard pilot flight booking
- **Training** – Instructional flight with an instructor
- **Maintenance** – Maintenance event (operations staff only)
- **Availability** – Instructor availability block (when availability is enabled)

## 9. Reading Event Cards

Each event card on the calendar shows:
- Event title or member name
- Start and end time
- Resource name (in views that show multiple resources)
- Event type

Click an event to open its details, including options to edit or delete (if you have permission).

On mobile:
- Event start and end selectors use 30-minute increments to match the web calendar.
- Past or completed events open as read-only unless you are an organization owner or admin.
- In-progress events can still be edited, but non-admin users cannot move the end time earlier than the current time.

## 10. Calendar Subscription (External Calendar Sync)

You can sync your Contact Ground reservations to an external calendar application using iCal.

### 10.1 Getting your iCal link
1. Open `Profile` from the sidebar.
2. Scroll to `Calendar Subscription`.
3. Copy the iCal URL shown.

### 10.2 Adding to your calendar app

**Apple Calendar:**
1. Open Calendar → File → New Calendar Subscription.
2. Paste the iCal URL and click Subscribe.
3. Configure refresh frequency (every hour recommended).

**Google Calendar:**
1. Open Google Calendar settings.
2. Select `Add calendar` → `From URL`.
3. Paste the iCal URL and click `Add calendar`.

**Outlook:**
1. Open Outlook → Calendar → Add calendar → Subscribe from web.
2. Paste the iCal URL.

**Note:** External calendar apps refresh on their own schedule (typically every few hours). Real-time changes in Contact Ground may not appear immediately in your external app.

### 10.3 What is included in the feed
- Your upcoming reservations
- Event titles, times, and resource names

The iCal URL is private. Do not share it publicly.

## 11. Printing and Exporting

Contact Ground does not have a built-in print or PDF export for the calendar view. To create a printable calendar:
1. Use your browser's print function while the calendar is open.
2. Adjust print settings for landscape orientation and scale if needed.

For a formatted list of upcoming events, use `Reports` → `Bookings` for a structured view that prints more cleanly.

## 12. Troubleshooting

### 12.1 Events not appearing on calendar
Possible causes:
1. Resource filter is set, hiding events for other resources.
2. You are looking at the wrong date.
3. Show Availability is off and you are looking for an availability block.

Action:
1. Clear the resource filter.
2. Confirm you are on the correct date.
3. Toggle `Show Availability` if looking for instructor availability.

### 12.2 Cannot create an event
Possible causes:
1. The time slot is already taken by another booking.
2. You are missing required endorsements or currency.
3. The resource is unavailable or in maintenance.

Action:
1. Try a different time slot or resource.
2. Check your endorsements and currency in `Profile`.
3. Verify resource status in `Resource`.

### 12.3 iCal feed not updating in external app
Cause: External apps refresh on their own schedule.
Action: Manually refresh or sync the calendar subscription in your calendar app. Check your app's settings for subscription refresh frequency.

## 13. Related Manuals

1. Making and managing reservations:
   `docs/users/members/PILOT_SCHEDULING_GUIDE.md`
2. Instructor availability requests:
   `docs/users/instructors/AVAILABILITY_REQUESTS.md`
3. Calendar subscription (in profile):
   `docs/users/members/MEMBER_PROFILE.md`
4. Flight operations board for operations:
   `docs/users/operations/FLIGHT_OPERATIONS.md`
