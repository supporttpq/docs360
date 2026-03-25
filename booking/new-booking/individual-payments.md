---
description: >-
  Send individual payment links in Tourpaq Office. Split a booking payment by
  passenger and email separate Customer Center payment links so each traveller
  pays their share.
---

# Individual payments

## Individual payments (split payments per passenger)

### Overview

**Individual payments** in **Tourpaq Office** lets you send **separate payment links** to multiple passengers on the same booking.

Each traveller receives an email with a **Customer Center** payment link. They can then **pay their own share** (their _passenger total_) without involving the main customer.

This is typically used when:

* You need **split payment** for a group booking.
* A booking includes multiple travellers who want to **pay separately**.
* You want the **payment link** sent to each passenger (not only the main customer).

{% hint style="info" %}
The payment is completed in the [**Customer Center**](../../setup/web-customer-center.md).
{% endhint %}

### Purpose

* Reduce back-and-forth between travellers about who pays what.
* Get faster payment collection for shared bookings.
* Keep a clear audit trail of who received which payment link.

### Preconditions

Make sure:

* The booking is created and has the correct passenger list.
* Each passenger who should pay has a valid email address.

{% hint style="info" %}
Only passengers with an email address entered will receive the individual payment email.
{% endhint %}

### Send individual payment emails

{% stepper %}
{% step %}
### 1. Add or verify passenger email addresses

1. Open the relevant booking.
2. Click [**Edit Passenger**](new-booking/edit-passenger/).
3. Go to the **Customer Data** tab.
4. In the **E-mail** column, enter the email address for each passenger who should receive the payment link.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (23).png" alt="Edit Passenger: add passenger email addresses under Customer Data"><figcaption><p>Enter an email address for each passenger who should receive an individual payment email.</p></figcaption></figure>

5. Click **Save Changes**.
{% endstep %}

{% step %}
### 2. Send the “Individual payment” email from the booking

1. Go back to the booking page.
2. Click the **Individual payment** button.
3. Tourpaq Office sends one email per passenger with an email address.

<figure><img src="../../.gitbook/assets/image (246).png" alt="Booking page: Individual payment button"><figcaption><p>Send the email from the booking page.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (2).png" alt="Individual payment email send dialog"><figcaption><p>Confirm the send action (dialog may vary by setup).</p></figcaption></figure>
{% endstep %}

{% step %}
### 3. What the passenger receives

Each passenger with an email address will receive an email containing:

* Payment details for the booking
* A **Customer Center payment link**, where they can pay their **passenger total**
{% endstep %}
{% endstepper %}

### Troubleshooting

#### A passenger didn’t receive the email

Check the following:

* Does the passenger have an email address filled in under **Edit Passenger → Customer Data**?
* Did you click **Save Changes** after entering the email address?
* Ask the passenger to check spam/junk folders (delivery can depend on their email provider).

#### An email was sent to the wrong address

1. Open **Edit Passenger → Customer Data**.
2. Correct the email address.
3. Save changes.
4. Send the individual payment email again (if your internal process allows resending).

### Related

* [**Economics**](economics.md) (payment overview, due dates, and payment status)
