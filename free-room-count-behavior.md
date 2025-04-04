# Free room count behavior

This feature handles the recalculation of the free hotel allotment number of a pricelist rule. \\

> **Please note!** Free room count value **will not be recomputed** on a pricelist that has no sale value set (any of the P1, P2, D1, etc..)

If the number on the pricelist is not greater than 0, then the offer will be listed on the agency presentation site, cannot be booked on Web Booking or Office. In the same time, because of large number of pricelist rules, they cannot be all (re)compute instantly this number.

#### **That is why a queue is used in Tourpaq.**

When updating hotel allotment values this queue collects all the pricelists that should update free room count. The system then starts recomputing the free room values of each. It can take several seconds or more minutes, depending of the extent of the updated interval and number of transports and agencies of the company selling that room. The wait duration can be estimated between 2 and 15 minutes. If after 15 minutes the free room count in pricelist rule is not recalculated, we can consider this a suspicious situation that needs to be investigated.

**Exception from the queued recalculation**

When placing a booking, canceling one, or replacing a room in a booking, the effect is updating the booked/free room allotment. This is visible in the edit hotel page, hotel allotment per day tab. \ This update should also trigger the pricelist rule free hotel room count number recalculation. \\

At the moment, the exact pricelist rule that is being used/canceled/released by being replaced in the booking will be updated **instantly**. No queue is involved here. This means that the **exact same** pricelist rule can be booked seconds after.

> **Please note!** As of this document's date, other pricelist rules that sell the same hotel room as above (but with other transports) are not being instantly updated. They are still being recalculated via a queue and will take some time to be observed.

#### **Manual recalculation**

A manual recalculation of a pricelist rule free room count values can be triggered by clicking on the magic wand icon highlighted bellow. The recalculation should be instant.

<figure><img src=".gitbook/assets/image (64) (1).png" alt=""><figcaption></figcaption></figure>
