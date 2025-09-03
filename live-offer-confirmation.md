# Live Offer Confirmation

### 📌 Overview

The **Live Offer Confirmation** interface is used to **monitor and manage reservation confirmations** in real-time, especially after offers have been sent and accepted by customers. It provides detailed insight into whether each booking has been successfully processed by both the **travel provider** and **Tourpaq**.

***

### 🎯 Purpose

This tool is essential for:

* **Tracking the confirmation status** of bookings sent to providers and Tourpaq.
* **Identifying and resolving failed bookings** quickly.
* Ensuring that all customer reservations are fully validated before proceeding with final booking stages.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 🧭 Interface Explanation & Instructions

#### 🔍 Booking Period Filters

* **Start Date / End Date**
  * Set the period for which you want to see booking confirmations.
* **Display Button**
  * Applies the selected date range and filter settings.
* **More Filters Button**
  * Expands the interface to allow additional criteria for more refined searches (e.g., by agency or hotel).
* **Clear Button**
  * Resets all filters and date ranges to their default values.

***

#### ✅ Reservation Status Filters (Checkboxes)

Use these checkboxes to filter the reservation list by status:

| Checkbox                              | Description                                                                                               |
| ------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **Failed Provider Reservation**       | Shows bookings where the external provider failed to confirm the reservation. Useful for troubleshooting. |
| **Tourpaq Pending Reservation**       | Displays bookings that are still awaiting confirmation from Tourpaq.                                      |
| **Successfully Provider Reservation** | Filters bookings that have been successfully confirmed by the external provider.                          |
| **Successfully Tourpaq Reservation**  | Filters bookings confirmed on the Tourpaq side. Ensures double-confirmation.                              |

***

#### 📊 Reservation Table Columns

Below the filter area, a table displays detailed booking entries:

| Column                   | Description                                                            |
| ------------------------ | ---------------------------------------------------------------------- |
| **Reservation ID**       | System-generated unique ID for the reservation.                        |
| **Booking No.**          | Internal booking reference number.                                     |
| **Hotel**                | Name of the hotel selected in the offer.                               |
| **Transport**            | Status or description of the transport (e.g., "No Transport").         |
| **Departure/Check-In**   | The departure date or hotel check-in date.                             |
| **Booking Date**         | Date when the booking was made in the system.                          |
| **Customer**             | Name of the customer associated with the booking.                      |
| **Phone**                | Customer's phone number.                                               |
| **Email**                | Customer's email address.                                              |
| **Pax No.**              | Total number of passengers in the booking.                             |
| **Total**                | Total value of the reservation, including taxes and optional services. |
| **Agency**               | The travel agency that initiated and confirmed the booking.            |
| **Transaction Status**   | Shows whether the payment has been **successfully captured**.          |
| **Provider Reservation** | ✅ if confirmed by provider, ❌ if failed.                               |
| **Tourpaq Reservation**  | ✅ if confirmed in Tourpaq, ❌ if still pending or failed.               |

***

### 🔄 Workflow & Usage Tips

1. **Use the date filters** to narrow down recent confirmations or troubleshoot specific date ranges.
2. **Check "Failed Provider Reservation"** regularly to identify problems early.
3. **Confirm both Tourpaq and Provider statuses** to ensure full booking validation.
4. **Sort by Booking Date or Total** to prioritize high-value or recent reservations.
