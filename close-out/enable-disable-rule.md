# Enable / Disable rule

### **Overview**

Close Out rules provide a mechanism to control **Free Hotel Allotment (FHA)** in price lists. By enabling a rule, the system cuts down FHA to zero for all hotels and rooms included in the rule. When the rule is disabled, FHA is restored to the current free allotment as defined in the hotel configuration.

This functionality ensures that hotel availability is correctly managed in alignment with operational requirements such as stop sales or capacity restrictions.

***

### **Rule Enablement**

When the **Enabled** checkbox of a rule is selected and saved:

* The rule is marked as active.
* Backend services are triggered to update the price list.
* Within \~2 minutes, **FHA is set to 0** for all rooms of the hotels included in the rule.

#### **Examples**

1. **Rule set on transport + resort**
   * All Price List Tables (PLTAs) from the corresponding period, created with that transport and hotels from the resort, will have FHA = 0.
2. **Rule set only on a resort (no transport)**
   * All PLTAs from the corresponding period, created with hotels from the resort and **all transports**, will have FHA = 0.

***

### **Rule Disablement**

When the **Enabled** checkbox of a rule is deselected and saved:

* The rule is marked as inactive.
* The **Stop Sale Resort service** restores FHA values on the price list.
* Within \~2 minutes, FHA is reset to the current free allotment defined for each hotel/room.

#### **Examples**

1. **Rule set on transport + resort**
   * All PLTAs from the corresponding period, created with that transport and hotels from the resort, will have FHA restored to their configured hotel/room allotments.
2. **Rule set only on a resort (no transport)**
   * All PLTAs from the corresponding period, created with hotels from the resort and **all transports**, will have FHA restored to their configured hotel/room allotments.

***

### **Key Notes**

* Updates take up to 2 minutes to be reflected in price lists.
* FHA values always reset to the **current hotel configuration** when a rule is disabled.
* Rules should be created with precise scope (transport, resort, hotel) to avoid unintentionally blocking or restoring availability across multiple areas.
