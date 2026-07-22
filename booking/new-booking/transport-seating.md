---
description: >-
  Assign and manage seat allocation in Tourpaq Office bookings. Select outbound
  and return flight seats per passenger, save assignments, and print tickets
  with seat numbers.
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
  actions:
    visible: true
---

# Transport Seating

### **Overview**

The **Transport Seating** tab in **Tourpaq Office** is used to manage **seat allocation** for flights in a booking. Assign airplane seats per passenger manually (or automatically, if enabled). It supports both outbound and return flights and prints seat numbers on tickets.

***

### **Purpose**

* Reserve specific airplane seats for each passenger in a booking.
* Allow agents to match customer seating preferences where possible.
* Display seat numbers on tickets and other booking documents.

***

### **Preconditions**

* The booking must be created and saved.
* Passengers must already be added to the booking.
* The transport (flight) must be configured with seat data (otherwise seats cannot be selected).

{% hint style="info" %}
If you cannot select seats, the issue is often related to setup. See:

* [**Seating**](../../seating/) (Seat List / Assign Seats)
* [**Seat Types**](../../seating/seat-types.md)
* [**Transport Layouts**](../../transport-layouts.md)
* [**Automatic Seating**](../../transport/transport/automatic-seating.md) (if you rely on automatic placement)
{% endhint %}

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (42).png" alt="Transport Seating tab showing seat map and passenger seat assignments for a booking"><figcaption></figcaption></figure>

### **Instructions**

#### **Accessing the tab**

1. Open the booking.
2. When the booking contains at least one passenger and a flight segment, the **Transport Seating** tab becomes available.
3. Click the **Transport Seating** tab.

***

#### **Outbound flight seat assignment**

1. Open the **Outbound** tab (the first tab).
2. Assign seats by clicking on **available** seats (commonly marked as free/green).
3. Select seats for each passenger.
4. Click **Save passenger assignment for outbound**.

***

#### **Homebound (return) flight seat assignment**

1. Open the **Homebound** tab (the second tab).
2. Assign seats by either:
   * Selecting seats manually (same method as outbound), or
   * Using the option to **auto-select the same seats as outbound** (if available in your setup).
3. Click **Save passenger assignment for homebound**.

***

#### **Final steps**

1. Click **Save** to confirm all seat assignments.
2. Return to the **Booking** tab.
3. Verify that the booking now shows the assigned seats (a seating-related column/field may appear depending on your layout).
4. Click **Print Ticket**.
5. Check the ticket – it should include a **Flight Reservation** section listing the selected seats for both outbound and homebound flights.
