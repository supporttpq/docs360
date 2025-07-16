# Notification

### 🧭 Overview

The **Reservation Notifications** page is a system-level tool used to **monitor, review, and manage issues and alerts related to bookings**. It centralizes all system-generated warnings, errors, and informational messages to help users maintain data integrity and ensure smooth booking operations.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 🎯 Purpose

This module is intended to:

* Provide **real-time visibility** into booking-related issues
* **Highlight critical problems** such as unpaid or overbooked reservations
* **Assist users in troubleshooting and resolving errors**
* Help ensure **reservation completeness and accuracy**

By consolidating alerts by type and severity, this module supports **operational efficiency and customer satisfaction**.

***

### ✅ Preconditions

* Available only to users with permission to access booking administration and notifications.
* Booking data must be up-to-date and error checking services should be running in the background.
* Some notifications (e.g., overbookings) may rely on system configuration thresholds (e.g., allotment).

***

### 🧭 Page Structure

#### 🔹 Left Panel: Notifications Menu (Categories)

The **left-side menu** organizes notifications by type. Each category shows a **counter** for active issues.

| Category                | Description                                                                       |
| ----------------------- | --------------------------------------------------------------------------------- |
| **Unpaid Bkg**          | Reservations with outstanding payments.                                           |
| **Overbkg**             | Overbookings at various levels (Homebound, Hotels, Rooms, Outbound).              |
| **Error Bkg**           | Errors that occurred while saving or updating a booking.                          |
| **Warnings**            | General warnings that don’t block the booking but may need attention.             |
| **Hotel Special Offer** | Issues related to hotel-based special offers.                                     |
| **Extra Special Offer** | Issues related to special offers on extras.                                       |
| **Upsale**              | Opportunities or issues related to additional product sales.                      |
| **Queue Management**    | Errors in background processing queues (e.g., confirmations, communication jobs). |

> 🔔 **TIP**: The count next to each category helps **prioritize** which notifications to address first.

***

#### 📋 Central Panel: Notification Table

This is the **main working area**, displaying **detailed alerts**. Columns include:

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

#### 🔄 Navigation & Pagination

* **Pagination Controls**: Located at the bottom of the table.
* **Records Per Page Selector**: Choose how many notifications to display at once (e.g., 10, 25, 50).
* **Sorting**: Clicking on column headers allows for sorting by Booking No, Date, or other fields.

***

### 🚩 Special Notes & Behaviors

* Notifications **do not auto-resolve**—they must be handled and cleared through booking updates or internal processing.
* System may **auto-refresh counters** periodically depending on configuration (e.g., every 30 minutes).
* The presence of multiple notification types for a single booking is possible.
* In some environments, **notification acknowledgment** features may be added to track who resolved what (if enabled).
