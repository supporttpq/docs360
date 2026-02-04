# Email Templates

### Overview

Use **Email Templates** to create and manage automated emails sent by the system.

Templates keep your messages consistent. They can also insert booking details automatically.

### Where to manage templates

Most template work is done in the [E-mail center](email-setup/e-mail-center.md).

### Purpose

Use email templates to:

* Standardize communication with customers.
* Insert booking details using placeholders.
* Decide which templates are active.
* Test templates before using them.

Most templates are sent automatically when the right conditions are met.

Automated emails can be sent to customers, hotel suppliers, or transport providers.

The system does two things:

* Picks the emails that should be sent.
* Sends them.

{% hint style="warning" %}
If a recipient does not have an email address, the email cannot be sent.
{% endhint %}

### Template fields

Each template has these fields:

* **Sender email address**: The “from” email address.
* **Sender name**: The name shown in the inbox.
* **Activation status**: Active sends. Inactive blocks sending.
* **Email subject**: The subject line.
* **Email body**: The message text.

{% hint style="info" %}
**Placeholders** are short codes in the text.

The system replaces them with real data when sending.
{% endhint %}

### Common automatic emails

These are some of the most used templates:

* Booking confirmation (thank you for booking)
* Booking cancelled
* Payment pre-reminder and payment reminder
* Deposit received and payment received
* Insurance information missing
* Welcome home and welcome home reminder
* Flight changes
* Hotel and supplier reporting emails

### Full list of automatic emails

The list below is long by design. Many emails follow similar rules.

<details>

<summary>General rules used by many templates</summary>

Many templates share these rules:

* The same email is usually sent only once per booking.
* Booking status must match the email type.
* Departure date must not be in the past.
* Some emails are not sent for last-minute bookings.

Exact behavior can vary by setup and brand.

</details>

<details>

<summary>1–12: Booking, cancellation, payment, insurance, and questionnaires</summary>

#### 1. Thank you for booking

Sent after a booking is created. An e-ticket is attached.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.

If the booking is made in Web Booking, the email can be delayed slightly.

#### 2. Reservation cancelled

Sent after a booking is cancelled. An e-ticket is attached.

Typical conditions:

* The email has not been sent before.
* Booking status is **Cancelled**.
* Departure date is not in the past.

#### 3. Payment pre-reminder

Sent **3 days before** the payment due date. Not earlier than the day after booking.

It can include a secure card payment link. Login is not required.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.
* A required payment is still unpaid.

#### 4. Payment reminder

Sent **3 days after** the payment due date.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.
* Outstanding balance is above your tolerance setting.

#### 5. Booking cancelled in 48 hours

Sent to bookings with missing payments and outstanding balances.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.
* One or more payment rates are unpaid.

#### 6. Deposit received

Sent when a deposit payment is received.

Typical conditions:

* Deposit is greater than 0.
* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.

#### 7. Insurance information missing

Sent **14 days after booking** when insurance details are missing.

It can include a secure passenger details link. Login is not required.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.

#### 8. Insurance information still missing

Sent **10 days after** “Insurance information missing”.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.
* “Insurance information missing” has already been sent.

#### 9. Second payment received

Sent when the second payment is received.

Typical conditions:

* Second payment is greater than 0.
* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.

#### 10. Full payment received

Sent when the remaining balance is paid.

Typical conditions:

* Remaining payment is greater than 0.
* The email has not been sent before.
* Booking status is **OK**.
* Not a last-minute booking.
* Departure date is not in the past.

#### 11. Welcome home

Sent **one day after return day**.

It can include a secure questionnaire link. Login is not required.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Departure date is not in the past.

#### 12. Reporting schedule communication

Sent by automated transport passenger reporting.

</details>

<details>

<summary>13–24: Last-minute bookings, booking changes, reminders, exports, wait list, vouchers</summary>

#### 13. Thank you for your LMS booking

Sent for last-minute bookings. An e-ticket is attached.

If the booking is not fully paid:

