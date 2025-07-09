# Waitting list

### **What is a waiting list**

The notion of a waiting list (waitlist) has appeared in Tourpaq from the need to handle the situations when more customers are interested in placing a booking than there are available places (transport seats/hotel beds). Instead of losing customer interest in the area, a better approach is to keep a record of their interest (place a waitlist-type booking) and also be prepared for a best-case scenario where the hotel/transport supplements the places or existing bookings get canceled. In this situation, the bookings on the waitlist, in the order they were created, will be automatically processed to get an allotment. The details of this system behavior are described on this page.

### **Making the settings**

The starting point is having a normal price list situation already in place: hotel allotment, transport allotment, and a price defined for a particular departure. The single setting to be made in order to activate waiting list behavior of this price list is checking the **Waitlist (WL)** checkbox on it (it can be found and activated by selecting the FLAGS option).

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **The effects**

When dealing with a waitlist price, the system behaves as standard as long as there is enough allotment to cover the customer's needs. When the allotment ends, the system places a normal booking, excepting the allotment reservation and the booking status. No payment steps are in place when dealing with a waitlist booking, no email is sent to the customer, and the ticket clearly states that the booking is not a contract but a waiting list. The booking status will be **WL** instead of **OK,** and, from this point on, an automatic service will check allotment availability and will reserve allotments when possible. The booking status then gets set to **WLOK,** and the booking will appear on the main Office Dashboard to be managed by an admin/sales agent. Only after someone saves one more time the booking will then the status "**OK**, the customer will receive the Thank you for booking email and ticket, the payment rates and possibility will become active for the customer, etc.

### **In Tourpaq Office**

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Because it is a special function, when placing a waitlist booking, the seller is warned in several ways that the booking will not be a standard type of booking. The first notice can be in the transport popup if all rooms for that departure are out of allotment and they are set as the waitlist. The transport may not appear unless you hit the "Search Waitlist also" button. Under the hotel popup, a new "heads up" sign is shown as a colored thick border around the room selection checkbox and a mouseover message. The most important check made to be sure the seller (and customer) is aware that they are operating in a waitlist scenario is when clicking the "Take allotment" button. A validation checkbox appears, and you cannot advance until you confirm this. The rest of the behavior is already explained above.

### **In Tourpaq Web booking**

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The need to acknowledge the waitlist scenario is even greater in Web booking's case. The customers need to know and understand that they are not placing a firm order and that it is likely that they will not benefit from it. That is why a header message is listed on most pages of the Web Booking: landing page, confirmation page, and first page of the Customer Center login. The message has a default version and also can be customized for each brand. Generally, the texts that can be customized in Web Booking can be managed only by **Tourpaq Support**. Also, the payment step or payment option in the customer center is not present since the deal is not yet fully completed.

### **Tips and tricks**

Please note that if a price has no allotment and also is not a waitlist, then the web booking will reject the booking attempt.
