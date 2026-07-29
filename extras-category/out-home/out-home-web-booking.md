# Out/Home - Web Booking

## Out/Home - Web Booking

The Out/Home configuration controls direction-specific transport Extras in Web Booking. It also applies when editing a booking in Customer Center.

### Do Booking

#### Overview

This workflow tests the **Individual Transport Extra Category** in **Web Booking**.

#### Purpose

This workflow verifies the following behavior:

* Individual transport Extras work for each direction.
* The booking saves selected Extras correctly.
* **Thank You for Booking** reflects the selected Extras.

#### Requirements

* Access to the **Do Booking** page.
* An operational Web Booking flow.
* An individual transport Extra Category for outbound, homebound, or both directions.
* Access to the **Extras (TILLAEG)** step.
* Extra items with configured brand, resources, prices, and availability.

#### System behavior

In **Extras (TILLAEG)**, Web Booking displays all available Extra Categories.

For individual transport categories, each passenger receives two columns:

* Outbound Extras.
* Homebound Extras.

The system displays only Extras eligible for each direction. It saves each selected Extra against the passenger and direction.

If no eligible Extras exist for a direction, Web Booking hides that direction's category.

#### Booking completion

After booking completion, **Thank You for Booking** displays the selected Extras. It separates outbound and homebound selections and calculates the totals.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (312).png" alt="Web Booking summary showing outbound and homebound transport Extras" width="563"><figcaption></figcaption></figure></div>

### Customer Center (Booking Confirmation)

#### Overview

Customer Center supports editing individual transport Extras in an existing booking.

#### Purpose

This workflow verifies the following behavior:

* Existing transport Extras load into the booking.
* Staff can modify Extras for either direction.
* The summary and totals reflect the updated selections.

#### Requirements

* An existing booking with at least one passenger.
* Transport Extras set for outbound and homebound directions.
* Access to **Booking Edit** and **Economics → Web Booking**.
* Transport Extras configured for booking visibility.

#### Access Booking Confirmation

In the booking edit view, open **Economics → Web Booking**. The **Booking Confirmation** page mirrors the Web Booking Extra structure.

#### System behavior

In **Extras (TILLAEG)**, Customer Center displays available Extra Categories.

For transport categories, each passenger receives outbound and homebound columns. The system displays only Extras eligible for each direction.

If no eligible products exist for a direction, Customer Center hides that direction's category.

#### Update Extras

Staff can add or change passenger Extras in **Extras (TILLAEG)**. The system saves the selections and updates the summary automatically.

#### Booking summary and totals

The summary lists all selected Extras. It separates outbound and homebound Extras and calculates totals from the selections.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (312).png" alt="Booking Confirmation summary showing outbound and homebound transport Extras" width="563"><figcaption></figcaption></figure></div>
