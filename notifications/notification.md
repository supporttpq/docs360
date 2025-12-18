# Notification

### Overview

The **Notifications** page is a system-level tool used to **monitor, review, and manage issues and alerts related to bookings**. It centralizes all system-generated warnings, errors, and informational messages to help users maintain data integrity and ensure smooth booking operations.

Open the **Notifications** module from the main navigation to see a consolidated list of issues across bookings and products.

<figure><img src="../.gitbook/assets/image (243).png" alt="Notifications overview"><figcaption><p>Notifications overview – categories on the left, detailed list in the center.</p></figcaption></figure>

### Purpose

This module is intended to:

* Provide **real-time visibility** into booking-related issues
* **Highlight critical problems** such as unpaid or overbooked reservations
* **Assist users in troubleshooting and resolving errors**
* Help ensure **reservation completeness and accuracy**

By consolidating alerts by type and severity, this module supports **operational efficiency and customer satisfaction**.

***

### Preconditions

* Available only to users with permission to access booking administration and notifications.
* Booking data should be up to date and error-checking services must be running in the background.
* Some notifications (for example, **overbookings** or **Stop Sales**) rely on system configuration thresholds (such as allotment and agreed allotment).

***

### Page Structure

#### 🔹 Left Panel: Notifications Menu (Categories)

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
🔔 **TIP**

Use the counters next to each category to **prioritize** which notifications to address first (for example, start with **Error Bkg** and **Overbkg**, then move on to **Unpaid Bkg** and **Warnings**).
{% endhint %}

***

#### Central Panel: Notification Table

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

#### Filters, Sorting & Navigation

* **Pagination controls** are located at the bottom of the table to move between pages of results.
* A **records-per-page selector** lets you choose how many notifications to display at once (for example, 10, 25, 50).
* Clicking on **column headers** allows sorting by fields such as **Booking No**, **Departure Date**, or **Customer**.
* Depending on your configuration, additional **filters** (for example, by departure period or destination) may be available at the top of the list to narrow down results.

***

### Working With Notifications

Use the Notifications page as your **daily control center** for booking quality:

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

### Special Notes & Behaviors

* Notifications **do not auto-resolve**—they must be handled and cleared through booking updates or internal processing.
* The system may **auto-refresh counters and lists** periodically depending on configuration (for example, every 30 minutes).
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



### **FAQ**

#### I see a Stop Sales notification. Where do I handle it?

In both cases, fix the root cause in the booking or setup.

* **Error Bkg**: something failed during save or processing.
* **Warnings**: something looks off, but may still be bookable.

#### What’s the difference between “Error Bkg” and “Warnings”?

A booking with the status "Error Booking" represents a booking that is not finalized (some changes still need to be made to it), while status "Warnings" represent bookings that have the status OK, and which warn you that there is a problem with that booking (travel insurance was not sent, etc.)

#### What should I prioritize first?

Example: **Unpaid Bkg** and **Warnings** at the same time.

Yes. One booking can trigger multiple issues at once.

#### Can the same booking show up under multiple categories?

1. Save the booking changes.
2. Go back to **Notifications**.
3. Refresh the list or wait for the next update cycle.

Notifications clear when the underlying issue is gone and the checks rerun.

***
