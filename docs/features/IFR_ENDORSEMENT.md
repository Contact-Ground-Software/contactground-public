# IFR Endorsement & Flight Rules

This manual describes the IFR endorsement and flight-rules tagging feature in Contact Ground.

## 1. Overview

Organizations can tag calendar events with **VFR** (Visual Flight Rules) or **IFR** (Instrument Flight Rules) to indicate the intended flight environment. When an organization has an **IFR endorsement type** configured:

- Members may select **VFR** or **IFR** when creating or editing an event.
- **IFR events** are restricted to members who hold an IFR endorsement.
- **VFR events** that are forecast to have non-VFR weather at departure time trigger an automatic weather alert in the pre-flight dispatch email.

If the organization has **not** created an IFR endorsement type, flight-rules tagging is unavailable and this feature has no effect.

---

## 2. Enabling the Feature (Admin)

The feature activates automatically when an IFR endorsement type exists in the organization. By default, Contact Ground creates a standard **IFR ☁️** endorsement type for every new organization.

### To verify or create the IFR endorsement type

1. Navigate to **Settings → Endorsements**.
2. Confirm an endorsement type named **IFR** (☁️) is listed.
3. If it does not exist, create one with the name `IFR`.

Once the IFR endorsement type exists, the **Flight Rules** selector appears on the event creation form for all members.

---

## 3. Member Experience

### During Event Creation

When the organization has an IFR endorsement type, a **Flight Rules** field appears on the event creation form:

| Option | Description |
|--------|-------------|
| *(not specified)* | No flight-rules preference recorded |
| **VFR** | Visual Flight Rules – standard VFR conditions expected |
| **IFR** | Instrument Flight Rules – IFR endorsement required |

Members without an IFR endorsement will receive an error if they attempt to book an IFR event.

### Pre-flight Email

The pre-flight dispatch email includes:
- **Flight Rules** in the Flight Details section (when specified).
- **VFR Weather Alert** warning box if the event is tagged **VFR** and the TAF-predicted conditions at the homebase are less than VFR (MVFR, IFR, or LIFR) at the scheduled departure time.

---

## 4. CFI Experience

CFIs can assign or remove the **IFR** endorsement from members through the standard endorsement workflow:

1. Navigate to **People → [Member] → Endorsements**.
2. Select **Assign Endorsement → IFR**.
3. The endorsement is recorded with the CFI's user ID and the current timestamp.

Once assigned, the member may book IFR events.

---

## 5. VFR Weather Notification

When a member creates a **VFR** event, Contact Ground checks the TAF forecast for the organization's homebase at the scheduled departure time. If the forecast predicts conditions below VFR minimums:

| Condition | Threshold |
|-----------|-----------|
| MVFR ceiling | 1 000 – 3 000 ft AGL |
| MVFR visibility | 3 – 5 SM |
| IFR ceiling | 500 – 999 ft AGL |
| IFR visibility | 1 – 2 SM |
| LIFR ceiling | < 500 ft AGL |
| LIFR visibility | < 1 SM |

A **VFR Weather Alert** warning box is included in the pre-flight email, identifying the predicted flight category and recommending the pilot review conditions before departure.

> **Note:** The weather check uses the base FM group in the TAF. TEMPO and PROB overlays are not used for the primary alert to avoid spurious warnings.

---

## 6. Booking Validation

| Scenario | Outcome |
|----------|---------|
| Org has no IFR endorsement type | Flight rules field hidden; no validation |
| IFR event, member has IFR endorsement | Booking succeeds |
| IFR event, member **lacks** IFR endorsement | Booking blocked with error: *"An IFR endorsement is required to book an IFR event"* |
| VFR event, any member | Booking always succeeds; weather checked at dispatch time |

---

## 7. Related Areas

- **Endorsements** – assign IFR endorsements to members.
- **Admin → Endorsements** – create/manage the IFR endorsement type.
- **Flight Operations → Pre-flight Dispatch** – includes flight rules and weather alert.
- **Calendar → Create Event** – select flight rules when org has IFR type.
