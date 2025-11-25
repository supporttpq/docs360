# Discount Extra Beds

### Overview

The **Extra Bed Discounts** feature allows administrators to define discounts specifically for rooms with extra beds. These discounts can be applied to children or adults depending on age and can be customized for multiple extra beds per room.

### **Purpose**

The purpose of the **Discount Extra Beds** section is to:

* Offer flexible discounting options for additional bed usage
* Automate price reductions for extra occupants
* Allow discounts that vary by age, stay period, booking period, or room type
* Support multiple transports and stay periods
* Ensure consistency across seasons and product configurations

This reduces manual adjustments and ensures accurate price calculations in the booking engine.

<figure><img src="../../.gitbook/assets/image (508).png" alt=""><figcaption></figcaption></figure>

### Field Explanations

1. **Age** – The age of the guest for which the discount is applied. Typically used for children.
2. **Start Date / End Date** – The validity period during which the discount is applied.
3. **Booking Start / End Date -** Booking interval. Only bookings created within the set interval will be applied the extra bed discount
4. **Discount Values**
   * **1st Column** – Discount applied to the first extra bed.
   * **2nd Column** – Discount applied to the second extra bed in a room (optional).
   * **3rd Column** – Discount applied to the third extra bed in a room (optional).
5. **Percent Checkbox** – When checked, the discount is applied as a percentage (e.g., 10%).
6. **Discount Type Options**
   * **FHC** – Extra bed discount calculated from profit (works with Price Margin Service).
   * **H (Hidden)** – The average discount per passenger per room is added to each passenger in the room.
   * **HP (Hotel Price)** – Percentage applied from the hotel price.
   * **PD (Per Day)** – When checked, the discount value is applied per day instead of per interval.
7. **Room Type** – Select the room(s) for which the discount applies.
8. **Transports** – Select transport(s) to which the discount may apply.
9. **Period** – Defines the transport intervals or periods for which the discount is valid.
10. Delete Icon - Removes the discount line.
11. Create - Adds new discount line.
12. Removed Discounts - Shows previously removed rules for audit or restoration.

    <figure><img src="../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure>


13. Show All - Displays all discount rows regardless of filtering.

***

### Instructions for Use

1. Navigate to the **Extra Bed Discounts** section in the Hotel Menu.
2. Click **Create** to create a new discount entry.
3. **Define age ranges -** Set the age interval(s) that qualify for the extra bed discounts (e.g., children 2–11 years).
4. **Set valid stay dates -** These are the dates when the discounted stay must occur.
5. **Set booking dates -** Fields allowing discounts only for bookings created between specific dates.
6. **Enter discount values -** You can specify:
   * **Discount 1st Extra Bed**
   * **Discount 2nd Extra Bed**
   * **Discount 3rd Extra Bed**
   * **Discount 4th Extra Bed**
   * Optionally mark discount as **percentage** (%).
7. **Select the discount type option -** Choose whether the discount applies to:
   * **FHC** – Extra bed discount calculated from profit (works with Price Margin Service).
   * **H (Hidden)** – The average discount per passenger per room is added to each passenger in the room.
   * **HP (Hotel Price)** – Percentage applied from the hotel price.
   * **PD (Per Day)** – When checked, the discount value is applied per day instead of per interval.
8. **Select Room Types -** Discount rules can be limited to specific rooms or applied to all rooms.
9. **Select Transports -** Each discount rule can be tied to one or more transport codes.
10. **Choose Period -** Select which price period the discount belongs to.
11. Save the discount. It will now be applied automatically when the booking meets the defined criteria.

Once configured, the system automatically calculates and applies the appropriate discount when a booking meets all criteria.

### **Example Use Case**

A hotel gives the following discounts for children:

* Ages **2–11**
* Valid for stays from **01-01-2025 to 31-12-2025**
* Booking period between **01-07-2024 and 01-12-2025**
* First child: **2000 DKK discount**
* Only applies to **CPHKGS70** transport
* Valid for all room types
* Assigned to **Period 1**