* Payment pre-reminder text can be added.
* A secure card payment link can be included.

If it is fully paid, a payment confirmation can be added.

Insurance information text can also be added if needed.

#### 14. Booking updated

Sent when a booking changes in a way that affects the total.

Examples include adding a product or changing room distribution.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Departure date is not in the past.

#### 15. Hotel release

Sent by hotel release automation.

#### 16. Flight changes

Sent when a flight change is made.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Departure date is not in the past.

#### 17. Welcome home reminder

Sent **one week after return day** if a questionnaire is still missing.

It can include a secure questionnaire link. Login is not required.

Typical conditions:

* The email has not been sent before.
* Booking status is **OK**.
* Departure date is not in the past.

#### 18. Seat email reminder

Sent to let the customer know seats can be reserved.

Typical timing:

* 60 days before departure, or
* 12 hours after booking for short lead times

#### 19. Financial export

Sent based on settings per agency. It covers bookings in a specific interval.

#### 20. Questionnaire after deposit paid

Sent after the deposit is paid.

Typical conditions:

* Booking departs in the future.
* Booking status is **OK**.
* Email has not been sent yet.
* “Thank you for booking” email has been sent.
* Deposit was fully paid in the last 24 hours.

#### 21. Wait list booking

Sent when allotment is full, but wait list bookings are allowed.

Typical conditions:

* Booking departs in the future.
* Booking status is **WaitList**.
* Email has not been sent before.
* Booking update is older than 20 minutes (Web Booking).

#### 22. Vouchers generated

Sent after vouchers are generated.

Typical conditions:

* Booking departs in the future.
* Booking status is **OK**.
* Email has not been sent before.
* Departure is close (configured in system setup).
* Product attributes are filled in.

#### 23. Attributes are missing

Sent when required product attributes are missing.

Typical conditions:

* Booking departs in the future.
* Email has not been sent before.
* Booking is fully paid.
* Departure is within 30 days.

#### 24. Creditor invoice

Sent to creditors with financial information for hotels and products.

</details>

<details>

<summary>25–35: Reporting, documents, manual sends, payments waiting, and edge cases</summary>

#### 25. Hotel reporting

Sent based on intervals set in the hotel’s **Communication** tab.

#### 26. Extras reporting

Sent based on intervals set in the extra’s **Communication** tab.

#### 27. Supplier extras reporting

Sent based on intervals set on the supplier.

#### 28. Documents uploaded

Sent when a document is uploaded for a transport, hotel, or product.

Typical conditions:

* Booking departs in the future.

#### 29. Email sent from View all bookings

Sent manually by an admin or seller to filtered bookings.

It is often used for changes or promotions.

#### 30. Email sent from Customer Export

Sent manually by an admin or seller to filtered bookings.

It is often used for promotions.

#### 31. Request more rooms

Sent to hotels from the **Dashboard** when more rooms are needed.

#### 32. Early booking rooming list

Can include two emails, depending on settings:

* A rooming list email to the supplier.
* A financial invoice email to the creditor.

#### 33. Extras category reporting

Sent based on intervals set in the extra category’s **Communication** tab.

#### 34. Pending payment notification

Sometimes the payment provider (DIBS) needs more time.

This email tells the customer to wait for a final status.

#### 35. Captured money but no allotment

This can happen when two customers pay at the same time.

One gets the last allotment. The other pays successfully too.

This email explains the situation. A refund may follow.

</details>

<details>

<summary>36–46: Individual payments, guest app templates, and confirmations</summary>

#### 36. Individual payment email

Sent from the booking page to passengers with an email address.

It includes a link to a customer center for individual payment.

#### 37. Destination email

Used by the Destination or Guest app.

It can be used for:

* Order confirmation
* Excursion messages
* Arrival messages
* Hotel stay messages

#### 38. Hotel contract

Sent with a contract attached and a link to approve or reject.

Important notes:

* Supplier must be selected for the hotel.
* The hotel must have **Reservation Dept Email** filled in.
* Contract type must be **Allotment** or **Request**.

