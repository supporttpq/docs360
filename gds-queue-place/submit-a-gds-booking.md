# Submit a GDS Booking

#### **Overview**

The first phase of the **GDS flight booking process** follows the same logic as for **Charter Transport**.\
The process ensures that flight availability, pricing, and ticketing rules are correctly handled through the integrated GDS system.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### **Booking Phase**

When the **Take Allotment** button is used, the system checks whether:

1. The flight configured for the selected transport and departure is **still available**.
2. The **price** of the flight has **not changed**.

* If the **price is higher**, the user is prompted to confirm whether to continue.
* If the **flight is no longer available**, the system automatically searches for a new flight and displays it for user approval.

Once a booking is made, it moves to the **GDS Pending** status.

***

#### **Submission to GDS**

In the **GDS Pending** phase, the **GDS tab** in the booking window can be used to **submit the booking to the GDS provider**.

Depending on internal payment rules, some users might be **restricted from submitting** the booking until certain payments are completed.\
When submission is initiated, the same checks made during the “Take Allotment” step are repeated, and the results from the GDS are displayed to the user.

***

#### **Low-Cost Carriers**

If the selected flight belongs to a **low-cost carrier**, the booking automatically moves to T**icketOK** status.\
In this case, the **ticket is generated directly by the airline**, and no further submission or ticketing step is required.

![!](https://docs.tourpaq.com/assets/images/7-999dd91587d10624ff9fcebbe27de7e1.png)

#### **Galileo Flights**

For **Galileo flights**, an additional **ticketing step** is required.

* When submitting the booking, a **ticketing limit** is applied according to the system configuration.
* If the flight is still available, the booking moves to **Hold and Confirmed** status (all segments in HK status).
* If **ticketing is not completed** before the ticketing limit expires, the **booking is automatically canceled by Galileo**.

Unlike other GDS bookings, **submission to Galileo** can be done **without waiting for payment**.\
However, **ticket requests** are only allowed **after payment has been received**. Once payment is registered, the user can use the **GDS tab** to send the ticket request.

![!](https://docs.tourpaq.com/assets/images/8-eec6d592779e58b0e1b5a14ba4bd4ab2.png)

#### **Expected Behavior**

* The system automatically checks availability and price consistency before confirming or submitting any GDS booking.
* Any change in flight price prompts the user to confirm continuation.
* Bookings for low-cost carriers are confirmed immediately and set to **TicketOK** status.
* Galileo bookings require a separate ticketing step and are automatically canceled if ticketing is not completed before the deadline.
* GDS submission and ticketing follow the configured payment validation rules.

***

#### **Customer Outcome**

* Users can handle GDS bookings following the same logic as Charter Transport bookings, minimizing the learning curve.
* The system ensures accurate booking and ticketing synchronization with external GDS providers.
* Payment-dependent restrictions prevent unintentional ticketing before customer payment.
* Automatic cancellation of unticketed Galileo bookings avoids financial or operational inconsistencies.

#### **Notes / Important**

* The booking and ticketing flow may vary slightly depending on the **GDS provider** (e.g., **Galileo**, **Amadeus**).
* **Ticketing deadlines** and **automatic cancellation logic** are controlled by the GDS system and may differ per airline.
* System administrators can configure provider-specific behavior and payment rules in the GDS setup module.
* It is recommended to always verify ticketing deadlines and confirm payments before final submission.
