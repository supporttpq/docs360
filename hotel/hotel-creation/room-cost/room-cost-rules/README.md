---
description: >-
  Configure base hotel room cost rules, stay types, filters, and validation
  steps.
---

# Room Cost Rules

### **Overview**

Room Cost Rules define the base cost your agency pays the hotel. They define how cost is calculated and when it changes.

### **Purpose**

Use Room Cost Rules to keep hotel costs correct across scenarios. Use thresholds to switch cost after a number of rooms are sold.

<figure><img src="https://tourpaq.gitbook.io/staging-tourpaq-docs/~gitbook/image?url=https%3A%2F%2F1539646852-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FZCqO8EQ5P5Mioq1zbQAc%252Fuploads%252Fy5ANj4em8WY2Wgrn0b4y%252Fimage.png%3Falt%3Dmedia%26token%3D32be6850-1417-4197-be48-4261791da3e6&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=3dbebddc&#x26;sv=2" alt=""><figcaption></figcaption></figure>

### **How it works**

* **Stay Type** (from the _Stay Type_ dropdown):
  * **Per Room Per Night**
    * The amount is split between passengers in the room.
    * The rule applies per night within the stay period.
    * It can apply on overlapping days within the booking.
  * **Per PAX Per Room**
    * The amount applies per passenger.
  * **Per Room Per Stay**
    * The amount is split across passengers and stay days.
    * The rule applies when arrival is inside the stay interval.
* **Single Price**
  * Adds an extra amount when a room has exactly one passenger.
* **Extra Cost Included**:
  * Subtracts **Extra Cost Included** from **Price**.
  * This happens only when Early Booking or Stay & Pay applies.

**Filters** Rules can be restricted based on the following conditions:

* Stay start and end dates
* Booking start and end dates
* Room type

**Changing Costs Based on Number of Rooms Sold** It is possible to adjust room costs dynamically using the **Up to rooms** and **Price2** fields:

* If **Up to rooms** is set, the system switches to **Price2** after the threshold.

### Related pages

* [Room cost](../)
* [Add room cost rule with "Per Room Per Stay" type](add-room-cost-rule-with-per-room-per-stay-type.md)
* [Add room cost rule with "Per Room Per Stay" with a specific stay days value](add-room-cost-rule-with-per-room-per-stay-with-a-specific-stay-days-value.md)
