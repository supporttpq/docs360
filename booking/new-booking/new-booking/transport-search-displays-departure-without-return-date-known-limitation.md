---
description: >-
  Understand an edge case where transport search shows a departure without a
  valid return date. Covers the cause, expected vs actual behavior, impact, and
  validation guidance.
---

# Transport Search Displays Departure Without Return Date (Known Limitation)

#### Overview

When searching for transport options during the booking process, the system may display a departure date even when the corresponding return date is not defined in the transport configuration. This occurs in specific edge cases related to how transport availability is generated from [Transport Rules.](../../../transport-rules/create-transport-rule.md)

This behavior has been identified as a **known limitation** and does not affect the actual availability of the transport. The system will still validate the transport configuration when the booking is finalized.

#### Context

This situation can occur when the transport rule automatically extends the available departure dates, but the return day is not defined for the generated transport.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

As a result, the search results may display a departure date that appears valid in the list but does not include the expected return day.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Scenario Example

1. Log in as a user.
2. Click **New Booking**.
3. Select the brand.
4. Complete the **Passengers** section.
5. Click **Edit** in the **Transport** section.
6. Set the following filters:
   * **From:** 20-12-2027
   * **To:** 10-01-2028
   * **Transport Code:** melX2-07D
7. Click **Search**.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Expected Result

The last available transport should be **31-12-2027**, which is the last departure that has a valid return date configured.

#### Actual Result

The search results display **01-01-2028** as an available departure even though the transport configuration does not include the corresponding return day.

#### Explanation

This happens because the transport search logic reads the generated departures from the **Transport Rule extension logic**, which may extend departure dates beyond the last fully configured return date.

In this case:

* The system identifies **01-01-2028** as a generated departure.
* However, the return day for that departure is not defined in the transport configuration.

#### Impact

This behavior only affects the **search display** of transport options. It does not allow bookings with invalid transport configurations because the system validates the transport during later stages of the booking process.

#### Known Limitation

This scenario is considered an **edge case**, and the system currently does not filter out departures that do not have a configured return date when displaying search results.

As a result, a departure date can appear in the transport list even if the corresponding return day is missing.

#### Recommendation

Users should rely on the configured transport schedule when validating transport availability. If necessary, review the transport configuration in the **Transport Management** page to confirm valid departure and return combinations.
