# Add Transport Type and Transport Mode to Extras Resources

### Overview

You can link an **Extra** to a transport resource. This controls when the extra is shown during booking.

Extras Resources now support two filters:

* **Transport Type**
* **Transport Mode**

Use these filters to limit an extra.

Only show it for certain kinds of transport.

### Access

* Open **Extras Setup → Extras**.
* Open your extra.
* Go to **Resources**.

### Purpose

Transport Type and Transport Mode allow you to control **when an extra is available**, based on the transport used in the booking.

This is useful when selling extras such as golf bags, infant prices, or seat selection on Dynamic Packages, while ensuring that these extras are not handled as ancillaries in Amadeus.

### Screenshot

<figure><img src="../../../.gitbook/assets/image (603).png" alt=""><figcaption></figcaption></figure>

### Transport Type

Transport Type limits an extra to bookings that use a specific transport type.

If the booking does not match your selection, the extra is not shown.

#### Example

* Transfer used only for Charter\
  Transport Type = Sys-Real
* Transfer used only for GDS flights\
  Transport Type = System

### Transport Mode

Transport Mode is an extra filter for dynamic transports. It helps you separate flights from other transport modes.

Transport Mode is only checked when the chosen Transport Type supports it.

#### Supported values

* FLY (flight)
* CAR
* BUS
* TRAIN

#### Example

* **Transfer only for Charter**
  * Transport Type = Sys-Real
* **Transfer only for GDS / Dynamic Flight**
  * Transport Type = System
  * Transport Mode = FLY

### How to set Transport Type and Transport Mode

1. Go to **Extras Setup → Extras**.
2. Open the extra you want to change.
3. Go to **Resources**.
4. Select one or more **Transport Type** values.
5. Optional: select one or more **Transport Mode** values.
6. Click **Save**.

### Using Excluded Values

Both filters support **Use as Excluded**.

Turn it on to exclude what you selected. The extra will be available for everything **except** those values.

#### Example

* You do not want an extra to show for flights.
  * Transport Mode = FLY
  * Use as Excluded = enabled

### Important Notes

* Both filters support multiple selections.
* If you leave **Transport Type** empty, the extra can be used with all transport types.
* **Transport Mode** does nothing unless the selected Transport Type supports it.
* These filters can help avoid sending extras to Amadeus.

### FAQ

<details>

<summary>What happens if I do not select a Transport Type?</summary>

The extra stays available for all transport types.

</details>

<details>

<summary>Can I select more than one Transport Type or Mode?</summary>

Yes. The extra will be available when the booking matches any selected value.

</details>

<details>

<summary>What does “Use as Excluded” do?</summary>

It flips the logic. The extra will be available for everything except the values you selected.

</details>

<details>

<summary>I expected the extra to show up, but it does not. What should I check?</summary>

Check these items:

* The booking uses a transport that matches your Transport Type.
* If you set Transport Mode, the booking also matches that mode.
* You saved the extra after making changes.

</details>

<details>

<summary>Does this change existing bookings?</summary>

No. These filters control what is offered during booking and changes. They do not add or remove extras in existing bookings.

</details>

### Related pages

* [Extras](../)
* [Resources](./)
