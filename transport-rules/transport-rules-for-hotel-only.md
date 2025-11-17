# Transport Rules for Hotel Only

### **Overview**

Some tour operators offer **Hotel Only** products where guests travel using their **own transport** (car).\
Guests may arrive on any weekday and stay for various durations (often **up to 28 nights or more**).

To support this, Tourpaq uses **Transport Rules**, even when no actual transport is provided.\
Transport Rules define:

* Valid arrival days
* Valid stay durations
* Valid travel period
* Departure & arrival gateways
* Transport mode (**CAR**)

These rules automatically generate the internal “departures” needed for booking validation and hotel allotment matching.

***

### **Purpose**

Transport Rules allow Tourpaq to support Hotel Only scenarios by:

* Creating all required travel combinations
* Ensuring bookings always match hotel allotment
* Allowing flexible travel dates across the entire season
* Avoiding manual creation of each duration/day combination
* Making Hotel Only setup identical across multiple hotels and seasons

This structure ensures **Hotel Only products behave like normal packages**, but without flights.

***

### **Recommended Setup**

#### ✔ Use a dedicated Departure Gateway: **OWN**&#x20;

Although not required, it is **strongly recommended** to create a dedicated departure gateway:

* **Code:** OWN
* **Name:** Own Transport / Self-transport
* **Purpose:** Indicate the customer is traveling independently

#### Benefits of using “OWN”

* Cleaner reporting
* Clearer customer communication (“Own transport”)
* Avoids mixing with flight or bus gateways
* No risk of incorrect GDS or Paxport connections
* Easy to filter Hotel Only products

***

### **How It Works**

When a Transport Rule is created for Hotel Only:

1. Define **departure = OWN** and **transport mode = CAR**.
2. Define a **season date range**.
3. Tourpaq automatically generates the required “departures”, one for each combination.

These departures behave like real transport for the booking engine, but represent **hotel stays only**.

***

<figure><img src="../.gitbook/assets/image (496).png" alt=""><figcaption></figcaption></figure>

#### Key fields:

#### **General**

| Field                   | Description                                         |
| ----------------------- | --------------------------------------------------- |
| **Code**                | Name of the rule (e.g., OWN CAR)                    |
| **Date From / Date To** | Valid travel season                                 |
| **Departure**           | Select **OWN – Own transport**                      |
| **Arrival**             | Select arrival destination closest to the hotel     |
| **Stay Days**           | Add all allowed durations (e.g., 04D, 07D, 10D…)    |
| **Allotment**           | Min allotment per duration (set to 0 or any number) |

#### **Transportation Section**

| Field                        | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| **Pick-up point required**   | For Hotel Only, leave **unchecked**             |
| **Travel Length Correction** | Optional shift if arrival/departure days differ |
| **Shift check-in date**      | Optional, usually leave blank                   |
| **Hotel nights correction**  | Adjusts number of hotel nights if needed        |
| **Transport mode**           | Select **CAR**, recommended                     |

#### **Outbound / Homebound**

For Hotel Only:

* **Transport Type** need be set to _ExternalProvider_
* the other settings will be made similarly to other modes of transport

### **When to Use This Setup**

Use Hotel Only Transport Rules when:

✔ Hotel products are sold without flights\
✔ Guests travel by car or arrange their own transport\
✔ You need 10–30 different stay durations\
✔ You want to avoid manual creation of separate transports\
✔ You want clean reporting & clear customer messaging

***

### **Summary**

Transport Rules provide a powerful and flexible way to support **Hotel Only** products. By using a dedicated **OWN** departure gateway and adding multiple stay durations, you can support **28+ stay days** quickly and efficiently.

✔ Recommended: **OWN** departure gateway\
✔ Recommended: **Transport mode = CAR**\
✔ Works with all booking flows\
✔ Minimal setup required
