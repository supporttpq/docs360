---
description: >-
  Create a new hotel in the Tourpaq Office with the Add Hotel Wizard. Add
  required hotel details, room types, and brand assignments in one setup flow.
---

# Create using the wizard

The **Add Hotel Wizard** creates a new hotel master record in one guided flow.

The created hotel is the same entity used across Tourpaq, including hotel selection in bookings, hotel contracts, allotments, cost rules, web content, and reporting. Continue with full setup in [Hotel creation](./) after the first save.

### Requirements

* Access to the **Hotel** module.
* Permissions for **Create using wizard**.
* Existing **Resort** setup. See [Resorts](../../setup/resorts.md).
* At least one room type available for selection in **Rooms** and **Standard room**.

{% hint style="info" %}
The **Create using wizard** action is typically available for administrator roles.
{% endhint %}

### Overview

The wizard collects the minimum required hotel data on a single screen.

After saving, Tourpaq creates the hotel and redirects to the hotel edit view for extended setup such as contracts, allotments, costs, facilities, and web content.

### Purpose

* Reduce hotel setup time for new hotel records.
* Enforce completion of minimum required fields before the first save.
* Create a valid foundation for downstream setup in hotel tabs and booking flows.

### Navigation

**Menu path**

Open **Hotel** → **Hotels**.

**Entry point**

Select **Create using wizard**.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1).png" alt="Add Hotel Wizard entry and form"><figcaption><p>Add Hotel Wizard.</p></figcaption></figure>

### Interface overview

The wizard screen is split into these areas:

* **Hotel details** for the core master data.
* **Rooms** for adding room types during creation.
* **Standard room** for choosing the default room.
* **Brand assignment** for controlling where the hotel is available.
* **Save** for creating the hotel record and leaving the wizard.

<figure><img src="../../.gitbook/assets/image (408).png" alt="Brand assignment area in Add Hotel Wizard"><figcaption><p>Brand assignment in the wizard.</p></figcaption></figure>

### Field description

#### Hotel details

**Code -** Unique identifier for the hotel record.

This field is mandatory.

This value is used across hotel search, integrations, exports, and reporting. Code uniqueness is validated at save time.

**Name -** Display name for the hotel.

This field is mandatory.

This value is shown in hotel selection flows and list views. It also impacts recognizability in operational work and downstream channels.

**Resort -** Resort assignment for the hotel.

This field is mandatory.

This selection links the hotel to destination structure. It affects hotel search, booking selection, and reporting grouping. Resort master data is maintained in [Resorts](../../setup/resorts.md).

**Stars -** Star rating used for classification and presentation.

This field is mandatory in the wizard.

Stars affects hotel presentation on tickets and in web-facing channels where star rating is displayed. Brand-specific overrides can be maintained later in the hotel record. See [General tab](general-tab.md).

**Contract type -** Commercial sourcing model for the hotel.

This field is mandatory.

Contract type influences hotel prioritization in the **Select Hotel** popup during booking and guides downstream contract setup in [Hotel Contracts](../../hotel-contracts/).

**Resort Name -** Optional free-text label related to the selected **Resort**.

This field is not mandatory.

This value does not replace the system link created by **Resort**. Use this field only when an additional label is required for internal context.

#### Rooms

**Rooms -** Room type list used during hotel creation.

This field is mandatory.

At least one room type must be added in this area before saving. Room configuration continues after creation in the hotel **Room Types** area in [Hotel creation](./).

**Edit -** Opens the room type editor for adding room types to **Rooms**.

This action is mandatory for first-time creation because the wizard requires at least one room type.

Room types relate to allotments, price lists, room cost rules, and booking validation. Rooms without allotments and prices cannot be sold. Cost setup is maintained in [Room cost](room-cost/).

**Standard room -** Default room type for the hotel.

This field is mandatory.

Standard room is used as the main room reference in hotel setup and supports downstream room behavior. The selected value must exist in **Rooms**.

