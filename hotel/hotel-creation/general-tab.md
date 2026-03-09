---
description: >-
  Configure the core hotel record in Tourpaq Office. Complete all fields in the
  Hotel creation General tab and understand how each field affects booking,
  contracts, web, integrations, and reporting.
---

# General tab

The **General** tab is the starting point for hotel setup in Tourpaq Office. It defines the core hotel record that other hotel features depend on, including [Room cost](room-cost/), [Facilities](../../facilities.md), [Hotel Contracts](../../hotel-contracts/), [Hotel combination](../../hotel-combination.md), and booking hotel selection from [Hotels](../hotels/).

### Requirements

* Access to the **Hotel** module.
* Administrator permissions to create or edit hotels.
* Existing setup for **Resort**.
* Existing setup for **Supplier** if supplier-based workflows are used.
* At least one room type available if **Standard room** must be assigned immediately.

### Overview

The **General** tab stores the main identity, sales behavior, supplier behavior, and integration behavior of a hotel.

The values entered here affect:

* hotel visibility in Office and web flows
* hotel selection in bookings
* room behavior and child pricing
* supplier communication and integrations
* website sorting and API output
* follow-up setup in other hotel tabs

### Purpose

The purpose of this tab is to create a complete hotel master record before allotments, costs, contracts, room configuration, and web content are maintained.

Accurate setup here reduces booking errors and keeps hotel behavior consistent across Tourpaq.

### Instructions

{% stepper %}
{% step %}
### Enter the mandatory fields

Complete **Code**, **Name**, **Resort**, **Contract type**, and **Standard room**.
{% endstep %}

{% step %}
### Complete the operational fields

Review supplier, visibility, pricing, child-age, voucher, and integration settings.
{% endstep %}

{% step %}
### Save the hotel record

Save the hotel after the required setup is complete.
{% endstep %}

{% step %}
### Continue in related hotel areas

Maintain rooms, contracts, costs, facilities, web content, and communication in the related hotel pages.
{% endstep %}
{% endstepper %}

### General tab fields

<figure><img src="../../.gitbook/assets/image (403).png" alt="Mandatory fields in the Hotel creation General tab"><figcaption><p>Mandatory fields in the General tab.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (404).png" alt="Additional fields in the Hotel creation General tab"><figcaption><p>Additional operational fields in the General tab.</p></figcaption></figure>

#### Required fields

**Code**

Defines the hotel code.

This field is mandatory.

The code is the internal identifier for the hotel record. It is used across hotel search, integrations, reporting, API output, and maintenance flows.

**Name**

Defines the hotel name.

This field is mandatory.

The name identifies the hotel in Tourpaq Office and in downstream hotel-related workflows. It is also used when staff search for hotels in operational flows.

**Resort**

Links the hotel to a resort.

This field is mandatory.

The selected resort affects where the hotel appears in hotel searches, booking flows, reporting, and destination structure. It connects the hotel to setup maintained elsewhere in Tourpaq.

**Contract type**

Defines the commercial model used for the hotel.

This field is mandatory.

**Contract type** affects how the hotel is prioritized in the **Select Hotel** popup during booking. It also relates to hotel sourcing logic, contract handling, and setup choices in [Hotel Contracts](../../hotel-contracts/).

**Standard room**

Defines the default room type for the hotel.

This field is mandatory.

The selected room is the main room reference for the hotel. It is used during hotel setup and supports downstream room behavior in room-related hotel configuration.

#### Additional fields

**Supplier**

Defines the supplier connected to the hotel.

This field is not mandatory for saving in all setups, but it is important for correct hotel operation.

**Supplier** relates to supplier communication, contract ownership, reporting, integrations, and financial processes such as [Autobilling](../../autobilling/) when those are used.

**Stars**

Defines the hotel star rating.

This field is not always mandatory, but it is normally required for correct commercial presentation.

**Stars** affects how the hotel is presented on tickets and in downstream display channels. It also works together with **Customized Stars** when brand-specific display must override the default value.

**Infant price**

Defines the infant price for staying at the hotel.

This field is not mandatory in all setups.

This value affects hotel pricing behavior for infant passengers and should match the commercial setup used in booking and pricing workflows.

**Status**

Controls whether the hotel is visible or hidden.

This field is not mandatory for creation, but it is important for operational visibility.

**Status** affects whether the hotel appears in the [Hotels](../hotels/) list and other selection flows. Hidden hotels can still matter for history and controlled maintenance.

**Facilities template**

Assigns the facilities structure used for the hotel.

This field is optional, but strongly recommended when hotel web content is used.

This field enables facility setup in the **Web** tab. It relates directly to [Facilities](../../facilities.md) and supports correct hotel presentation in web-facing channels.

**Hotel combination**

Links the hotel to a combined-hotel setup.

This field is optional.

This setting allows two or more hotels to work as one combined product while drawing room allotments from the linked hotels. It relates directly to [Hotel combination](../../hotel-combination.md).

**Child price ages**

Defines the age interval that uses child price logic.

