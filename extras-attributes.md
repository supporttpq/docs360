# Extras Attributes

## Extras Attributes

### Overview

Attributes define additional properties of an extra and influence its behavior, allowing guests to select a product that best fits their needs. For example, a Ski Rental extra can have an attribute specifying the guest's height, helping suppliers or agencies determine the correct ski length. Attributes automatically appear on the **Ticket** and in **Customer Center**.

### Purpose

* Enable customization of extras based on guest-specific criteria.
* Ensure accurate information is collected for suppliers or internal use.
* Improve visibility of extra details across vouchers, hotel lists, and extra lists.
* Enforce mandatory selections when required.

Example: A Ski rental product can have an attribute specifying the height of the guest so that the suppliers or the agency can know what length the ski equipment will be needed for the guest.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (21) (1) (1) (1) (1) (1).png" alt="Extras Attributes page"><figcaption></figcaption></figure></div>

### Configure attributes

You can choose one or more attributes for an extra.

An attribute will appear automatically on the Ticket and in Customer Center.

In **Extras Setup**, open **Extra Attributes** to set up an attribute.

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (23) (1) (1) (1).png" alt="Extra Attributes configuration"><figcaption></figcaption></figure></div>

#### Fields

Complete the following fields:

* Name: name of the attribute.
* List name: this is how you can find in lists.
* Yes/No - When this type is mandatory the system understands 'no' as the checkbox is not checked, and 'yes' if it is. The system will not force the user to check the attribute
* Decimal - usually used for financial amounts because it allows 2 decimal points
* Integer - is a value with no decimal points. (Example: age - 18. Rejected value: 18,5)
* Multiline Text - is a small description that allows text on multi lines, not only one as 'text' type
* Text - small description
* Time.
* Click on save.
* Max chars: For decimal types you need to count the 2 decimal points, the comma and the integer values. Example: max 4 means '9,00' is accepted, '10,00' is not because it has 5 chars. Available only for Decimal, Integer, Multiline Text and Text.
* Appears on voucher: the attribute will appear on vouchers.
* Appears on hotel list: the attribute will appear on hotel lists.
* Appears on extra list: selecting the checkbox, the attribute will appear on extra lists.
* Is mandatory: By checking this the user will be forced to set a value for this product attribute.
* Display rule[\* ](#user-content-fn-1)[^1]you can select:
  * display as stay days choices = shows the days the product to which the attribute is linked to as options.
  * display default days = allows only selecting the first day of the product (check-in date generally)
* Click on Save

{% hint style="info" %}
\*The Display Rules are hardcoded, meaning they are predefined and cannot be modified by the customer. Any changes to these rules can only be made by a Tourpaq developer.
{% endhint %}

### Display rule and voucher creation

The **Display rule** controls which stay-day values Tourpaq offers for an extra attribute. It does not create a voucher or change voucher timing.

The selected value is stored with the extra in the booking. It can appear on the voucher when **Appears on voucher** is enabled.

#### System behavior

* **display as stay days choices** offers every day of the linked product's stay. Select the relevant service day before voucher generation.
* **display default days** offers only the product's first stay day. This is usually the check-in date.
* When **Is mandatory** is enabled, a value is required before Tourpaq generates the Extra Voucher.
* When **Is mandatory** is disabled, an empty value does not block voucher generation.

The **Display rule** limits the available value choices. It does not make the attribute mandatory.

#### Example

An equipment-rental extra runs from 10 June through 16 June:

* **display as stay days choices** allows a selected value from 10 June through 16 June.
* **display default days** allows only 10 June.
* If **Is mandatory** is enabled and no value is selected, Tourpaq does not generate the Extra Voucher.

See [vouchers.md](setup/vouchers.md "mention") for all voucher generation requirements.

[^1]: View the information at the bottom of the page.
