# Cancellation Insurance

#### Overview

**Cancellation Insurance** represents the fee a customer pays to ensure they can recover part of the total booking amount if they are forced to cancel their trip.

The insurance amount can be calculated in several ways, depending on the company’s configuration and business logic.

#### Purpose

This feature allows travel companies to offer financial protection to customers while maintaining flexibility in how the insurance price is determined. It ensures that the cancellation insurance is tailored to factors such as trip cost, duration, or transport type.

#### Instructions

There are **four methods** available for setting the price of the cancellation insurance:

1. **Based on Passenger Price**
   * The insurance fee is determined by the total amount the passenger pays for the trip.
   * Up to **four price ranges** can be defined.
   * Example:
     * If the passenger’s trip price fits within the first range, a specific fee is applied.
     * If it falls into the second range, a different fee is used, and so on.
2. **Based on Trip Duration**
   * The insurance fee is determined by the length of the trip.
   * Up to **four duration ranges** can be defined, each with its own insurance fee.
3. **Based on Percentage of Passenger Price**
   * The fee is calculated as a **percentage** of the passenger’s total trip price.
   * Example: If the percentage is 5% and the trip price is €1000, the insurance fee will be €50.
4. **Based on Transport Mode**
   * The insurance fee is determined by the **type of transport** selected for the booking (e.g., flight, bus, train).

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### External Cancellation <a href="#external-cancellation" id="external-cancellation"></a>

The **External Cancellation** setup allows integration with third-party insurance providers, enabling automatic mapping and management of external cancellation insurance products within Tourpaq.

Currently, Tourpaq supports two main providers:

* **Gouda**
* **Europeiske**

<figure><img src="../.gitbook/assets/external-cancellation-c9308d8d9e4939f5f63674392cc01434.png" alt=""><figcaption></figcaption></figure>

**Gouda Configuration**

To configure a Gouda external cancellation insurance:

* **Product Code** – A code used internally by Tourpaq, displayed in the web booking interface.
* **Gouda ID** – Identifies and maps the cancellation insurance product from Gouda to the corresponding entry in Tourpaq.
* **Name** – The name of the product as displayed in the web booking interface.

**Europeiske Configuration**

To configure a Europeiske external cancellation insurance:

* **Product Code** – A code used internally by Tourpaq, displayed in the web booking interface.
* **Europe ID** – Identifies and maps the cancellation insurance product from Europeiske to the Tourpaq system.
* **Name** – The name of the product as displayed in the web booking interface.
* **Trip Type** – Specifies the type of trip (e.g., charter, dynamic package, or scheduled transport) for which the cancellation insurance applies.
