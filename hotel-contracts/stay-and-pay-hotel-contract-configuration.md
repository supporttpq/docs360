# Stay & Pay - Hotel Contract Configuration

#### Purpose

The **Stay and Pay** tab is used to configure promotional offers like **"Stay X Nights, Pay Y Nights"**. This feature allows you to set up flexible, promotional pricing that incentivizes longer stays without proportionally increasing cost.

***

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

#### Fields Explained

| Section            | Field                                      | Description                                                                                                                                             |
| ------------------ | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Booking Period** | **Start / End**                            | Date range in which the **booking must be made** to benefit from the stay/pay offer.                                                                    |
| **Stay Period**    | **Start / End**                            | Actual **stay dates** for which the promotion applies.                                                                                                  |
| **Room**           | Dropdown (All rooms / specific room types) | Select the room(s) the Stay & Pay applies to                                                                                                            |
| **Week Days**      | Multi-select                               | Specify the weekdays where the guests shall arrive for the Stay & Pay to be applied                                                                     |
| **Period**         | Period number                              | Links the promotion to a **contract period** (set in the _Periods_ tab).                                                                                |
| **EB**             | Checkbox                                   | **Early Booking** flag—tick if this promotion should only apply to early bookings (this can work in combination with the _Early Booking Discount_ tab). |
| **Stay Days No**   | Numeric                                    | Minimum number of nights required to trigger the offer.                                                                                                 |
| **Pay Days No**    | Numeric                                    | Number of nights that will actually be charged.                                                                                                         |
| (🗑)               | Trash icon                                 | Deletes the row.                                                                                                                                        |

***

#### Example Configuration

| Field          | Value                   |
| -------------- | ----------------------- |
| Booking Period | 01-08-2025 → 31-08-2025 |
| Stay Period    | 01-09-2025 → 30-09-2025 |
| Room           | All rooms               |
| Week Days      | Selected all (7)        |
| Period         | 1                       |
| EB             | ☐                       |
| Stay Days No   | 7                       |
| Pay Days No    | 6                       |

This configuration means:

> Guests who book **in August** and plan to **stay in September** for **7 nights**, will only pay **6 nights**. The offer applies to all rooms and all weekdays.

***

#### Related Workflows

* **Contract Setup**: Ensure that **Periods** are defined.
* **Offers Module**: These promotions can appear as **special offers** in customer-facing booking tools.
* **Booking Flow**: If a booking qualifies (based on date, duration, and room), the discount is automatically applied.
* **EB Combination**: If **Early Booking (EB)** is selected, the rule stacks only when the early booking conditions are also met (_see Early Booking Discount tab_).

***

#### Best Practices

* Use **rounded values** like 7/6 or 4/3 for clarity.
* Avoid overlapping offers with identical conditions, which may confuse the booking engine.