This field is optional, but important when child pricing differs from adult pricing.

This field affects how hotel price list child pricing is applied in booking flows. It should stay aligned with price list and room configuration logic.

**Child ages for extra bed**

Defines the age interval for children using an extra bed.

This field is optional.

If a child age falls outside this interval, the child uses adult extra-bed logic instead. This setting overrides the child age behavior defined on the base room type when a hotel-specific rule is needed.

**Adult hotel**

Defines an age limit for adult-only sale restrictions.

This field is optional.

If a passenger is below the configured age limit, the hotel cannot be booked. This field affects booking validation and should match the hotel’s commercial policy.

**Order No.**

Defines the internal hotel sort order.

This field is optional.

**Order No.** is used by the Tourpaq API to control the order of hotels sent to the website or other downstream consumers. It affects hotel display priority outside the edit screen.

**Customise room offer priority**

Controls whether room offer priority uses a custom order.

This field is optional.

When selected, Tourpaq uses the hotel’s own room priority, such as `orderId`, instead of automatic API prioritization based on room configuration like bed count. This field affects how room offers are ordered in downstream search and sales flows.

**Issue voucher**

Controls whether vouchers can be issued for the hotel.

This field is optional.

This setting relates to voucher generation and document workflows. Enable it when the hotel requires voucher-based operational handling.

**For one way**

Marks the hotel as a hotel used for one-way transport setups.

This field is optional.

This field relates to one-way travel configurations and should only be used when the hotel is part of a one-way setup model in Tourpaq.

**Extra Bed Discount Name**

Defines the display name of the extra-bed discount.

This field is optional.

The configured name appears on the ticket and in web booking when extra-bed discount logic is used. It relates to [Discount Extra Beds](discount-extra-beds.md).

**Managed by Availpro**

Marks the hotel as managed by Availpro.

This field is optional.

When enabled, the hotel uses rooms and costs from Availpro. This affects how room and cost data is sourced and maintained.

**Managed by SkiStar**

Marks the hotel as managed by SkiStar.

This field is optional and only available when SkiStar Sync is enabled for the company.

When enabled, Tourpaq performs automatic daily synchronization of allotment and cost prices for SkiStar accommodations. This affects how hotel availability and cost data are updated.

**SkiStar Resort ID**

Defines the SkiStar resort identifier.

This field is only relevant when **Managed by SkiStar** is enabled.

The value links the hotel to the correct SkiStar resort in the synchronization flow.

<figure><img src="../../.gitbook/assets/image (526).png" alt="Managed by SkiStar and SkiStar Resort ID fields"><figcaption><p>SkiStar-related fields.</p></figcaption></figure>

**Hide as filter on lists**

Removes the hotel from filters across the system.

This field is optional.

This setting affects list behavior in Tourpaq. It is useful when the hotel should remain in the database but should no longer appear as a normal filtering option in system lists.

**Is VisitSun**

Marks the hotel for VisitSun-related handling.

This field is optional.

Use this field only when the hotel is part of a VisitSun-specific setup or integration. Its relevance depends on the company configuration.

**Custom Hotel Days Booking**

Enables Hotel Price Per Day behavior for the hotel.

This field is optional.

This setting allows rooms to use the Hotel Price Per Day option in **Room Types** and relates directly to [A la Carte](../../booking/new-booking/a-la-carte/) and [Price List Custom Hotel Days](../../price-list-custom-hotel-days-service.md).

**Uses infant beds**

Controls whether infants occupy beds in this hotel.

This field is optional.

When enabled, infants count toward bed usage in the rooms assigned to the hotel. This affects capacity and room-allocation behavior.

### Customized star fields

The brand-specific star presentation can also be maintained on the hotel record.

This area affects what is sent to downstream display services and what can appear on tickets.

<figure><img src="../../.gitbook/assets/image (527).png" alt="Customized star fields on the hotel record"><figcaption><p>Default customized star fields.</p></figcaption></figure>

**Stars**

Defines the default star value for the hotel.

If a brand-specific **Stars** value exists, that value overrides the default value for that brand. If the brand-specific value is empty, Tourpaq uses the default value.

**Customized Stars**

Defines a custom star label for the hotel.

If this field is filled, the custom value can be shown instead of the standard star rating on the ticket. If a brand-specific **Customized Stars** value exists, that value overrides the default value for that brand.

The ticket heading for this value can be customized in **Users → Brands → Ticket**.

### After saving

After the hotel record is saved, continue with the next hotel areas as needed:

* [Room cost](room-cost/)
* [Extra Beds Costs](extra-beds-costs.md)
* [Discount Extra Beds](discount-extra-beds.md)
* [Facilities](../../facilities.md)
* [Hotel Contracts](../../hotel-contracts/)
* [Hotel reporting](communication/hotel-reporting.md)

### Related pages

* [Hotels](../hotels/)
* [Create using wizard](create-using-the-wizard.md)
* [Hotel combination](../../hotel-combination.md)
* [Autobilling](../../autobilling/)
* [A la Carte](../../booking/new-booking/a-la-carte/)
