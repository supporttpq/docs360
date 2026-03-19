---
description: Your daily control centre for booking alerts, errors, and system warnings.
icon: bell
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

<img src="../.gitbook/assets/file.excalidraw.svg" alt="" class="gitbook-drawing">

{% hint style="warning" %}
Notifications are not automatically cleared when you save a reservation. The system checks for updates every 30 minutes.
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

### Working Pattern by Category

Use the category name to decide both **priority** and **owner**.

Some notifications can be resolved by an agent in the booking. Others point to a wider setup or system issue and should go to an administrator or product owner.

| Category             | Typical owner                    | Typical next action                                             | What usually clears it                                    |
| -------------------- | -------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------- |
| **Unpaid Bkg**       | Sales or finance user            | Register payment, correct payment method, or verify balance     | The balance no longer matches the unpaid rule             |
| **Overbkg**          | Operations or product user       | Move passengers, adjust allotment, or review availability       | The booking no longer exceeds hotel or transport capacity |
| **Error Bkg**        | Senior agent or admin            | Open the booking, fix invalid data, then save again             | The booking passes validation and background checks       |
| **Warnings**         | Agent, operations user, or admin | Read the warning text and complete the missing follow-up        | The missing task or condition is no longer true           |
| **Stop Sales**       | Product or operations user       | Review the booking together with the Stop Sale rule             | The booking no longer conflicts with the active rule      |
| **Queue Management** | Admin or support user            | Check the failed background job, integration, or resend process | The queue job succeeds on the next run                    |

{% hint style="info" %}
If a notification points to a setup issue, fixing one booking may not be enough. Check whether similar bookings could be affected by the same rule, contract, or integration problem.
{% endhint %}

### What to check before opening the booking

Use the notification row to decide your first check:

* Check **Departure Date** first for anything time-sensitive.
* Check **Balance** first for **Unpaid Bkg**.
* Check **Error Description** first for **Error Bkg**, **Warnings**, and **Queue Management**.
* Check whether the issue looks **booking-specific** or **system-wide** before you start editing data.

This saves time and reduces duplicate work between agents.

***

### FAQ

#### What is the difference between Error Bkg and Warnings?

An **Error Bkg** means the booking is in an incomplete or invalid state.

Something failed during saving or processing. The booking may not be fully confirmed.

A **Warning** means the booking is valid, but still needs follow-up.

Examples include missing travel insurance communication, missing documents, or another non-blocking issue.

#### Can the same booking appear under multiple categories at the same time?

Yes.

One booking can trigger several checks at once. For example, it can appear under both **Unpaid Bkg** and **Warnings**.

Each category reflects a separate issue. Resolve each one at the source.

#### What should I tackle first each day?

Start with **Error Bkg**, **Overbkg**, and **Queue Management**.

These are the categories most likely to block processing or affect departures.

Then handle **Unpaid Bkg**, followed by **Warnings** and the remaining categories.

#### Why does the category count not match the rows I currently see?

The category count shows all unresolved items in that category.

The table can still be narrowed by filters, sorting, pagination, or the current date range.

If the count looks wrong, clear filters and reload the category.

#### Can I clear or delete a notification manually?

No.

Notifications are cleared by resolving the underlying issue.

If the source problem still exists, the notification will return on the next system check.

#### I fixed a booking but the notification is still showing. Why?

The system checks for updates every 30 minutes.

After saving a fix, refresh the page after the next check cycle.

If it still appears, the root cause was not fully resolved.

#### Why did a notification disappear and then come back?

The same condition was detected again.

This usually means the issue was only partly fixed, or another background job recreated the same problem.

Check the booking again. Then review any related setup, integration, or queue process.

#### How do I handle Stop Sales notifications?

A Stop Sales notification means a booking conflicts with an active Stop Sale rule, or agreed allotment has been exceeded.

Review both the booking and the Stop Sale setup before changing anything.

Use [Stop Sales](../stop-sales.md) to inspect the rule behind the alert.

#### Who should handle Queue Management notifications?

Usually an administrator or advanced support user.

These notifications often involve failed background jobs, integrations, communication sends, or system automation.

If the error description mentions GDS, SMTP, FTP, or queue processing, escalate early.

#### What if I open the booking and nothing looks wrong?

Start with the area named in the notification text.

Then check **History**, **Economics**, **E-mails**, **SMS**, or related product setup depending on the category.

Some issues are caused by background processing, not by visible booking data alone.

#### Are notifications assigned to one user?

No.

The page is a shared operational list, not a personal task queue.

Two users can work the same notification unless your team coordinates ownership outside the page.

#### I can see the Notifications page, but some bookings are missing. Why?

This is usually caused by user rights, brand scope, or filter settings.

Check your current filters first.

If the booking is still missing, ask your administrator to review your access under [Users](../users/users/).

#### Where do I control which warnings are generated?

Use [Warning Notification Rules](../warning-notification-rules.md).

That is where you configure warning recipients, delivery method, and warning types.

### Related Pages

* [Warning Notification Rules](../warning-notification-rules.md) — configure which system warnings are generated and who receives them
* [Stop Sales](../stop-sales.md) — manage Stop Sales rules linked to Stop Sales notifications
* [All Bookings](../booking/all-bookings/) — find and open bookings referenced in notifications
* [Service Cases](../service-cases/) — manage customer service issues that may also generate notifications
* [Customer Information (Errata)](../customer-information-errata/) — notifications related to customer errata based on booking and stay periods
* [Email Templates](../email-templates.md) — manage automated email content triggered by booking events
