# Pending payments DIBS transaction late response

### Why was this needed <a href="#why-was-this-needed" id="why-was-this-needed"></a>

DIBS e-payment platform sometimes does not provide a straightforward answer upon a transaction request: accepted and captured or declined.

&#x20;Pending payment For a small fraction of the transactions, some hours are needed for the transaction analysis and status update. During this time, the booking information was possible to be lost from the temporary cache without this new behaviour.

#### **Presentation video**

{% embed url="https://www.youtube.com/watch?feature=youtu.be&v=UEM6nwMeSTw" %}

### Details <a href="#details" id="details"></a>

To manage these situations, Tourpaq is using a temporary placed booking of status PENDPAY. This booking is blocking no hotel or transport allotment and exists only to hold information for the time when and if the transaction is accepted and the amount is captured from the customer's credit card.

At that moment, a background service checks the new transaction status and verifies for available allotment in the Tourpaq system.

If allotment is available, allotment is taken, and the booking is saved as OK status booking. The customer will receive the **"Thank you for booking"** email, and all the usual behaviour continues from this point on.

If allotment is not available anymore, the service will place a Tourpaq Dashboard note on the "Refund money" tab because the amount has been captured.

At this point, the brand administrator needs to refund the amount from the DIBS admin interface and also take out the transaction from the system by inserting an out/credit transaction with the same value on the booking. Canceling the PENDPAY booking is optional but recommended for clarity in the statistical overview.

<figure><img src=".gitbook/assets/web_booking_flow-1165f3dfba425adf63393a3ed21eed55.png" alt=""><figcaption></figcaption></figure>

Another option is to withdraw the money from the booking using a cash-out option, cancel the booking, and place another one. Then add the money to the new booking using a cash-in option with the cancelled booking number and transaction ID in the comment.

For this to work allotments have to be added in the sistem if the agency can obtain them from the hotel/transport, or another hotel/transport is used in the booking. In this case, contacting the client and informing him/her of the options is highly recommended.

### Web Booking part <a href="#web-booking-part" id="web-booking-part"></a>

When placing a "Last minute sale" booking, or if an agency always asks for deposit before allowing customers themselves to place bookings, DIBS payment platform becomes involved in the process.

This occurs by having a take-off page in Tourpaq that sends DIBS needed details for the transaction and also a landing page to receive DIBS feedback on the action.

When this feedback is "capture" it means that the transaction was successful and the amount captured on the customer's credit card.

When the feedback is not instant (minutes or hours later) or incomplete (they confirm they have received the request but not yet have a final status on it) the system will now place a Pending payment status booking. This will not block hotel or transport allotment, also will not block seats in transport seating layout or hotel room layout (if any chosen).

For a clear communication, the Web booking is presenting the customer with a page that will state a customizable message for each agency. Usually explanatory text about not being able to confirm the booking yet, until the final status of the transaction is received from DIBS (and that, when and if this will occur, the customer will receive the automatic email confirming the order).

<figure><img src=".gitbook/assets/wb_pendpay_message_-_mozilla_firefox_2018-10-01_12.27.21-9ef5aa76480821ccba563c0a960e2d25.png" alt=""><figcaption></figcaption></figure>

Instead of sending the "Thank you for booking" email (it's not the case yet), Tourpaq can send an explanatory email **"Pending payment notification"** with more or less the same the earlier details.

<figure><img src=".gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

### Tourpaq Service part <a href="#tourpaq-service-part" id="tourpaq-service-part"></a>

The Pending Payment Status Checker service will take the process from where the Web Booking has left it. This happens by periodically (aprox every 2 hours) checking in chronological order the incomplete payments in the system against the DIBS platform.

Please note that some transactions never seem to get an update from the "pending" status, Tourpaq will set them as failed if nothing changes within 5 days since their placement.

If a consistent update has occured (either captured or declined), the service will either try to finalize the booking or set the transaction as failed.

If the capture was successful, the system will check if hotel and transport allotment is still available. If yes, the system takes the needed allotment and saves the booking as OK, registering the transactions as successful.

If no allotment is available anymore, the service will place a notice on the Tourpaq Office dashboard in Refund money tab, because the amount was captured but the booking cannot be placed anymore.

The customer can also receive an instant email explaining him that, unfortunately there were no rooms/seats available at the moment of the payment confirmation and he will, most likely, be contacted for a refund as soon as possible. This email type is named **"Captured money but no allotment"**.

Other notice types will appear in this tab and you can read more about them in the Office section bellow.

### Office part <a href="#office-part" id="office-part"></a>

Here you can see the Pending Payment bookings in the View All booking page and also edit them. However, they are not taken in consideration for the turnover/profit calculations.

Please note! We do not recommend applying big changes on the PENDPAY booking, you can do however passenger/customer name corrections and extras management. Also, please do not cancel it before its listing in the Refund tab on the Dashboard.

If you receive a payment for the booking in other ways than through DIBS (eg: bank imports, cash, etc), the booking will not leave the PENDPAY status, only DIBS reply can make it become an OK status.

So, if you instantly need to obtain an OK booking for the customer, please manually set a new one in the system and link whatever payments you have to it. The PENDPAY one still needs to receive a final status from DIBS in order to reach a final status - OK or a situation where an admin/sales agent will overview the outcome. The "Refund money" tab on dashboard can present the following situations that need to be overviewed:

* Refund money - amount was captured on the credit card but the booking cannot be placed.
  * At this point, the brand administrator needs to refund the amount from the DIBS admin interface and also take out the transaction from the system by inserting an out/credit transaction with the same value on the booking. Canceling the PENDPAY booking is optional but recommended for clarity in the statistical overview.
  * Another option is to withdraw the money from the booking using a cash out option, cancel the booking and place another one. Then add the money to the new booking using a cash in option with the cancelled booking number and transaction id in the comment.
* Check booking - when the service found that the capture was successful and was able to save the booking as OK. In these situations, please check in the Internal Comment of the booking if the customer had chosen transport seating or hotel layout (where the case) and manually set them on the booking. Also please check booking overall integrity.
* Timeout - no Dibs status update happened within the 5 days since the transaction was placed. We consider this as a fail transaction but please manually check it in the DIBS admin if the case. In this case the booking can be canceled. If the payment gets confirmed later than 5 days, please cancel initial booking, place a new OK one and inform Tourpaq Support to assign initial payment to new booking, or simply set a fictive payment to the new booking, with comment refference to the real DIBS payment.
* Tourpaq error - in case something went wrong with processing the payment transaction. Please inform Tourpaq Support on these situations, if they occur, and wait for an update.

> 📝 **Note:** Please note!

Pending transactions older than 5 days are no longer checked for DIBS status change. They get automatically considered declined. -**A PENDPAY status booking cannot be set to OK by an admin** (however passenger name changes are possible etc). Only the service that checks pending transactions can do that. If another action is needed to overcome this default one, please **consider creating a new booking** and work on that one.
