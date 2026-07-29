# Cancellation Insurance

## Cancellation Insurance

### Overview

**Cancellation Insurance** represents the fee a customer pays to ensure they can recover part of the total booking amount if they are forced to cancel their trip.

The insurance amount can be calculated in several ways, depending on the company’s configuration and business logic.

### Purpose

This feature allows travel companies to offer financial protection to customers while maintaining flexibility in how the insurance price is determined. It ensures that the cancellation insurance is tailored to factors such as trip cost, duration, or transport type.

### General settings

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Cancellation Insurance general settings"><figcaption></figcaption></figure></div>

**Brand**\* - Select the brand to which this cancellation insurance rule will apply. Mandatory field.

**Arr. dest**\* - Choose the arrival destination (e.g., Dubai). This is the location where the customer is traveling to. Mandatory field.

**Booking start**\* - Set the start date when the cancellation insurance becomes valid. Only bookings made after this date will be covered.

**Booking to**\* - Set the end date after which the cancellation insurance will no longer apply.

**Type of rule -** Determines how the cancellation insurance is calculated.

Options may include:

\- **Related to basic price**

\- **Related to transport type**

\- **Related to length of travel**

**- Percentage of basic price**

**Commision -** The commission is the percentage of the price that is used to calculate the cost (what is paid to the insurance company).

If the **commission percentage** is changed after bookings have already been created, the system will:

* Recalculate the cancellation insurance cost
* Update the cost on all existing bookings that use this insurance

This behavior ensures that the insurance cost reflects the correct commission configuration.

**Currency -** Defines the currency used in all related price inputs (e.g., DKK - Danish Krone).

**External Cancellation -** Allows linking to an external cancellation policy or provider (if integrated). - Gouda - Europieske

### Configure the insurance price

There are **four methods** available for setting the price of the cancellation insurance:

#### Related to basic price

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Cancellation Insurance related to basic price"><figcaption></figcaption></figure></div>

* The insurance fee is determined by the total amount the passenger pays for the trip.
* Up to **four price ranges** can be defined.
* Example:
  * If the passenger’s trip price fits within the first range, a specific fee is applied.
  * If it falls into the second range, a different fee is used.

#### Related to length of travel

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Cancellation Insurance related to length of travel"><figcaption></figcaption></figure></div>

* The insurance fee is determined by the length of the trip.
* Up to **four duration ranges** can be defined, each with its own insurance fee.

#### Based on percentage of basic price

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Cancellation Insurance percentage of basic price"><figcaption></figcaption></figure></div>

* The fee is calculated as a **percentage** of the passenger’s total trip price.
* Example: If the percentage is 5% and the trip price is €1000, the insurance fee is €50.

#### Related to transport type

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Cancellation Insurance related to transport type"><figcaption></figcaption></figure></div>

* The insurance fee is determined by the **type of transport** selected for the booking (e.g., flight, bus, train).

### External Cancellation <a href="#external-cancellation" id="external-cancellation"></a>

The **External Cancellation** setup allows integration with third-party insurance providers, enabling automatic mapping and management of external cancellation insurance products within Tourpaq.

Tourpaq supports two main providers:

* **Gouda**
* **Europeiske**

<div data-with-frame="true"><figure><img src="../.gitbook/assets/external-cancellation-c9308d8d9e4939f5f63674392cc01434.png" alt="External Cancellation provider configuration"><figcaption></figcaption></figure></div>

#### Gouda configuration

To configure a Gouda external cancellation insurance:

* **Product Code** – A code used internally by Tourpaq, displayed in the web booking interface.
* **Gouda ID** – Identifies and maps the cancellation insurance product from Gouda to the corresponding entry in Tourpaq.
* **Name** – The name of the product as displayed in the web booking interface.

#### Europeiske configuration

To configure a Europeiske external cancellation insurance:

* **Product Code** – A code used internally by Tourpaq, displayed in the web booking interface.
* **Europe ID** – Identifies and maps the cancellation insurance product from Europeiske to the Tourpaq system.
* **Name** – The name of the product as displayed in the web booking interface.
* **Trip Type** – Specifies the type of trip (e.g., charter, dynamic package, or scheduled transport) for which the cancellation insurance applies.

{% hint style="info" %}
In order to be able to track the data sent via the API, there is a log for the data sent to Gouda and Europæiske (travel insurance and cancellation), These logs can be checked in the [Internal Logs](../setup/internal-logs/insurance-payload-log-gouda-and-europaeiske.md) page of Setup
{% endhint %}
