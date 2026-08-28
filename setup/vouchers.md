---
description: >-
  How Tourpaq automatically generates hotel, extra, and discount vouchers, what
  must be true first, and what to check when one is missing.
---

# Vouchers

#### Overview

A voucher is the document Tourpaq generates to confirm a booked service - it is what the customer and the supplier use to prove what was booked. Tourpaq generates vouchers automatically, checking several times a day, in three types: Hotel vouchers (one per hotel stay), Extra category vouchers (one per booked extra, such as an equipment rental or activity), and Discount and supplement vouchers (one per discount or supplement applied to the booking). Some extras also carry attributes - extra details a supplier needs beyond the extra itself, such as an equipment size or a service date. When an attribute is marked Appears on voucher its value prints on the Extra Voucher; when it is marked Is mandatory, Tourpaq will not generate the voucher until that value is filled in.

#### Purpose

* Provide customers and suppliers with the documents needed before departure.
* Save time and reduce manual errors through automatic generation.
* Verify that each booking meets voucher-generation conditions.

#### Preconditions

Tourpaq generates a voucher only when all conditions are met:

* The booking status is **OK**.
* The booking is fully paid.
* A voucher of the same type does not already exist.
* The departure date is not in the past.
* The departure date is within **X days before departure**. Set **X** in **System Setup → Vouchers Generation**.
* The hotel, extra, or discount has **Issue Voucher** enabled and a **Supplier** selected.
* For an **Extra Package**, every extra in the package has a **Supplier** assigned.
* Any attribute marked **Is mandatory** on a booked extra has a value.

Before an attribute can appear on an **Extra Voucher**:

* Create the attribute in [extras-attributes.md](../extras-attributes.md "mention").
* Assign the attribute to the extra in [attributes.md](../extras-setup/extras-general-page/attributes.md "mention").
* Enable **Appears on voucher** for the attribute.
* Select the extra for the relevant passenger.

#### How-to

Attribute values can also be entered during checkout or through **Edit Passenger**.

**Enter attribute values for a passenger**

1. In Tourpaq Office, open the booking and select **Passenger Details**.
2. Select the passenger.
3. Select the extra in its extra category.
4.  Enter or select the attribute values.

    <figure><img src="../.gitbook/assets/28.08.2026_14.20.11_REC.png" alt="Passenger Details showing attribute value fields for the selected extra."><figcaption><p>Enter the selected extra's attribute values in Passenger Details.</p></figcaption></figure>
5. Click **Save Passenger**.

**Regenerate vouchers after a change**

1. In Tourpaq Office, open the booking.
2. Select **Vouchers**.
3. Click **Regenerate all vouchers**.

#### Field reference

Configure extra attributes in **Extras → Extra → Attributes**.

<figure><img src="../.gitbook/assets/28.08.2026_14.17.51_REC.png" alt="Extra Attributes configuration for an extra in Tourpaq Office."><figcaption><p>Configure attributes for an extra in Extras.</p></figcaption></figure>

| Field                                            | Description                                                  | Notes                                                                                                                                         |
| ------------------------------------------------ | ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Is mandatory**                                 | Requires a value before Tourpaq generates the Extra Voucher. | Ski Rental: **Height** uses the **Integer** type and has **Is mandatory** enabled. Tourpaq blocks the Extra Voucher when Height has no value. |
| **Appears on voucher**                           | Prints the attribute value on the Extra Voucher.             | Ski Rental: **Start date** uses **display as stay days choices** and has **Appears on voucher** enabled. The voucher prints Start date.       |
| **Automatically Select Default Attribute Value** | Populates the configured default value when enabled.         | The default value appears under **Passenger Details**.                                                                                        |

The **Attributers** fields collect Ski Rental's Height and Start date during checkout or in **Passenger Details**.

Set the voucher-generation timing in **System Setup → Vouchers Generation**.

<figure><img src="../.gitbook/assets/28.08.2026_11.12.39_REC.png" alt="Vouchers Generation settings in System Setup."><figcaption><p>Set the number of days before departure for voucher generation.</p></figcaption></figure>

| Field             | Description                                                   | Notes                                                                                                                                  |
| ----------------- | ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue Voucher** | Enables voucher generation for the hotel, extra, or discount. | Tourpaq does not generate a voucher unless this setting is enabled.                                                                    |
| **Supplier**      | Selects the supplier for the hotel, extra, or discount.       | Every extra in an **Extra Package** requires a Supplier. Tourpaq does not generate a voucher for the package when any extra lacks one. |

<figure><img src="../.gitbook/assets/28.08.2026_11.09.29_REC.png" alt="Voucher settings for a hotel, extra, or discount, including Issue Voucher and Supplier."><figcaption><p>Enable Issue Voucher and select a Supplier for the booked entity.</p></figcaption></figure>

| Control                     | Description                        | Notes                                                                                                                                                                           |
| --------------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **View**                    | Opens an existing voucher.         | Available on the booking's **Vouchers** tab.                                                                                                                                    |
| **Send**                    | Sends an existing voucher.         | Available on the booking's **Vouchers** tab.                                                                                                                                    |
| **Regenerate voucher**      | Regenerates one voucher.           | Use after changes that affect that voucher.                                                                                                                                     |
| **Regenerate all vouchers** | Regenerates all voucher documents. | Use after an attribute changes or when another Extra Voucher is generated after multiple vouchers already exist. This updates all vouchers with the latest booking information. |

<figure><img src="../.gitbook/assets/28.08.2026_13.40.15_REC.png" alt="Vouchers tab in a booking showing voucher regeneration controls."><figcaption><p>Regenerate voucher documents from the booking's Vouchers tab.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/28.08.2026_13.38.12_REC.png" alt="Extra attribute settings showing mandatory and default-value options."><figcaption><p>Configure mandatory attributes and default attribute values.</p></figcaption></figure>

{% hint style="info" %}
If a voucher is missing, check these conditions in order:

* The booking is not **OK**.
* The booking is not fully paid.
* It is not yet **X days before departure**.
* A voucher of the same type already exists.
* The hotel, extra category, or discount does not have **Issue Voucher** enabled.
* The hotel, extra category, or discount is missing a **Supplier**.
* Required extra attributes are not filled in.
{% endhint %}

#### Related pages

* [qr-code-for-vouchers.md](../booking/new-booking/qr-code-for-vouchers.md "mention") — Add QR codes to generated voucher documents.
* [extras-attributes.md](../extras-attributes.md "mention") — Configure mandatory attributes and values used on extra vouchers.
* [extra-suplier.md](../suppliers/extra-suplier.md "mention") — Create suppliers for extras and assign their services.
* [general-settings](../brands/general-settings/ "mention") — Configure voucher numbering for a Brand.
