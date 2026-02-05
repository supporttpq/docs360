# Add Transport Type and Transport Mode to Extras Resources

### Overview

Extras can be linked to transport resources to control when and how they are available during booking. To support selling products such as golf bags, infant prices, or seating on Dynamic Packages without triggering ancillaries in Amadeus, Extras Resources now support filtering by **Transport Type** and **Transport Mode**.

This allows precise control over which extras apply to which transport scenarios.

### Purpose

Transport Type and Transport Mode allow you to control **when an extra is available**, based on the transport used in the booking.

This enables:

* Selling extras on Dynamic Packages without sending ancillaries to Amadeus
* Differentiating between Charter, GDS, and other system transports
* Distinguishing between flight-based and non-flight-based dynamic transports

### **Transport Type**

Transport Type limits an extra so it is available only when the booking contains a matching transport type.

If the transport in the booking does not match the selected Transport Type, the extra is not offered.

Example

* Transfer used only for Charter\
  Transport Type = Sys-Real
* Transfer used only for GDS flights\
  Transport Type = System

### **Transport Mode**

Transport Mode adds an additional filter for dynamic transports.\
It allows you to distinguish between different types of transport, such as flights or car-based transport.

Transport Mode is evaluated only when the selected Transport Type supports dynamic behavior.

Supported Values

* FLY
* CAR
* BUS
* TRAIN

Example

* **Transfer only for Charter**
  * Transport Type = Sys-Real
* **Transfer only for GDS / Dynamic Flight**
  * Transport Type = System
  * Transport Mode = FLY

### How to Configure Transport Type and Mode for an Extra

1. Go to **Extras Setup > Extras**.
2. Open the extra you want to configure.
3. Navigate to the **Resources** section.
4. Use the **Transport Type** filter to select one or more transport types.
5. If needed, use the **Transport Mode** filter to further limit availability.
6. Save the extra.

### Using Excluded Values

Both Transport Type and Transport Mode support **Use as Excluded**.

When enabled, the extra will be available for all transport types or modes **except** the selected ones.

### Important Notes

* Both filters support multiple selections.
* If no Transport Type is selected, the extra is available for all transport types.
* Transport Mode has no effect unless a compatible Transport Type is selected.
* These settings help prevent extras from being sent as ancillaries in Amadeus.
