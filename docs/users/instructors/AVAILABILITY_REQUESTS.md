# Availability Requests

This manual explains how members submit availability requests to instructors and how instructors respond.

Availability requests are how members ask an instructor or DPE to schedule time with them. The workflow connects member scheduling needs to instructor-published availability without requiring back-and-forth outside the platform.

## 1. Before You Start

### 1.1 Prerequisites
The availability request workflow requires that your organization has `Availability Event Type` enabled in `Organization` settings. If this is not enabled, instructors cannot publish availability blocks and members cannot submit requests.

### 1.2 Where key pages are
- Calendar (view availability, submit requests): left sidebar `Calendar`
- Notification inbox: left sidebar `Notifications`
- Availability responses (for instructors): `Calendar` → open an availability event → respond

## 2. How the Workflow Works

1. An instructor publishes an availability block on the calendar.
2. A member views the availability block on the calendar.
3. The member submits a request with their purpose and desired time.
4. The instructor receives a notification and reviews the request.
5. The instructor accepts or declines.
6. On acceptance, a booked training/checkride event is created and the member is notified.
7. On decline, the member is notified with the reason provided.

## 3. For Members: Submitting an Availability Request

### 3.1 Finding instructor availability
1. Open `Calendar` from the sidebar.
2. Availability blocks appear as events on the calendar.
3. Availability events show which instructor posted them and the time range available.

### 3.2 Submitting a request
1. Click on an availability block on the calendar.
2. Select the option to request a time within that block.
3. Fill in the request form:
   - `Purpose`: What you want to do during this session (for example, "IFR approaches practice" or "instrument proficiency check").
   - `Requested Time Window`: The start and end time you want within the instructor's availability block.
4. Submit the request.

### 3.3 After you submit
1. Your request is sent to the instructor.
2. The instructor receives a notification.
3. You will be notified when the instructor accepts or declines.
4. If accepted, the scheduled event appears on your calendar.
5. If declined, you will receive the instructor's reason.

### 3.4 Tips for a successful request
- Be specific about your purpose. "Flight instruction" is less helpful than "cross-country planning and VOR tracking practice."
- Request a time window that fits within the instructor's availability block.
- Give yourself buffer time for pre-flight briefing and post-flight debrief.
- Confirm with your instructor if you need a specific aircraft reserved.

## 4. For Instructors: Responding to Requests

### 4.1 Receiving a request notification
When a member submits a request for your availability:
1. You receive a notification via your enabled notification methods (email, in-app, SMS).
2. The notification includes the member's name, purpose, and requested time.

### 4.2 Reviewing and responding
1. Open the notification or navigate to `Calendar`.
2. Find the availability event the request is associated with.
3. Open the request details.
4. Choose `Accept` or `Decline`.

### 4.3 Accepting a request
On acceptance:
1. Review the event details (time, resource if applicable).
2. Select the resource (aircraft/equipment) if your original availability block did not specify one.
3. Submit the acceptance.

**What happens on acceptance:**
- A booked training event is created on the calendar.
- The original availability block is automatically split so the remaining time stays available.
- The requesting member receives a notification confirming the booking.
- The request status updates to accepted.

### 4.4 Declining a request
On decline:
1. Enter a clear, helpful reason (for example, "I have a conflict at that time—please request the later window" or "I am not current on that aircraft type").
2. Submit the decline.

**What happens on decline:**
- The request status updates to declined.
- The member receives a notification with your reason.
- Your availability block remains intact for other requests.

### 4.5 Best practices for responding to requests
1. **Respond promptly.** Members are often planning flights around your response. Delayed responses can block their scheduling.
2. **Provide useful decline reasons.** A reason like "not available" is not as helpful as "I have a ground lesson at that time, but I'm free in the afternoon—try requesting 2–4 PM."
3. **Review pending requests daily.** Check your notifications or calendar each day for outstanding requests.
4. **Specify the resource during acceptance.** If the training requires a specific aircraft, confirm and select it when accepting to ensure the aircraft is reserved.

## 5. Managing Your Availability (Instructors)

For guidance on publishing availability blocks, editing them, and the full instructor calendar workflow, see:
`docs/users/instructors/INSTRUCTOR_AVAILABILITY_AND_RATES.md`

## 6. Notification Preferences

Both members and instructors can control whether they receive availability request notifications.

To manage this preference:
1. Open `Profile` from the sidebar.
2. Scroll to `Notification Preferences`.
3. Toggle `Availability Requests` on or off.

If this category is off, you will not receive request-related alerts.

For full notification setup guidance, see:
`docs/users/members/MEMBER_NOTIFICATION_PREFERENCES.md`

## 7. Troubleshooting

### 7.1 No availability blocks visible on calendar
Possible causes:
1. No instructors have published availability.
2. `Availability Event Type` is not enabled in your organization.
3. You are viewing a date range with no availability.

Action:
1. Check with your instructor about when they plan to post availability.
2. Contact an admin to confirm that `Availability Event Type` is enabled in `Organization` settings.
3. Navigate forward in the calendar to check upcoming dates.

### 7.2 Cannot submit a request
Possible causes:
1. Requested time window is outside the availability block.
2. The availability block was already booked or removed.

Action:
1. Confirm your requested start and end times fall within the instructor's availability block.
2. Refresh the calendar to see if the block is still available.
3. Contact the instructor directly if the issue persists.

### 7.3 Acceptance failed
Possible causes:
1. The requested time is outside the original availability block.
2. A required resource was not selected.
3. A newer conflicting event was created.

Action:
1. Refresh the request page.
2. Verify the requested time and resource.
3. Re-submit the acceptance response.

### 7.4 Not receiving request notifications
Possible causes:
1. `Availability Requests` category is turned off in notification preferences.
2. All notification methods are disabled.

Action:
1. Open `Profile` → `Notification Preferences` and enable `Availability Requests`.
2. Confirm at least one notification method (email, SMS, push) is active.

## 8. Related Manuals

1. Instructor availability publishing:
   `docs/users/instructors/INSTRUCTOR_AVAILABILITY_AND_RATES.md`
2. Notification preferences:
   `docs/users/members/MEMBER_NOTIFICATION_PREFERENCES.md`
3. Pilot scheduling guide:
   `docs/users/members/PILOT_SCHEDULING_GUIDE.md`
