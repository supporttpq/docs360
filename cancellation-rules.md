# Cancellation Rules

#### Overview

The **Cancellation Rules** section defines how cancellation fees are calculated when a booking or passenger is canceled. The system determines the fee based on the number of days remaining until the departure date.

Administrators can configure up to four time ranges representing days left before departure. Each range can define either a fixed amount or a percentage of the passenger’s total price.

It is also possible to include **Cancellation Insurance** in the total fee calculation, depending on whether the insurance is paid and whether it covers the cancellation.

#### Purpose

Cancellation rules ensure consistent and automated fee calculation for canceled bookings. They help travel companies:

* Apply fair and transparent cancellation policies.
* Adjust penalties based on how close the cancellation occurs to the departure date.
* Integrate cancellation insurance coverage into the final fee.

<figure><img src=".gitbook/assets/image (26) (1).png" alt=""><figcaption></figcaption></figure>

#### Instructions

**1. Defining Cancellation Rules**

1. Navigate to the **Cancellation Rules** setup page.
2. Define up to **four ranges** for the number of days left to departure.
3. For each range, specify either:
   * A **fixed amount**, or
   * A **percentage** (calculated from the total passenger price).
4. (Optional) Select the checkbox **Include the cancellation insurance in the total** if the cancellation insurance amount should be added to the booking total.

> **Note:** Cancellation rules are linked to the **transport** at the time it is created.

<figure><img src=".gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**2. How the Cancellation Fee Is Calculated**

* **If cancellation insurance is paid:**
  * **Cover option selected:** The cancellation fee equals the amount of the cancellation insurance.
  * **Does not cover option selected:** The fee includes both the cancellation insurance amount and the amount defined in the cancellation rules.
* **If no cancellation insurance is paid:**
  * Only the **Cover option** is available, and the cancellation fee will be based solely on the defined cancellation rule.

> **Important:** Infants are exempt from cancellation fees.
