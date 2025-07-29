# Allotments

### **Manual**

Is usually used for products available at the destination. The user can generate allotments when the product is available by using a simple generator. In the booking the system will display the product as available for all extra allotments that are between arrival and departure date and if there is still allotment.

Example:

* Product allotment: 01/08, 03/08, 07/08, 10/08
* Charter: arrival 01/08. dep 08/08 there will be possible to book this extras for 01/08, 03/08, 07/08
* OWO: flight on 01/08 there will be possible to book this extra for 01/08
* OWH: flight 08/08 - there will not be possible to book the extra
* CT: same as charter

### **Linked to transport**

Is usually used for products available at the transport (eg bag, catering). The user can generate allotments to match departure dates of a transport. The allotment can be split by interval. The system will display the product available if there is allotment for selected interval.

Linked to Transport Allotment is an extra allotment type given only to passengers travelling with a given transport and using allotments defined for it. This is due mainly because the extra is available only for a certain period and in limited supply.

To use it properly the user must create a new extra and select **Linked to transport**.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

After the general settings have been set, and the extra saved, the next step is setting the brand and establishing the prices and resources. At the **Resource** tab, a must is setting the **Transport** filter.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (2) (1).png" alt=""><figcaption></figcaption></figure>

The next step is setting up the allotments.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

As long as the transport resource is selected, there is no need for a start and end date, these beeing defined by the transport fix quota. When setting the number of products (Al1/Al2/Al3/Al4), the user must take into account that the values will be summed up. For example, if, Al1=30, Al2=20, AI3=10 and the rest are 0, the total sum will be 60.

Note! The extra allotments are set up as the transport allotments. The allotment must be edited by an user or overbookings may happen.

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* AI1-AI4 = allotments for intervals 1-4
* TOTAL OUT = allotments total for departures
* URET = allotments for return flights
* BI1-BI4 = products booked for intervals 1-4
* BOUT = total products booked for departures
* BRET = total products booked for return
* FO1-FO4 = free allotments for intervals 1-4

#### **Calculation for Allotment:**

* Calculation for TOTAL OUT

The Total Out is calculated as a sum from the departures: TO = AI1 + AI2 + AI3 + AI4

* Calculation for URET

The URET is calculated as a sum from the departures, but taken diagonally like in the screenshot below:

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Special case for extras that are from a category that has the **"link to column in transport"** enabled

For these extras, the allotment total and calculation is displayed also on transport selection pop-up in the booking process. All extras linked to the transport will be taken in consideration when displaying the total, no matter if there are more from the same category or different categories.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/LinkedToTransport-9c2183e4a9db0582d6849ed7fee00404.png" alt=""><figcaption></figcaption></figure>

### **One way usage**

For ONE WAY flights, another extras is required, as extras are not available for ONE WAYS unless a specific action is taken, action that will invalidate the extra for CHARTER flights.
