---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Payment registration

Applies for Administrator and Financial

Payment registration is a module that allows the making and viewing of payments.

The payments inserted in the system can be either booking payments or guide payments. Booking payments are made for a certain booking. Guide payments are made by a guide for a certain destination.

From Payment registration is possible to insert only booking payments. But it is possible to view both booking and guide payments.

When making a new payment these are the steps:

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Click on "Create button"
* Choose a method of payment
* Choose the payment date
* Insert the booking number for which the payment is made
* Insert the paid amount
* Insert a comment
* Save the payment

It is also be possible to view all the payments from the system, by using certain search filters:

* Payment start date
* Payment end date
* Departure start date
* Departure end date
* Payment method – it will be selected from all the payment methods that have been inserted in the system for the current company; it should also be possible to select no payment method
* Debit/Credit payment type – the possible values will be Debit, Credit, no value
* Booking number – the booking number will be filled in
* Guide – it will be selected from all the guides that have been inserted in the system for the current company; it should also be possible to select “all guides” or “no guide”
* Giftcard number
* Resort (this filter should appear only when a guide or “all guides” is selected) – it will be selected from all the resorts from the system for the current company; it should also be possible to select no resort
* Transport

These are the default values:

* Payment start date – today date
* Payment end date – today date
* Departure start date – no selected date
* Departure end date – no selected date
* Payment method – no payment method selected
* Debit/Credit payment type – no selected type
* Booking number – no inserted number
* Guide – no guide selected
* Resort – no resort selected

When a date will be left empty (no selected date), it will mean that the filter shouldn’t be taken into account.

Let’s consider these filters in order to understand how this should work:

* Payment start date = 26.03.2025
* Payment end date = 31.03.2025
* Departure start date = no selected date
* Departure end date =  30.04.2025

All the payments for bookings with departure date before 30.04.2025, that are made after 1st should be displayed.

Below are all the cases when the filters shouldn’t be taken into account:

* Payment start date empty - if Payment end date value is filled in, there will be returned all the records with payment date before the Payment end date value; if the Payment end date is left empty, the Payment date filter won’t be taken into account
* Payment end date empty – if Payment start date value is filled in, there will be returned all the records with payment date after the Payment start date value; if the Payment start date is left empty, the Payment date filter won’t be taken into account
* Departure start date – if Departure end date value is filled in, there will be returned all the payments done for bookings with departure date before the Departure end date value; if the Departure end date is left empty, the Departure date filter won’t be taken into account
* Departure end date – if Departure start date value is filled in, there will be returned all the payments done for bookings with departure date after the Departure start date value; if the Departure end date is left empty, the Departure date filter won’t be taken into account
* Payment method – if no payment method is selected, the Payment method filter will not be taken into account
* Debit/Credit – if no type selected, the Debit/Credit filter will not be taken into account
* Booking number – if no number is filled in, there will be returned the payments for all the bookings
* Guide – if no guide is selected, the filter won’t be taken into account
* Resort – if no resort selected, the Resort filter won’t be taken into account

If at least one of the filters Departure start date, Departure end date or Booking number is filled in, then the guide payments won’t be taken into account. That’s because these filters are linked to a booking, but not to a group of passengers (for which the guide payments are made).

The reverse situation happens when a value is selected for guides (“all guides” or a certain guide); in this case, the booking payments won’t be taken into account. Even more, in this case, the filter for booking number should disappear, as a payment can be either a booking or a guide payment.
