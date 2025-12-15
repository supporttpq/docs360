# Edit Passenger - FAQ

## Edit Passenger - FAQ

This FAQ complements the [Passengers Tab](edit-pas.md) documentation and focuses on common questions when editing travelers and customer contact details during booking creation.

### Passengers tab (traveler details)

#### What’s the difference between a **passenger (pax)** and the **customer**?

* A **passenger (pax)** is an individual traveler on the booking.
* The **customer** is the main contracting/contact person for the booking (typically the person who receives confirmations, invoices, and messages).

You edit traveler information in **Passengers**, and communication/contact selection in **Customer Data**.

#### Why is it important that names match the passport/travel document?

Tickets, airline messages (SSR), and supplier documents can require an exact match. If a name is incorrect, it can cause:

* Document/ticket mismatches
* Failed check-in or manual handling requirements
* Extra work with suppliers to correct passenger details

#### Does changing **Birthdate** or **Age** affect the price?

Yes. Age and birthdate drive price logic such as:

* Adult/Child/Infant categorization
* Child-price rules
* Insurance eligibility
* Some discounts/supplements and supplier rules

If prices look wrong, verify the **birthdate** first.

#### Why does the **Age** not look correct?

Typically, age is calculated from **birthdate**. If age looks wrong:

* Confirm the birthdate is entered correctly (day/month/year).
* Make sure the travel dates are correct (age is usually evaluated “at time of travel”).

#### Can I add passengers after I already started the booking?

Yes.

* Use **Add new** to add another pax.
* Always **Save Changes** when you are done.

If the booking’s allotments (hotel/transport) were already taken, you may need to re-check availability and/or take allotment again (depending on your workflow).

#### What happens when I remove a passenger?

Removing a passenger will normally:

* Remove that pax from the booking’s passenger list
* Trigger recalculation of totals and per-pax services
* Potentially change eligibility for discounts/supplements or pricing rules

If you are removing passengers after services have been allocated (seats, rooms, extras), double-check that allotment and connected services still match the intended passenger count.

#### When should I use “TBA” passengers?

Use **TBA** (to be advised) placeholders when you need to reserve capacity (seats/rooms) but do not have final passenger names yet.

When names become known, replace TBA with the real passenger details to avoid ticketing/document issues.

### Customer Data tab (contact person + communication)

#### What is the **Customer** checkbox used for?

It marks who is the booking’s **main contracting customer/contact person**.

Typically:

* The customer is the passenger with valid **email** and **phone**.
* Customer-level communication is based on this selection.

#### Why can’t I mark a passenger as **Customer**?

In many setups, a customer record requires contact details. If the passenger is missing required contact fields (commonly email/phone), the system may not create/assign the customer as expected.

Fill in the contact information first, then set the passenger as **Customer**.

#### Who receives **Email** and **SMS** messages?

* The passenger marked as **Customer** is typically the primary recipient.
* Additional passengers can be opted in via the **EMAIL** and **SMS** checkboxes (they will receive the same communication as the customer).

#### Can I send confirmations/documents to more than one person?

Yes—enable **EMAIL** (and/or **SMS**) for additional passengers who should receive the same messages.

{% hint style="info" %}
If you need different message content per passenger (not identical to the customer), this is usually handled through template/setup rules rather than the Customer Data checkboxes.
{% endhint %}

#### What should I do if the wrong person is receiving messages?

1. Open **Edit Passenger**.
2. Go to **Customer Data**.
3. Set the correct passenger as **Customer**.
4. Adjust **EMAIL** / **SMS** checkboxes for other passengers.
5. **Save Changes**.

### Troubleshooting

#### I updated passenger details but the booking documents still show the old data

* Ensure you clicked **Save Changes** in the Edit Passenger window.
* If documents were already generated/sent, you may need to regenerate or resend them depending on your email/ticket flow.

#### I can’t save changes

Common causes:

* Missing mandatory fields (often title/first name/last name/birthdate)
* Invalid date format in birthdate
* Invalid characters in name fields (depending on ticketing rules)

### Related pages

* [Passengers Tab](edit-pas.md)
* [New Booking](./)
* [New Booking search support](new-booking-search-support.md)
