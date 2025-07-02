# Remove pax on outbound or homebound only

### **Overview**

This page shows the correct behavior of the "No-show" functionality when removing a passenger (pax) from either the outbound or homebound segment of a trip within a booking. The functionality allows setting a passenger as a "No-show" for a specific flight without altering the rest of the booking and ensures consistent data handling even when transport changes occur.

### **Purpose**

The purpose of this page is to ensure that:

* The "No-show" checkbox can be individually set per passenger and flight segment.
* The state of the "No-show" checkbox remains unchanged when editing the booking (as long as the transport for the passenger remains unchanged).
* When a transport is changed, the system treats the change as new data and the "No-show" setting is cleared accordingly.

### **Preconditions**

* Access to the booking module is required.
* A booking must either already exist or be created for testing.
* The user must have access rights to view and modify travel plans.

### **Test Steps and Expected Results**

| **Steps**                                                                                  | **Expected Results**                                                                                                                                                                                                                         |                                                                                                                            |
| ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| 1. Create a new booking or edit an existing one                                            | The edit page of the booking is displayed.                                                                                                                                                                                                   | <div><figure><img src="../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>     |
| 2. In the "Details" part, go to the **Travelplan** tab                                     | A new **"No-show"** column appears with a checkbox for each line in the travel plan. The default state is **not enabled**. Each line shows flight data per passenger, allowing the "No-show" status to be independently set for each flight. | <div><figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div> |
| 3. Set the **"No-show"** checkbox for the desired passenger and flight                     | The checkbox is set. No "Save" action is required. It's also not necessary to edit the passenger individually to enable "No-show".                                                                                                           | <div><figure><img src="../../../.gitbook/assets/image (2) (1) (3).png" alt=""><figcaption></figcaption></figure></div>     |
| 4. Edit the booking without changing the transport for the passenger                       | The already set **"No-show"** checkbox remains set and unchanged.                                                                                                                                                                            | <div><figure><img src="../../../.gitbook/assets/image (4) (3).png" alt=""><figcaption></figcaption></figure></div>         |
| 5. Edit the booking with a change in transport (e.g., flight date, transport, or interval) | The **"No-show"** checkbox will be cleared, treating the transport as new data.                                                                                                                                                              | <div><figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure></div>             |

### **Notes**

* This page ensures that the **No-show** status is preserved under stable transport conditions.
* Transport updates are treated as a new context for the passenger, and therefore previous "No-show" flags are removed to reflect the updated itinerary.
