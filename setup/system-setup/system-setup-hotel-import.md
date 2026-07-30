# System Setup – Hotel Import

### Overview

**Hotel Import** defines default values for imported hotel data and hotel contracts.

The settings affect releases, single-room supplements, board supplements, and gala dinners.

They also control whether contract imports create Board Basis extras.

These settings support [Hotel Contracts](../../hotel-contracts/) and [Releases](../../hotel/hotel-creation/releases/).

### Purpose

Use **Hotel Import** to apply consistent defaults during hotel contract imports.

The defaults reduce repeated setup across hotel contracts.

They also align imported contract data with the company pricing policy.

### Requirements

Before configuring **Hotel Import**, confirm the following:

1. Administrator access to **Setup → System Setup** is available.
2. Hotel data is ready for import, or a hotel contract is available for testing.
3. The company pricing policy defines the required percentage adjustments.

{% hint style="warning" %}
Changes can affect future imports and contract behavior.

Validate changes with a test contract or import before using production contracts.
{% endhint %}

### Navigation

In Tourpaq Office, open **Setup → System Setup → Hotel Import**.

### Interface overview

The screen contains one time field, three percentage fields, and one checkbox.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (393).png" alt="Hotel Import settings, including release hour, price adjustments, and the board basis extras checkbox."><figcaption><p>Hotel Import settings.</p></figcaption></figure></div>

The fields apply defaults when a hotel contract is imported.

### Field descriptions

#### Hotel Release Hour

**Hotel Release Hour** sets the default release time for imported hotel releases.

This field is optional. Tourpaq uses `07:00` when no value is configured.

Enter a 24-hour time in `HH:MM` format.

For example, `06:00` sets imported releases to 6 AM.

This setting affects the release data used in [Releases](../../hotel/hotel-creation/releases/).

#### Single Room Supplement Price

**Single Room Supplement Price** adds a percentage markup for single-room bookings.

This field is optional. Enter a percentage value without a percent sign.

For example, `2` adds a 2% markup to the base price.

During import, Tourpaq inserts this value in **Hotel → Hotels → Single Room Supplement**.

Reimporting a hotel contract overwrites a manually changed supplement value.

See [Single Room Supplement](../../hotel/hotel-creation/occupancy-handling/single-room-supplement.md) for rule configuration.

#### Board Supplement Price

**Board Supplement Price** adds a percentage markup for board, or meal-plan, supplements.

This field is optional. Enter a percentage value without a percent sign.

For example, `2` adds a 2% markup to the base room price.

This default relates to board supplements in imported hotel contracts.

See [Board Supplements - Hotel Contract Configuration](../../hotel-contracts/board-supplements-hotel-contract-configuration.md) for contract-level setup.

#### Gala Dinner Price

**Gala Dinner Price** adds a percentage markup when an imported hotel contract includes a gala dinner.

This field is optional. Enter a percentage value without a percent sign.

For example, `2` adds a 2% markup to the booking price.

This default relates to the **Gala Dinner** section in hotel contracts.

#### Do not create extras for board basis

**Do not create extras for board basis** controls Board Basis extras during hotel contract import.

Select this checkbox when board basis must not create extras.

When selected, Tourpaq does not create Board Basis extras during import.

The **Board Basis** menu is also hidden in the hotel contract.

Leave this checkbox cleared when Board Basis extras are required.

See [Board Supplements - Hotel Contract Configuration](../../hotel-contracts/board-supplements-hotel-contract-configuration.md) for Board Basis behavior.

### Configuration steps

1. In **Setup → System Setup → Hotel Import**, set **Hotel Release Hour**.
2. Enter **Single Room Supplement Price** according to the company pricing policy.
3. Enter **Board Supplement Price** according to the company pricing policy.
4. Enter **Gala Dinner Price** according to the company pricing policy.
5. Select **Do not create extras for board basis** when Board Basis extras are not required.
6. Save the settings.
7. Import a test hotel contract and verify the imported values.

### System behavior

#### Import defaults

Tourpaq applies the configured values as defaults during hotel contract import.

Existing manual values can be replaced when the related hotel contract is reimported.

#### Board Basis extras

Tourpaq creates Board Basis extras during import when the checkbox remains cleared.

Selecting **Do not create extras for board basis** prevents their creation.

The selection also hides **Board Basis** in the hotel contract.

#### Release time

Tourpaq uses the configured **Hotel Release Hour** for imported hotel releases.

Without a configured value, Tourpaq uses `07:00`.

### Examples

#### Earlier release time

Set **Hotel Release Hour** to `06:00`.

Imported hotel releases use 6 AM as their default release time.

#### Single-room markup

Set **Single Room Supplement Price** to `2`.

Imported single-room supplement prices receive a 2% markup.

#### No Board Basis extras

Select **Do not create extras for board basis**.

Importing a hotel contract does not create Board Basis extras.

### Troubleshooting

* **Release time is incorrect after import:** Confirm **Hotel Release Hour** is saved.
* **Unexpected price changes occur:** Review all three percentage fields.
* **Board Basis extras are missing:** Clear **Do not create extras for board basis**, then import the contract again.
* **Board Basis extras are not needed:** Select **Do not create extras for board basis**, then reimport or recreate the contract.

### Related pages

* [Hotel Contracts](../../hotel-contracts/): Import targets and contract configuration.
* [Board Supplements - Hotel Contract Configuration](../../hotel-contracts/board-supplements-hotel-contract-configuration.md): Board Basis and gala dinner configuration.
* [Single Room Supplement](../../hotel/hotel-creation/occupancy-handling/single-room-supplement.md): Single-room supplement rules.
* [Releases](../../hotel/hotel-creation/releases/): Hotel release rules and behavior.
