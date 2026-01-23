# Transport Seating

### **Overview**

The **Transport Seating** tab is used to manually (or, where supported, automatically) assign airplane seats to passengers in a booking. It supports both outbound and return flights and ensures that seat assignments are visible on the booking and on the printed ticket.

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

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (3).png" alt=""><figcaption></figcaption></figure>

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

***

### **FAQ**

#### **Why can’t I select any seats?**

Common reasons:

* The flight is not configured with seat data, so no seats are available to choose.
* The booking is not fully saved or passengers are missing.
* Seats are already taken or not released for selection.

**Where to fix it (setup pages):**

* Check that a seat map exists and seats are defined in [**Seating**](../../seating/) (Seat List / Assign Seats).
* Check that the flight/transport has a layout assigned in [**Transport Layouts**](../../transport-layouts.md).
* Check that the seat categories used by the layout exist in [**Seat Types**](../../seating/seat-types.md).

If your organisation uses automatic seat placement, also review [**Automatic Seating**](../../transport/transport/automatic-seating.md).

***

#### **What does “auto-select the same seats as outbound” do?**

It attempts to assign the **same seat numbers** on the return flight as on the outbound flight. This can save time and keep seating consistent, but it only works when the same seats exist and are available on the homebound flight.

***

#### **Do seat assignments automatically appear on the ticket?**

Seat assignments appear on the ticket after they are saved. If the seats do not show up:

* Make sure you clicked the relevant **Save passenger assignment** buttons for outbound/homebound.
* Click **Save** on the page to confirm.
* Reprint or preview the ticket again.

***

#### **Can I change seats after assigning them?**

Yes. Reopen **Transport Seating**, update the seat selections, and save again. Then reprint the ticket to ensure the updated seats are shown on customer documents.
