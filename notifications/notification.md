---
description: Your daily control centre for booking alerts, errors, and system warnings.
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

The **Notifications** page is a centralised monitoring tool that collects and displays all system-generated alerts related to bookings, products, payments, and operational processes. Instead of discovering problems one booking at a time, agents and administrators can open this page and immediately see every issue that needs attention — organised by type and severity.

Notifications are generated automatically by the system based on background checks. They do not resolve themselves — each one must be investigated and fixed at the source before it disappears from the list.

<figure><img src="../.gitbook/assets/image (243).png" alt="Notifications overview"><figcaption><p>Notifications overview – categories on the left, detailed list in the center.</p></figcaption></figure>

### Purpose

The Notifications module exists to help teams:

* Spot and resolve **booking errors** before they affect customers or operations
* Track **unpaid bookings** and outstanding balances at a glance
* Identify and fix **overbooking situations** across hotels, rooms, and transports
* Stay on top of **Stop Sales violations**, queue errors, and upsell opportunities
* Maintain overall **data quality and reservation accuracy** across the platform

It is particularly valuable for operations managers and senior agents who need a daily system health check without opening individual bookings one by one.

***

### Preconditions

Before using the Notifications page, ensure the following:

* You are logged in with a user role that has **access to booking administration and notifications**. If the Notifications page is not visible in your sidebar, contact your system administrator to review your permissions under [Users](https://manual.tourpaq.com/users/users).
* Background error-checking services are running correctly. If no notifications appear at all and you expect them, contact your administrator to verify that system checks are active.
* Allotment thresholds and Stop Sales rules must be correctly configured for overbooking and Stop Sales notifications to fire accurately. See [Stop Sales](https://manual.tourpaq.com/stop-sales) and [Hotel Contracts](https://manual.tourpaq.com/hotel-contracts).

***

### How to Use the Notifications Page

#### Step 1 — Open Notifications

Click **Notifications** in the left sidebar. The page opens with the full list of active notifications across all categories.

***

#### Step 2 — Select a category

In the **left panel**, click the notification category you want to review. The central table immediately refreshes to show only notifications of that type. The number displayed next to each category name is the count of active, unresolved notifications in that category.

{% hint style="info" %}
**Recommended daily priority order:**

* **Overbkg** — overbooking situations that may affect customers
* **Unpaid Bkg** — outstanding balances requiring follow-up
* **Warnings** — non-blocking issues that still need attention
* **Stop Sales / Queue Management** — operational and configuration issues
{% endhint %}

***

#### Step 3 — Review the notification list

In the central panel, scan the table for the most urgent items. Use column headers to sort the list — for example, sort by **Departure Date** to prioritise upcoming trips, or by **Balance** to focus on the largest outstanding payments first.

Use the **records-per-page selector** at the bottom to control how many rows are shown, and the **pagination controls** to navigate through the full list.

***

#### Step 4 — Open and resolve the booking

Use the **Booking No** in the notification row to locate the affected booking. Open it via [All Bookings](https://manual.tourpaq.com/booking/all-bookings) and correct the underlying issue — for example:

* Register a missing payment for an **Unpaid Bkg**
* Adjust allotment or move a passenger for an **Overbkg**
* Fix missing or invalid data for an **Error Bkg**
* Review and update product rules for **Warnings**

***

#### Step 5 — Verify the notification is cleared

After saving the fix, return to the Notifications page and refresh the list. If the underlying issue has been resolved, the notification will no longer appear. If it persists, the fix was incomplete — review the booking again.

{% hint style="warning" %}
&#x20;Notifications are not automatically cleared when you save a reservation. The system reruns its checks periodically, every 30 minutes.
{% endhint %}

***

### Field Reference

#### Left Panel — Notification Categories

| Category                | Description                                                                                                                                                  |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Unpaid Bkg**          | Bookings with outstanding payments — the customer owes a balance that has not been registered                                                                |
| **Overbkg**             | Overbooking situations, broken down by type: Homebound transport, Hotels, Rooms, and Outbound transport                                                      |
| **Error Bkg**           | Bookings that encountered a system error during saving or processing and are in an incomplete or invalid state                                               |
| **Warnings**            | Bookings in a valid state but with a condition that requires attention — for example, travel insurance was not sent, or a special service request is missing |
| **Hotel Special Offer** | Issues related to hotel special offers — for example, an offer that was applied incorrectly or is inconsistent with contract conditions                      |
| **Extra Special Offer** | Issues with special offers on extras — similar to Hotel Special Offer but for extra products                                                                 |
| **Upsale**              | Alerts related to upsell opportunities or upsell products that have an issue requiring review                                                                |
| **Stop Sales**          | Bookings or products affected by an active Stop Sales rule, including cases where agreed allotment has been exceeded                                         |
| **Queue Management**    | Errors in background processing queues — for example, failed confirmation sends, communication jobs, or automated processing tasks                           |

***

#### Central Panel — Notification Table

The columns displayed depend on the selected category. The most commonly shown fields are:

| Column                | Description                                                                                                                                      |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Booking No**        | The unique identifier of the affected booking. Use this to locate the booking in [All Bookings](https://manual.tourpaq.com/booking/all-bookings) |
| **Departure Date**    | The outbound travel date associated with the booking. Use this to prioritise time-sensitive cases                                                |
| **Customer**          | Full name of the lead passenger or primary customer on the booking                                                                               |
| **Booking Total**     | The total value of the reservation, including all travel components and extras                                                                   |
| **Paid Amount**       | The amount already registered as paid by the customer                                                                                            |
| **Balance**           | The remaining unpaid amount. A positive value means money is still owed                                                                          |
| **Error Description** | A plain-language description of the issue or error detected by the system                                                                        |

***

#### Navigation Controls

| Control              | Description                                                                                                               |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Column headers**   | Click any column header to sort the list ascending or descending by that field                                            |
| **Records per page** | Selector at the bottom of the table — choose 10, 25, or 50 rows per page                                                  |
| **Pagination**       | Navigate between pages of results using the Previous / Next controls at the bottom                                        |
| **Filters**          | Where available, use filters at the top of the list to narrow results by departure period, destination, or other criteria |

***

### FAQ

**Q: What is the difference between Error Bkg and Warnings?** An **Error Bkg** means the booking is in an incomplete or invalid state — something failed during saving or processing and the booking may not be fully confirmed. A **Warning** means the booking is technically valid and confirmed, but a condition exists that needs attention — for example, travel insurance was not sent, or a required document is missing. Errors are more urgent than warnings.

***

**Q: Can the same booking appear under multiple categories at the same time?** Yes. A single booking can trigger notifications in multiple categories simultaneously — for example, a booking could appear under both **Unpaid Bkg** (because a payment is missing) and **Warnings** (because travel insurance was not sent). Each issue must be resolved independently.

***

**Q: What should I tackle first each day?** Start with **Error Bkg** — these represent bookings in an invalid state that may cause downstream problems. Then move to **Overbkg** — these can directly affect customers if not resolved before departure. Follow with **Unpaid Bkg**, then **Warnings**, and finally the remaining categories.

***

**Q: I fixed a booking but the notification is still showing — why?** The system reruns its background checks on a periodic cycle. After saving a fix, wait a few minutes and then refresh the Notifications page. If the notification persists after several minutes, the fix may be incomplete — review the booking again to ensure the root cause was fully addressed.

***

**Q: How do I handle Stop Sales notifications?** A Stop Sales notification means a booking exists for a product that is currently under a Stop Sales restriction, or that agreed allotment has been exceeded. Review the affected booking and the Stop Sales configuration. See [Stop Sales](https://manual.tourpaq.com/stop-sales) for full details on how to manage Stop Sales rules and their allotment settings.

***

**Q: I can't see the Notifications page in my sidebar — why?** Your user role may not include access to the Notifications module. Contact your system administrator and ask them to review your permissions under [Users](https://manual.tourpaq.com/users/users).

***

### Related Pages

* [Warning Notification Rules](https://manual.tourpaq.com/warning-notification-rules) — configure which system warnings are generated and who receives them
* [Stop Sales](https://manual.tourpaq.com/stop-sales) — manage Stop Sales rules linked to Stop Sales notifications
* [All Bookings](https://manual.tourpaq.com/booking/all-bookings) — find and open bookings referenced in notifications
* [Service Cases](https://manual.tourpaq.com/service-cases) — manage customer service issues that may also generate notifications
* [Customer Information (Errata)](https://manual.tourpaq.com/customer-information-errata) — notifications related to customer errata based on booking and stay periods
* [Email Templates](https://manual.tourpaq.com/email-templates) — manage automated email content triggered by booking events