#### Brand assignment

Brand assignment controls whether the hotel is available under a given brand in Tourpaq Office and web flows.

Brand assignment is not technically required to save the hotel, but it is required for the hotel to appear in brand-scoped workflows such as booking and WebBooking.

**Brand -** Brand identifier shown as a row label in the assignment area.

This is read-only and reflects company brand configuration. See [Brands](../../brands/).

**Assignment -** Availability selection per brand.

This field is mandatory per brand row when the hotel must be visible for that brand.

Typical values are variations of **Not assigned**, Office-only availability, web-only availability, or combined availability. Exact available options depend on company setup.

This setting relates directly to booking brand selection and web publishing behavior. If a hotel is missing in booking search or WebBooking, brand assignment is a primary validation point. See [Hotels list page](../hotels/hotels-list-page.md).

#### Actions

**Save -** Creates the hotel record and leaves the wizard.

Save is blocked until all mandatory fields are valid, including **Rooms** and **Standard room**.

### Configuration steps

{% stepper %}
{% step %}
### Open the wizard

Open **Hotel** → **Hotels**.

Select **Create using wizard**.
{% endstep %}

{% step %}
### Enter hotel details

Complete **Code**, **Name**, **Resort**, **Stars**, and **Contract type**.

Complete **Resort Name** only when an extra label is needed.
{% endstep %}

{% step %}
### Add room types and select the default room

In **Rooms**, select **Edit** and add at least one room type.

Select **Standard room** from the added room types.
{% endstep %}

{% step %}
### Assign brands

Set the brand availability in the brand assignment area.

Ensure the target sales channel is enabled for the brand where the hotel must be sold.
{% endstep %}

{% step %}
### Save and continue with full setup

Select **Save**.

Continue hotel configuration in [Hotel creation](./), starting with the [General tab](general-tab.md).
{% endstep %}
{% endstepper %}

### System behavior

**Validation**

* Save requires completion of all mandatory fields.
* **Code** must be unique.
* Save requires at least one room type in **Rooms**.
* **Standard room** must be selected and must exist in **Rooms**.

**After Save**

* Tourpaq creates the hotel master record.
* Tourpaq redirects to the hotel edit view for continued setup.

**Availability in booking and web flows**

* Brand assignment controls hotel visibility in brand-scoped workflows.
* Missing brand assignment can cause a newly created hotel to be absent from booking search or WebBooking.
* Contract type affects hotel priority in booking selection flows, but it does not create allotments or prices.

**Selling prerequisites after creation**

The wizard does not create allotments, prices, or costs.

Selling a hotel requires downstream setup such as:

* allotments in hotel allotment areas
* prices in price lists
* cost setup in [Room cost](room-cost/)
* contracts in [Hotel Contracts](../../hotel-contracts/)

### Examples

**Example: Create a new hotel record for one brand**

1. Set **Code** to `SUNSET01`.
2. Set **Name** to `Sunset Resort`.
3. Set **Resort** to `Agia Marina`.
4. Set **Stars** to `4`.
5. Set **Contract type** to `Allotment`.
6. In **Rooms**, select **Edit** and add `Double Room`.
7. Set **Standard room** to `Double Room`.
8. In brand assignment, set the target brand to an enabled availability option.
9. Select **Save**, then continue with allotments, prices, and contracts.

**Example: Hotel created but not visible in booking search**

1. Open **Hotel** → **Hotels** and locate the hotel.
2. Open the hotel edit view and validate brand assignment.
3. Validate that the hotel has required downstream setup for selling, such as allotments and prices.

### Related pages

* [Hotels list page](../hotels/hotels-list-page.md)
* [Hotel creation](./)
* [General tab](general-tab.md)
* [Hotel Contracts](../../hotel-contracts/)
* [Room cost](room-cost/)
* [Resorts](../../setup/resorts.md)
* [Brands](../../brands/)
* [Booking overview](../../booking/booking-overview.md)