If Reservation Dept Email is missing, the email will not be sent.

#### Email templates with ticket attachment

Common examples:

* Thank you for booking
* Reservation cancelled
* Insurance information still missing
* Full payment received
* Thank you for your LMS booking
* Booking updated
* Flight changes
* Wait list booking

#### 39. Product reservation email

Sent to a passenger who bought a parking extra.

Typical conditions:

* Booking is fully paid.
* Reporting to APCOA succeeded.
* Latest APCOA report is older than 20 minutes.
* VRN (vehicle registration) is completed.
* Sent 30 days before departure.

#### 40. Special offer rejected

Sent when a hotel’s special offer is rejected from **Notifications**.

#### 41. Quotation list

Sent to a potential customer with a detailed price list.

#### 42. Stop sales introduction

Sent when a new stop sale is created.

#### 43. Mail platform for SMS

Sent to notify guests with general information.

#### 44. Dynamic Email / SMS

Used for messages like reminders, welcomes, and product tips.

#### 45. Confirmation hotel

Confirms a hotel reservation with dates, room type, and booking number.

It can also include address, contact details, and payment status.

To work correctly, you usually need:

* Supplier selected for the hotel.
* **Reservation Dept Email** filled in on the hotel.
* Contract type set to **Allotment** or **Request**.

#### 46. Confirmation transfer

Confirms a scheduled transfer with date, time, and locations.

Typical setup requirements:

* An extra that acts as the transfer.
* A supplier for the extra.
* Contract type is **Allotment** or **Request**.
* Category type is **Transfer**.

</details>

<details>

<summary>47–63: Reporting, gift cards, deprecated templates, and flight change variants</summary>

#### 47. Seats vs. beds reporting

Sent based on a communication scheduler. A report is attached.

#### 48. Gift card email

Sent automatically after the gift card is paid.

#### 49. Time share fee created notification

No longer used.

#### 50. Select offer SMS

Sent manually to inform the customer about a requested offer.

The text can be configured under **Brands → Select Offer**.

#### 51–52. Time share fee reminder / pre-reminder

No longer used.

#### 53. Car registration

Sent to passengers with a product requiring car registration.

#### 54. Full individual payment received

Sent when a passenger completes a full individual payment.

#### 55. Deposit received per passenger

Sent when a deposit is paid through individual payment.

This template supports special placeholders only used here:

* `[ConfirmationCode]`: confirmation code from APCOA
* `[CarRegistration]`: car license plate
* `[Product]`: product name
* `[EntryDateTime]`: departure date minus 2 hours
* `[ExitDateTime]`: departure date plus 1 hour

#### 56–63. Flight change templates

Different flight change templates can be used based on the type of change:

* Default
* Flight number
* Large earlier / large later
* Small earlier / small later
* Tiny earlier / tiny later

These are sent when a flight changes. An e-ticket can be attached.

</details>

### Related pages

* [E-mail center](email-setup/e-mail-center.md)
* [Dynamic E-mail/SMS Center](email-setup/dynamic-e-mail-sms-center/)

### FAQ

<details>

<summary>Where do I edit automated email templates?</summary>

Use the [E-mail center](email-setup/e-mail-center.md).

</details>

<details>

<summary>Why wasn’t an email sent?</summary>

Common reasons:

* The template is inactive.
* The recipient has no email address.
* The booking does not meet the template rules.
* The booking date or status is not eligible.

</details>

<details>

<summary>Can I test an email before it goes to customers?</summary>

Yes. Use the template testing options in the E-mail center.

</details>

<details>

<summary>What are placeholders?</summary>

They are short codes in the email text.

The system replaces them with real values during sending.

</details>

<details>

<summary>Why do I see a placeholder code in a sent email?</summary>

Most often, the placeholder is incorrect or the booking data is missing.

Test the template again and check the required booking fields.

</details>

<details>

<summary>Can I change a live template safely?</summary>

Make small changes and test them first.

If possible, copy the template and test the copy.

</details>
