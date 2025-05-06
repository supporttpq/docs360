# Multiple product selection in product category

This behaviour has been developped in response to the neeed of presenting the Web Booking users the possibility to buy multiple products in the same product category. This is also available on the Office booking placing process.

The activation of this behaviour is being made by the Tourpaq Office user under edit category "//Accepts multiple product selection//" checkbox.

### Various scenarios of work[​](https://docs.tourpaq.com/docs/documentation/multiple-product-selection-in-category#various-scenarios-of-work) <a href="#various-scenarios-of-work" id="various-scenarios-of-work"></a>

**1) Multiple products selected in same category**[**​**](https://docs.tourpaq.com/docs/documentation/multiple-product-selection-in-category#1-multiple-products-selected-in-same-category)

When the user needs to buy sepparate meals like: breakfast, lunch and dinner, all in the same category.

<figure><img src="../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

**2) Upgrade autoselected product**[**​**](https://docs.tourpaq.com/docs/documentation/multiple-product-selection-in-category#2-upgrade-autoselected-product)

The basic idea is to propose the user a default product (a rental car) which can be upgraded by paying the difference to a higher class option. The system allows also to downgrade an automaticly added product.

<figure><img src="../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

**3) Unremovable autoselected product and hidden in basic room price**[**​**](https://docs.tourpaq.com/docs/documentation/multiple-product-selection-in-category#3-unremovable-autoselected-product-and-hidden-in-basic-room-price)

The Tourpaq system also supports using in the same time all three settings of: autoselected product + multiple product selection on product category + agency hide autoselected prices (and include product price in room price). **Please note the listed informations make sense to the user only if the products that are being autoselected also have a 0 price value.** The result will allow to produce something like:

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

> 📝 \*_Note:_ **Please note a scenario that is not supported by the Tourpaq system.**

The system informs the user of this when trying to activate "agency hide autoselected prices" feature or "multiple product selection on product category" and the user takes responsibility for such scenario and effects.

If the autoselected product value is higher than 0, the listed values will be listed incorrectly. Let's assume the autoselected product price is 100DKK. That amount is being included in the room price. Two more products can be added and their values are 101DKK and 102DKK. Their difference to the base product is being listed as +1DKK and +2DKK, but adding them will make the total booking increase by 101+102=203DKK, not by 3DKK. Please see bellow printscreen of scenario where this issue appears.

<figure><img src="../../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

**KNOWN ISSUES**:

* Limitation - concerning Catering product category, the Transport reporting list will include only the last product selected by a passenger in this category.

> ⚠️ **Warning:** **Please be aware that Tourpaq supports but does not recommend**:

* Deactivating multiple product selection from a product category after bookings have been made with multiple product selected in the same category. This is **highly** not recommended. If still done, the booking will try to present correctly all the products already selected in the booking, but other issues may appear.
