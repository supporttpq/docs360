# Coded discount booking

### **Overview**

This page explains how to apply a **coded discount** (also referred to as a **bonus code**) during the booking process.

A bonus code is predefined in the system and can:

* Apply a **discount** (reduce the price), or
* Apply a **supplement** (increase the price), depending on the configured rules.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### **Purpose**

The **Bonus Code** feature allows agencies to apply predefined discounts or supplements to a booking. Bonus codes are typically configured by brand and can be linked to marketing campaigns, partner agreements, or seasonal promotions. This functionality ensures that eligible customers receive the correct price adjustment automatically during the booking process.

***

### **Preconditions**

* You are creating or editing a booking in **New Booking**.
* The booking is created under the **correct Brand** (bonus codes are often brand-specific).
* You have the bonus code provided by the customer or internal workflow.
* The bonus code is active and valid for the booking (dates, products, and other restrictions depend on configuration).

{% hint style="info" %}
Bonus codes are commonly managed as part of **Campaigns**. See: [Campaigns](../../campaigns.md).
{% endhint %}

***

### **How to apply a bonus code**

{% stepper %}
{% step %}
### 1. Create the booking as usual

1. Go to **Booking → New Booking**.
2. Select the correct **Brand**.
3. Select transport and hotel.
4. Click **Take allotment**.
5. Fill in passenger details and save passengers if required by your workflow.
{% endstep %}

{% step %}
### 2. Enter the bonus code

1. Locate the **Discount/Supplement Bonus Code** field.
2. Enter the code.
3. Click outside the field (or tab out) to trigger validation.

If the code is valid, the system applies the related discount/supplement and recalculates the total.
{% endstep %}

{% step %}
### 3. Verify the result

1. Confirm that the booking total changed as expected.
2. Open [Economics](economics.md) to verify how the discount/supplement affects:
   * Total price
   * Costs (if relevant)
   * Profit
{% endstep %}

{% step %}
### 4. Save the booking

Save the booking to store the applied bonus code and the resulting price adjustment.
{% endstep %}
{% endstepper %}

***

### **How validation works**

When you enter a code, Tourpaq typically checks (depending on configuration):

* Code exists and is active
* Brand/agency restrictions
* Booking date / travel date validity
* Eligibility rules (destination, hotel, transport, products, passenger types)
* Whether the code can be combined with other discounts

{% hint style="warning" %}
Some codes (for example campaign codes) may also **auto-add or override discounts/extras** based on the campaign definition. If you see products or discounts appear/disappear after entering a code, verify the campaign setup.
{% endhint %}

***

### **Notes**

* If a code is invalid or expired, it will not apply and you may see a warning.
* If the booking is later modified (changing hotel, transport, passengers, etc.), the system may **recalculate** discounts/supplements.
  * If you need to control discount recalculation behavior, see: [Keep automatic discounts prices](keep-automatic-discounts-prices.md).
* Access to using certain codes can depend on user permissions and brand setup.

***

### **FAQ**

#### **1. Where do I enter the coded discount / bonus code?**

Enter it in the **Discount/Supplement Bonus Code** field on the booking page. Click outside the field to validate and apply it.

***

#### **2. The code is accepted, but the total price did not change — why?**

Common reasons:

* The code is valid but does not apply to the selected transport/hotel/dates.
* The campaign rules require specific products/extras to be present.
* Another discount rule overrides it or the code is configured as “not combinable”.

***

#### **3. Why do I get an invalid/expired code message?**

The code may be:

* Mistyped
* Outside its active validity period
* Not enabled for the selected brand/agency
* Restricted to other destinations/products than the current booking

If you manage codes internally, verify the setup in [Campaigns](../../campaigns.md).

***

#### **4. Can bonus codes be combined with other discounts?**

It depends on how the code/campaign is configured. Some are combinable, others explicitly block combining with other discounts.

***

#### **5. Do I need to re-enter the code after making booking changes?**

Usually no, but booking changes can trigger recalculation. If the total changes unexpectedly after edits, verify that the booking still meets the code requirements and review the discount behavior.

***

#### **6. How do I remove a bonus code from a booking?**

Remove the code from the **Discount/Supplement Bonus Code** field (clear the field) and save the booking, then confirm in **Economics** that the discount/supplement is no longer applied.
