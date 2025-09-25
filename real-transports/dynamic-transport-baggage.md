# Dynamic transport baggage

### **Overview / Purpose**

The **Dynamic Transport Baggage** feature allows the system to automatically reserve baggage for flights, particularly for **ACH / Low Cost Carriers**, and ensures that baggage information is visible in the Office interface (including 1G flights). This helps streamline booking management and ensures accurate pricing and inventory for flights.

### **How to Activate**

1. Navigate to the **Legs** tab of the relevant dynamic transport.
2. In the **General Dynamic Information** section, check the **Dynamic Baggage** checkbox.
3. Update the flights for this transport.
   * This allows the service to detect, include, and price baggage for each flight.

<figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

### **How It Works**

* Once activated, the system automatically retrieves baggage information for each airline, including:
  * **Price**
  * **Quantity / Allowance**
* This data is saved in memory and added to the flight price.
* Baggage details are displayed in:
  * **Test Search** (from `Configure -> Leg`)
  * **View Flights** (from `Fix Quota`)

**"Test Search"**

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

**"View Flights"**

1. **Take Allotment**: Baggage prices are verified again when the booking is made.
2. **GDS Tab**: Baggage is booked as an optional service when the booking is created.
3. **Successfully Submitted Bookings**: The booked baggage is displayed in the Office system.
4. **Load PNR**: Optional services, including baggage, are loaded again to ensure consistency.

### **Key Benefits**

* Automatic baggage pricing and inventory management.
* Reduces errors and manual input for low-cost carrier bookings.
* Ensures baggage is accurately displayed for office users and bookings.
