# Keep automatic discounts prices

On booking, editing the booking engine handles price updates on discounts in two different ways:

1. The first way is to update prices on discounts/extras/travel insurance when a booking change is made.
2. The second way is to keep prices used at the time of the booking.

Default behavior is to keep prices, but there is a switch to make it the other way.

### How it works <a href="#how-it-works" id="how-it-works"></a>

On the booking page in the back office, there is a checkbox called "Keep automatic discount prices." The state of this checkbox is set by the company's general setting; here, you have the option to override it.

When this checkbox is checked, prices for extras, discounts/supplements, and insurance are kept to existing values.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When not checked, prices on extras, discounts/supplements, and insurance get updated with the new available prices.

### Do not apply <a href="#do-not-apply" id="do-not-apply"></a>

**Keep automatic discount prices** doesn't apply in these situations:

* Departure date is changed
* Transport is changed
* Hotel is changed
