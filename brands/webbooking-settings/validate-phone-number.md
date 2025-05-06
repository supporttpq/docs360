# Validate Phone Number

On WB, the phone number field is “split” into 2 fields:

* **country code** — autofilled according to country selection, but editable, so it can be changed with a different one from dropdown list
* **normal phone number field** — with an only numeric chars validation, plus a minimum of 8 digits validation.

If country code is different from the country set, make sure the phone number is saved properly on booking (full, with country code included)

This option is enabled with a checkbox on **Brand → Web Booking Settings**.

* Remark: Country codes will be displayed according to the countries defined in the system (superadmin).
* If country is the same as country prefix, phone number is correctly displayed on booking (without prefix)

<figure><img src="../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>
