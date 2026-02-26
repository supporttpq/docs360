---
description: >-
  Monitor and resolve booking alerts in Tourpaq Office. Review unpaid bookings,
  overbookings, errors, warnings, and Stop Sales notifications.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Notifications

### Overview

The **Notifications** module in **Tourpaq Office** helps you monitor and resolve **booking alerts**. It centralizes system warnings, booking errors, and operational messages so your team can keep bookings accurate.

Use it to track common issues like **unpaid bookings**, **overbookings**, and **Stop Sales** conflicts.

Open **Notifications** from the main navigation to see a consolidated list of issues across bookings and products.

<figure><img src="../.gitbook/assets/image (243).png" alt="Notifications overview"><figcaption><p>Notifications overview – categories on the left, detailed list in the center.</p></figcaption></figure>

### Purpose

This module is intended to:

* Provide fast visibility into booking-related issues and system warnings
* Highlight critical problems such as **unpaid bookings** and **overbookings**
* Help users troubleshoot and resolve booking errors (**Error Bkg**)
* Improve booking completeness and day-to-day operations

By consolidating alerts by type and severity, this module supports **operational efficiency and customer satisfaction**.

***

### Preconditions

* Available only to users with permission to access booking administration and notifications.
* Booking data should be up to date and error-checking services must be running in the background.
* Some notifications (for example, **overbookings** or **Stop Sales**) rely on system configuration thresholds (such as allotment and agreed allotment).

***

### Page Structure

#### Left panel: Notification categories

The **left-side menu** organizes notifications by type. Each category shows a **counter** for active issues.

| Category                | Description                                                                                    |
| ----------------------- | ---------------------------------------------------------------------------------------------- |
| **Unpaid Bkg**          | Reservations with outstanding payments.                                                        |
| **Overbkg**             | Overbookings at various levels (Homebound, Hotels, Rooms, Outbound).                           |
| **Error Bkg**           | Errors that occurred while saving or updating a booking.                                       |
| **Warnings**            | General warnings that don’t block the booking but may need attention.                          |
| **Hotel Special Offer** | Issues related to hotel-based special offers (for example, rejected or inconsistent offers).   |
| **Extra Special Offer** | Issues related to special offers on extras.                                                    |
| **Upsale**              | Opportunities or issues related to additional product sales.                                   |
| **Stop Sales**          | Notifications related to active or upcoming Stop Sale rules and their agreed allotment status. |
| **Queue Management**    | Errors in background processing queues (for example, confirmations or communication jobs).     |

{% hint style="warning" %}
Use the counters to prioritize. Start with **Error Bkg** and **Overbkg**. Then handle **Unpaid Bkg** and **Warnings**.
{% endhint %}

***

#### Center panel: Notifications list (table)

This is the **main working area**, displaying **detailed alerts**. Depending on the notification type, the central panel may present different data fields. Some of the most commonly displayed information includes:

| Column Name           | Description                                             |
| --------------------- | ------------------------------------------------------- |
| **Booking No**        | Unique identifier of the affected reservation.          |
| **Departure Date**    | The date of travel associated with the booking.         |
| **Customer**          | Full name of the lead passenger or customer.            |
| **Booking Total**     | Total value of the reservation (all included services). |
| **Paid Amount**       | Amount already paid by the customer.                    |
| **Balance**           | Remaining unpaid amount.                                |
| **Error Description** | Human-readable explanation of the issue or error.       |

Each row represents a **single notification event**, tied to a specific booking.

***

#### Filters, sorting, and navigation

* **Pagination controls** are located at the bottom of the table to move between pages of results.
* A **records-per-page selector** lets you choose how many notifications to display at once (for example, 10, 25, 50).
* Clicking on **column headers** allows sorting by fields such as **Booking No**, **Departure Date**, or **Customer**.
* Depending on your configuration, additional **filters** (for example, by departure period or destination) may be available at the top of the list to narrow down results.

***

### How to resolve notifications

Use Notifications as your daily control center for booking quality and exception handling.

{% stepper %}
{% step %}
### 1. Select a category

1. In the left panel, click the notification category you want to review (for example, **Unpaid Bkg** or **Overbkg**).
2. The central table is refreshed to show only notifications of that type.
{% endstep %}

{% step %}
### 2. Review the list

1. Scan the **Error Description**, **Departure Date**, and **Balance** (if available) to understand the impact.
2. Use sorting (for example, sort by **Departure Date**) to focus on the most urgent cases first.
{% endstep %}

{% step %}
### 3. Open and fix the related booking

1. Use the **Booking No** (and, where applicable, the **Customer** name) to locate and open the corresponding booking in **All bookings** or another booking view.
2. Correct the underlying issue (for example, update payments, fix product selection, or adjust allotment/Stop Sales rules).
{% endstep %}

{% step %}
### 4. Refresh and verify

1. After saving the booking, return to the **Notifications** page.
2. Refresh the list or wait for the next automatic update.
3. Confirm that the notification has disappeared or changed status as expected.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
For **Stop Sales** notifications, you can use the dedicated workflow described in [Notification on Dashboard Stop Sale](../stop-sales/notification-on-dashboard-stop-sale.md) to filter by **Only Agreed Allotment** and focus on the most business-critical rules.
{% endhint %}

***

### Behavior and refresh

* Notifications clear after you fix the root cause and the system checks run again.
* Counters and lists may auto-refresh depending on configuration (for example, every 30 minutes).
* The presence of **multiple notification types for a single booking** is possible (for example, a booking can appear under both **Unpaid Bkg** and **Warnings**).
* In some environments, **notification acknowledgment** features may be enabled to track who resolved which notification and when.

***

### Related Topics

For configuration of automated messages and related alerts, see:

* [Warning notification rules](../warning-notification-rules.md) – configure which system warnings are sent and to whom.
* [Email Templates](../email-templates.md) – manage the content of automated e-mails triggered by booking events.
* [Notification on Dashboard Stop Sale](../stop-sales/notification-on-dashboard-stop-sale.md) – specific behavior of **Stop Sales** notifications on the Dashboard.
* [Service Case – Notification](../service-cases/notification.md) – notifications related to customer **Service Cases** and new incoming e-mails.
* [Customer information (errata)](../customer-information-errata/) – how special guest notifications are shown based on stay and booking periods.

### FAQ

#### Where do I handle Stop Sales notifications?

Fix the root cause in booking setup or booking data.

Use [Notification on Dashboard Stop Sale](../stop-sales/notification-on-dashboard-stop-sale.md) for the recommended Stop Sales workflow.

#### What’s the difference between “Error Bkg” and “Warnings”?

* **Error Bkg**: The booking is not finalized. Something failed during save or processing.
* **Warnings**: The booking status is OK. Something still needs attention. Example: travel insurance not sent.

#### Can one booking show up under multiple categories?

Yes. One booking can trigger multiple notifications.

#### What should I prioritize first?

Start with issues that can block operations.

1. **Error Bkg**
2. **Overbkg**
3. **Unpaid Bkg**
4. **Warnings**

#### How do notifications disappear after I fix a booking?

1. Save the booking changes.
2. Go back to **Notifications**.
3. Refresh the list or wait for the next update cycle.

Notifications clear when the issue is fixed and the checks rerun.

***
