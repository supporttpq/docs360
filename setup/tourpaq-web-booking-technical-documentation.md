---
noIndex: true
---

# Tourpaq Web Booking - Technical documentation

### Overview

Tourpaq Web Booking is the online booking page where customers can:

* book a trip
* pay (full or partial, depending on setup)
* print tickets
* manage selected extras

Each brand/agency can have its own design and a few behavior differences.

The entry point is **DoBooking.aspx**. This page receives booking details through the link (the URL parameters).

Below you’ll find an explanation of each parameter.

Tourpaq validates the full set of parameters. If something is wrong, the booking is blocked and the customer sees a message. An email with details can also be sent to the configured mailbox.

### Environments (live and staging)

Typical domains:

* Live: `[agencyBrandName].webbooking.tourpaq.com`
* Staging: `staging.[agencyBrandName].webbooking.tourpaq.com`

Staging is usually a copy of live data. It can be up to 2–3 weeks behind and may be cleaned.

### Parameter description <a href="#parameter-description" id="parameter-description"></a>

Example URL:

`https://primotours.webbooking.tourpaq.com/DoBooking.aspx?pltaID=84042&p=1&rno=3&pt=2&a=6&c=1&aa=14&ca=3&f=1&fd=12&ft=1`

| Name        | Meaning                                                                                        | Accepted values (required unless stated otherwise)                                                                                                                                                     |
| ----------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **pltaID**  | The trip ID used as the basis for the offer (departure, return, hotel room, base price, etc.). | Positive integer(s) for the current agency/brand. The booking is rejected if the ID is not valid or is not allowed (for example: departure is in the past, too close to departure, or the price is 0). |
| **p**       | Stay length code (how long the trip is).                                                       | Integer value in `1,2,3,4,100,101`. Values `1–4` are the standard intervals. `100` and `101` are used for one-way/custom setups.                                                                       |
| **rno**     | Number of rooms of each room type.                                                             | Integer(s) greater than 0. The booking is rejected if the passenger count does not fit the room(s) (too many or too few beds).                                                                         |
| **pt**      | Price type.                                                                                    | `1` = normal, `2` = discounted, `3` = group price.                                                                                                                                                     |
| **a**       | Number of adults.                                                                              | Positive integer(s).                                                                                                                                                                                   |
| **c**       | Number of children.                                                                            | Integer(s), can be `0`. Must match the room capacity rules together with adults.                                                                                                                       |
| **aa**      | Adult ages (optional).                                                                         | Comma-separated list of ages. If you provide fewer ages than the number of adults, the missing ones are treated as `99`.                                                                               |
| **ca**      | Children ages.                                                                                 | Must contain the same number of ages as `c`. Comma-separated for single-room setups. For multi-room setups, split by room using \`                                                                     |
| **db**      | Bonus code (optional).                                                                         | 5–20 characters. Codes with length 12 are typically reserved for gift cards. If the code is not valid, no bonus is applied.                                                                            |
| **f**       | Financing (optional).                                                                          | `0` or `1`. Financing is typically not allowed if departure is within the next 21 days.                                                                                                                |
| **fd**      | Financing duration (months).                                                                   | Used for financed bookings. Allowed values depend on the agency setup (for example `12,24,36,...`).                                                                                                    |
| **ft**      | Financing type.                                                                                | Used for financed bookings. Allowed values depend on the agency setup (for example `1–4`).                                                                                                             |
| **offerNo** | Offer number (optional).                                                                       | Used when a booking is opened from an offer.                                                                                                                                                           |
| **uh**      | User hash (optional).                                                                          | Identifies the agent who sent the offer link.                                                                                                                                                          |

### Multiple room types (comma-separated values)

Some setups support booking more than one room type in the same booking. In that case, most parameters must contain the same number of comma-separated values.

Example:

`https://primotours.webbooking.tourpaq.com/DoBooking.aspx?pltaID=84042,84572&p=1&rno=3,1&pt=2,1&a=6,2&c=1,1&aa=14&ca=3,7&f=1&fd=12&ft=1`

### Children ages per room (using `|`)

If you use multiple rooms and you want to control which child stays in which room, split child ages by room using `|`.

Example:

`DoBooking.aspx?pltaID=729932,729961&p=1&rno=2,1&pt=2,2&a=4,1&c=1,2&aa=&ca=9|12,5`

{% hint style="warning" %}
If you use comma-separated values, use them consistently.

Either you provide multiple values for the relevant parameters, or you provide single values. Mixing formats is not supported.
{% endhint %}

{% hint style="info" %}
In some setups, the same URL parameter structure can also be used in Office for testing.
{% endhint %}

***

### Validation errors

In Faster Web Booking, a detailed warning is shown on screen when something is wrong.

<details>

<summary>Legacy: Error.aspx parameters (older setups)</summary>

In older setups, a validation error could redirect to a page like:

`http://primotours.webbooking.tourpaq.com/Error.aspx?e=0&salg=0`

| Name     | Meaning                              | Possible values                      |
| -------- | ------------------------------------ | ------------------------------------ |
| **e**    | Error category number.               | Set by the system (varies).          |
| **salg** | Shows extra details when set to `1`. | `0` (default) or `1` (more details). |

If you need support, include the full Error URL and the parameters you used.

</details>

### FAQ

<details>

<summary><strong>What is the easiest way to build a correct Web Booking link?</strong></summary>

Start from a working example for the same brand/agency.

Change only one thing at a time (for example `pltaID`).

</details>

<details>

<summary><strong>Why is a booking link rejected?</strong></summary>

Common reasons:

* The departure date is in the past.
* The departure is too close to travel date (minimum limit).
* Passenger count does not fit the room(s).
* `c` and `ca` don’t match (number of children and child ages).
* The selected trip ID does not belong to the current brand/agency.

</details>

<details>

<summary><strong>How should I format multiple room types?</strong></summary>

Use comma-separated values for the parameters that relate to each room type.

Keep the same number of values across those parameters.

</details>

<details>

<summary><strong>How do I split children ages per room?</strong></summary>

Use `|` (pipe) inside `ca`.

Each side of the pipe represents one room.

</details>

<details>

<summary><strong>What should I send to support if something fails?</strong></summary>

Send:

* the full URL you used
* whether you tested on live or staging
* screenshots of the message shown to the customer

</details>
