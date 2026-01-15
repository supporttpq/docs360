# Stay & Pay - Hotel Contract Configuration

### Overview

Use **Stay & Pay** to create promotions like **“Stay X nights, pay Y nights”**. This feature allows you to set up flexible, promotional pricing that incentivizes longer stays without proportionally increasing cost.

It supports common deals like **7/6** or **4/3**.

***

### Purpose

Use this tab to set contract-based price incentives for longer stays.

The discount is applied automatically when a booking matches your criteria.

***

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Preconditions

Before you start:

* The hotel contract exists and is open for editing.
* **Periods** are configured. You will reference them in **Period**.
* Room types are set up in **Rooms** (if you want to target specific rooms).

***

### Fields

| Field                          | Description                                                                              |
| ------------------------------ | ---------------------------------------------------------------------------------------- |
| **Booking Period (Start/End)** | Booking window. The booking must be created within this range.                           |
| **Stay Period (Start/End)**    | Stay window. The stay dates must be within this range.                                   |
| **Room**                       | Select **All rooms** or limit the rule to specific room types.                           |
| **Week Days**                  | Arrival weekdays that qualify. This is the **check-in day**.                             |
| **Period**                     | Links the promotion to a contract period set in **Periods**.                             |
| **EB**                         | Marks the rule as **Early Booking**. Use this if it should only apply to early bookings. |
| **Stay Days No**               | Minimum number of nights required for the promotion.                                     |
| **Pay Days No**                | Number of nights charged when the rule applies.                                          |
| 🗑️ **Delete**                 | Deletes the row.                                                                         |

***

### How it works

{% stepper %}
{% step %}
### Set the booking and stay windows

Use **Booking Period** to define when the booking must be made.

Use **Stay Period** to define when the stay must happen.
{% endstep %}

{% step %}
### Choose scope

Select **Room** to target specific room types.

Select **Week Days** to restrict by arrival weekday.
{% endstep %}

{% step %}
### Set the deal

Set **Stay Days No** and **Pay Days No**.

Example: `7` and `6` gives “stay 7, pay 6”.
{% endstep %}

{% step %}
### Validate with a test booking

Create a booking that matches the booking and stay windows.

Verify the priced nights match **Pay Days No**.
{% endstep %}
{% endstepper %}

***

### Example configuration

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

### Tips

* Use simple ratios like **7/6** or **4/3**. They are easy to explain.
* Keep **Pay Days No** lower than **Stay Days No**. Otherwise, it is not a discount.
* Avoid overlapping promotions with the same scope. Results get harder to predict.

{% hint style="info" %}
If you use **EB**, make sure your Early Booking setup also allows the combination you want. Test with a booking.
{% endhint %}

***

### Related workflows

* [Hotel contract - General](hotel-contract-general.md)
* [Rooms – Hotel Contract Configuration](rooms-hotel-contract-configuration.md)
* [Periods – Hotel Contract Configuration](periods-hotel-contract-configuration.md)
* [Early Booking Discount – Hotel Contract Configuration](early-booking-discount-hotel-contract-configuration.md)

***

### FAQ

**Does “Week Days” mean arrival day or every day of the stay?**\
It is the **arrival / check-in day**.

**Does Stay & Pay show up as a “special offer” in sales channels?**\
It can. It depends on your channel setup.\
Validate in your booking tool.

**Why is my Stay & Pay not applied?**\
Check **Booking Period** and **Stay Period** first.\
Then confirm **Period**, **Room**, **Week Days**, and stay length.

**Can I combine Stay & Pay with Early Booking Discount?**\
Yes, if your rules are set up to allow it.\
Use the **EB** flag and the Early Booking Discount’s **S\&P** option as needed.

**What should I enter for a “7 nights for the price of 6” deal?**\
Set **Stay Days No = 7** and **Pay Days No = 6**.

**What if the guest stays longer than “Stay Days No”?**\
The rule still requires the minimum stay.\
If you need multiple bundles or special behavior, add dedicated rules and test pricing.
