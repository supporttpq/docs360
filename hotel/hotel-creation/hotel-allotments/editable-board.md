# Editable Board

### Overview

This functionality defines how **Board Basis (meal plan)** behaves in relation to bookings, hotel allotments, and products.

The key principle is that the **board basis is stored at booking level (BPLTA)** at the moment the booking is created and is **not dynamically updated** when the hotel configuration changes later.

***

### Purpose

* Ensure pricing and product consistency after booking creation
* Prevent unexpected changes caused by hotel configuration updates
* Control product availability based on board compatibility
* Maintain a stable reference point (BPLTA) for board basis

***

### Preconditions

Before testing or using this functionality, ensure the following:

1. A hotel is configured with:
   * Hotel → Allotment → **Board Basis** set on relevant rooms
2. At least one product exists with:
   * **Board Type matching** the hotel allotment board basis
3. A booking is created:
   * The **board type is saved in BPLTA** at creation time
4. A product is assigned:
   * Must have the **same board type** as the hotel allotment

***

### Core Concept

* The **BPLTA (Booking Product Line Travel Allocation)** stores the board basis at booking creation
* This stored value is the **reference point for product availability**
* Changes in hotel configuration do **not retroactively affect existing bookings**

***

### Test Scenarios and Expected Behavior

#### 1. Change Board Basis in Hotel Allotment

**Action:**\
Modify the board basis in Hotel → Allotment

**Expected Result:**

* No impact on existing bookings
* Booking continues using the **original board basis stored in BPLTA**

The booking is already "locked" to the board basis at creation time.

***

#### 2. Change Product Board Type

**Action:** Modify the product so that its board type no longer matches the booking

**Expected Result:** Product becomes **unavailable** for the booking

Product availability depends on matching:

* Product Board Type
* Booking Board Basis (from BPLTA)

***

#### 3. Change Room and Re-Take Allotment

**Action:**

* Change room to one with a different board basis
* Click **Take Allotment**

**Expected Result:**

* A **new BPLTA is created**
* Booking board basis is updated accordingly
* Available products are recalculated based on the new board

Taking allotment refreshes the booking’s board basis reference.

***

### Behavior Summary

| Action                       | Impact on Booking | Impact on Products             |
| ---------------------------- | ----------------- | ------------------------------ |
| Change hotel allotment board | No change         | No change                      |
| Change product board type    | No change         | Product may become unavailable |
| Change room + Take allotment | Updates BPLTA     | Products recalculated          |

***

### Important Notes

* Board basis is **not dynamically linked** after booking creation
* Product availability is **strictly dependent on board matching**
* “Take Allotment” acts as a **reset/recalculation mechanism**
* This prevents inconsistencies in pricing and service delivery

***

### Best Practices

* Ensure correct board basis before creating bookings
* Avoid changing product board types during active sales
* Use **Take Allotment** when changing rooms to refresh availability
* Validate product compatibility after any room or board change

***

### Summary

The system ensures stability by storing the board basis at booking level (BPLTA).\
Hotel configuration changes do not affect existing bookings, while product availability is dynamically validated against the stored board.

This approach guarantees consistent pricing and avoids unintended side effects in active bookings.
