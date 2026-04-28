# Blog Entries and News

This manual explains how to create, manage, and use the `News` page in Contact Ground.

`News` is your organization's announcement board for content that should remain accessible over time—policy updates, training announcements, operational guidance, and member communications that members may need to reference later.

## 1. Who Can Post to News

You can create a blog entry in `News` if at least one of the following is true:
1. You hold one of these roles: `owner`, `admin`, `cfi`, `cfii`, `dpe`, `operations`, or `accounting`.
2. You have the `Blog` endorsement assigned to your profile.

All members can view entries regardless of their role or endorsements.

## 2. Viewing News Entries

1. Open `News` from the sidebar.
2. Select an entry from the `Recent Entries` list on the left.
3. Read the full content in the viewer pane.

Each entry shows its title, author, and publish date.

## 3. Creating a New Entry

1. Open `News`.
2. Click `New Entry`.
3. Enter a title.
4. Write the body content. Markdown formatting is supported.
5. Save the entry.

The entry appears immediately in the `Recent Entries` list for all members.

When a new entry is published, members who have `News Updates` enabled in their notification preferences can receive email, push, and in-app notifications that link directly to that exact entry.

### 3.1 Markdown support
The body field supports Markdown formatting. You can use:
- `# Heading`, `## Heading 2` for section headers
- `**bold**` and `*italic*` for emphasis
- `- item` for bullet lists
- `1. item` for numbered lists
- Blank lines to separate paragraphs

Keep formatting simple so content is easy to read on all devices.

## 4. Editing and Deleting Entries

### 4.1 Editing
1. Open the entry in `News`.
2. Click the edit icon.
3. Update the title or body.
4. Save your changes.

**Who can edit:**
- The author of the entry.
- Any `owner` or `admin`.
- Any member with a role or endorsement that permits creating blog entries.

### 4.2 Deleting
1. Open the entry in `News`.
2. Click the delete icon.
3. Confirm the deletion.

**Who can delete:**
- The author of the entry.
- Any `owner` or `admin`.

Deletion is immediate and permanent.

## 5. Giving Standard Members Posting Access

If a standard member (without an elevated role) should be able to post in `News`:
1. Open `People` and find the member's profile.
2. In the endorsements section, add the `Blog` endorsement.
3. If the `Blog` endorsement type does not exist in your organization yet:
   - Go to `Organization` → `Endorsements`.
   - Create an endorsement type named `Blog`.
   - Then assign it to the member in `People`.

Note: New organizations typically include `Blog` as a default endorsement type. Older organizations may need to create it manually.

## 6. Writing Effective News Entries

1. **Start with a specific title.** Members scan titles to find relevant content. Avoid vague titles like "Update" or "FYI."
2. **Lead with the key action.** Put the most important information first. Members may not read all the way to the end.
3. **Use short paragraphs and bullet points.** Dense blocks of text are harder to skim.
4. **Include dates in full format.** Write `March 1, 2026` instead of `3/1` to avoid ambiguity.
5. **State if action is required.** If members need to do something, say so explicitly and early.

## 7. News vs. Messaging: When to Use Each

| Use Case | Recommended Tool |
|----------|-----------------|
| Announcement members should reference later | `News` |
| One-time notification to a specific group | `Messaging` |
| Policy change that applies permanently | `News` |
| Urgent operational alert | `Messaging` |
| Training or safety guidance | `News` |
| Personal reply needed from members | `Messaging` |

Use `News` for durable content. Use `Messaging` when the goal is distribution and immediate awareness.

## 8. Maintaining the News Feed

1. **Update outdated entries.** Members should not act on stale information. Edit or delete entries that are no longer accurate.
2. **Do not let old entries dominate.** If the `Recent Entries` list is full of old announcements, new content is harder to find. Archive or delete entries that are no longer relevant.
3. **Pin important content by keeping it current.** There is no pinning feature—keeping critical entries up to date ensures they remain useful.
4. **Keep content appropriate.** Avoid profanity, irrelevant content, and keep all post text within acceptable organizational guidelines.

## 9. News Notification Preference

Members control News notifications in `Profile` → `Notification Preferences` → `News Updates`.

Notes:
1. This preference is per organization.
2. Turning it off stops new-entry notifications, but does not remove access to the `News` page itself.
3. Delivery method still depends on the member's enabled notification methods (email, SMS, push). News notifications currently use in-app, email, and push where available.

## 10. Related Manuals

1. Organizational messaging for targeted notifications:
   `docs/users/administration/MESSAGING.md`
2. Endorsement management (for Blog endorsement setup):
   `docs/features/ENDORSEMENTS.md`
3. Administration overview:
   `docs/users/administration/ADMINISTRATION.md`
