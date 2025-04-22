# Free room count behavior

This feature handles the recalculation of the free hotel allotment number of a price list rule.&#x20;

> **Please note!** Free room count value **will not be recomputed** on a pricelist that has no sale value set (any of the P1, P2, D1, etc..)

If the number on the price list is not greater than 0, then the offer will be listed on the agency presentation site and cannot be booked on Web Booking or Office. In the same time, because of the large number of pricelist rules, they cannot all (re)compute this number instantly.

#### **That is why a queue is used in Tourpaq.**

When updating hotel allotment values, this queue collects all the price lists that should update the free room count. The system then starts recomputing the free room values of each. It can take several seconds or more minutes, depending on the extent of the updated interval and the number of transports and agencies of the company selling that room. The wait duration can be estimated between 2 and 15 minutes. If after 15 minutes the free room count in the price list rule is not recalculated, we can consider this a suspicious situation that needs to be investigated.

**Exception from the queued recalculation**

When placing a booking, canceling one, or replacing a room in a booking, the effect is updating the booked/free room allotment. This is visible in the edit hotel page, hotel allotment per day tab. \ This update should also trigger the pricelist rule free hotel room count number recalculation. \\

At the moment, the exact price list rule that is being used/canceled/released by being replaced in the booking will be updated **instantly**. No queue is involved here. This means that the **exact same** price list rule can be booked seconds after.

> **Please note!** As of this document's date, other pricelist rules that sell the same hotel room as above (but with other transports) are not being instantly updated. They are still being recalculated via a queue and will take some time to be observed.

#### **Manual recalculation**

A manual recalculation of a price list rule's free room count values can be triggered by clicking on the magic wand icon highlighted below. The recalculation should be instant.

<figure><img src=".gitbook/assets/image (64) (1).png" alt=""><figcaption></figcaption></figure>
