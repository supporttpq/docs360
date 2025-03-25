# GDS Queue Place

This page displays reservations that are in the queue for processing in the GDS (Global Distribution System). These reservations have not been automatically completed and require either additional verification or manual action to be placed correctly.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

### Page Elements

\
a) **Main Table – Booking List**\
The table contains essential information about each booking in the queue, with the following columns:

* Booking – Unique identifier of the booking in the system.
* Status – Indicates the status of the booking in the GDS queue. (Example: “1” could mean that the booking is pending).
* Departure Date – The travel start date for the booking.
* Customer – The name of the customer associated with the booking.
* Booking Total – The total value of the booking.
* Paid Amount – The amount paid by the customer to date.
* Balance – The difference between the booking total and the amount paid. A balance other than “0” indicates an outstanding payment.
* Last Update – The date the booking was last modified.

&#x20;**b) “Place Bookings” button**\
&#x20;This button, located at the top right of the page, allows users to retry bookings that are in the queue.   This can be a solution to resubmit bookings to the GDS after any issues have been corrected.



### **Workflow**

1. Reviewing Reservations
   * The user can review each reservation in the list to identify issues (e.g. unpaid balance, pending processing status).
2. Correcting and Updating Reservations
   * If there is an outstanding balance, it may be necessary to pay it in order for the reservation to be processed.
   * If a reservation has not been updated recently, the user can check if any changes are needed.
3. Resending Reservations
   * By using the “Place Bookings” button, the user can try to process the reservations in the queue again.

### Possible issues and solutions

| Issue                                 | Possible cause                           | Recommended solution                             |
| ------------------------------------- | ---------------------------------------- | ------------------------------------------------ |
| QueueBooking remains in GDS Queue     |  Lack of confirmation from supplier      | Manually check and resubmit booking              |
| Balance remaining in “Balance” column | Payment not fully processed              | Check payments and contact customer if necessary |
| Status unchanged after resubmission   | Technical error or synchronization issue | Contact IT support team for assistance           |
