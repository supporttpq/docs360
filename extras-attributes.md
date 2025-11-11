# Extras Attributes

Attributes define additional properties of an extra and influence its behavior, allowing guests to select a product that best fits their needs. For example, a Ski Rental extra can have an attribute specifying the guest's height, helping suppliers or agencies determine the correct ski length. Attributes automatically appear on the **Ticket** and in **Customer Center**.

#### Purpose

* Enable customization of extras based on guest-specific criteria.
* Ensure accurate information is collected for suppliers or internal use.
* Improve visibility of extra details across vouchers, hotel lists, and extra lists.
* Enforce mandatory selections when required.

Example: A Ski rental product can have an attribute specifying the height of the guest so that the suppliers or the agency can know what length the ski equipment will be needed for the guest.

<figure><img src=".gitbook/assets/image (21) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Users can choose one or more attributes for an extra.&#x20;

An attribute will appear automatically on the Ticket and in Customer Center.&#x20;

To setup an attribute go to Extra setup menu Click on Extra attribute.

<figure><img src=".gitbook/assets/image (23) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The next step is to complete the fields:&#x20;

* Name: name of the attribute.&#x20;
* List name: this is how you can find in lists.&#x20;
* Yes/No - When this type is mandatory the system understands 'no' as the checkbox is not checked, and 'yes' if it is. The system will not force the user to check the attribute&#x20;
* Decimal - usually used for financial amounts because it allows 2 decimal points&#x20;
* Integer - is a value with no decimal points. (Example: age - 18. Rejected value: 18,5)&#x20;
* Multiline Text - is a small description that allows text on multi lines, not only one as 'text' type&#x20;
* Text - small description&#x20;
* Time.&#x20;
* Click on save.
* Max chars: For decimal types you need to count the 2 decimal points, the comma and the integer values. Example: max 4 means '9,00' is accepted, '10,00' is not because it has 5 chars. Available only for Decimal, Integer, Multiline Text and Text.&#x20;
* Appears on voucher: the attribute will appear on vouchers.&#x20;
* Appears on hotel list: the attribute will appear on hotel lists.&#x20;
* Appears on extra list: selecting the checkbox, the attribute will appear on extra lists.&#x20;
* Is mandatory: By checking this the user will be forced to set a value for this product attribute.&#x20;
* Display rule[\* ](#user-content-fn-1)[^1]you can select:&#x20;
  * display as stay days choices = shows the days the product to which the attribute is linked to as options.&#x20;
  * display default days = allows only selecting the first day of the product (check-in date generally)
* Click on Save

{% hint style="info" %}
\*The Display Rules are hardcoded, meaning they are predefined and cannot be modified by the customer. Any changes to these rules can only be made by a Tourpaq developer.
{% endhint %}

[^1]: Please view the information at the bottom of the page
