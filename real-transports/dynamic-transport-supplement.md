# Dynamic transport supplement

### **Overview / Purpose**

The **Dynamic Transport Supplement (DTS)** feature allows the system to secure the cheapest available flight for a departure, even if its price exceeds the maximum transport price set for that departure. Instead of blocking the booking, the price difference is automatically converted into a **supplement per passenger**, ensuring flexibility and accurate cost handling.

This prevents missed sales opportunities caused by strict maximum price limits while maintaining transparency in pricing.

### **How to Activate**

* This feature applies **only to dynamic transports**.

1. Go to the **Legs** tab.
2. In the **General Dynamic Information** section, check the **Dynamic Supplement** checkbox.
3. Update the flights for the selected transport.
   * This step ensures the service finds the cheapest flights while ignoring the "Max return price per person from GDS" restriction.

### **How It Works**

1. After activation, the service scans for the cheapest flights linked to the transport, ignoring the maximum price limit.
2. These flights are saved into the database.
3. When a booking is created and passengers are saved via **Take Allotment**:
   * A dynamic supplement (`DTS`) from category `DT` is automatically added per passenger.
   * The supplement amount represents the **difference between the real flight price and the maximum set transport price**.

#### **Supplement Details**

* **Code:** `DTS`
* **Category:** `DT`
* These values are **manually added per company** and are **mandatory** (cannot be deleted).

### **Calculation Rules**

#### **Charter Transport**

* **Transport Cost = 0**
* **DTS Cost = Real Transport Price**

#### **GDS Transport**

* DTS is calculated against the **Max return price per person from GDS**.
* Example:
  * Max return price per person (from GDS): **100 DKK**
  * Real flight price: **1720 DKK**
  * **Transport Cost = 100 DKK** (the defined maximum)
  * **DTS Price = 1720 – 100 = 1620 DKK**
  * **AlternativeCost = 1620 DKK**
  * **Passenger Table → TransportGDSCost = 100 DKK**

### **Key Benefits**

* Ensures the cheapest flights are always available, even when above max. transport price.
* Automatically balances costs with transparent supplements per passenger.
* Works seamlessly with both **Charter** and **GDS** transports.
