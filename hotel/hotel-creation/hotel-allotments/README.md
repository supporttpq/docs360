# Hotel allotments

### Overview

The **Allotments** page lets you define and control how many hotel rooms you can sell in a period.

Each allotment line links to a room category and (optionally) a board type. This helps you split availability between **secured** and **guaranteed** rooms.

### Purpose

Use allotments to manage hotel contracts by setting aside a fixed number of rooms for sale. This prevents overselling and keeps bookings aligned with contract terms.

### Preconditions

* The hotel and its room categories must already be set up in the system.
* Relevant board types (meal plans) must be configured.
* A valid contract period must exist for the hotel.

### Fields

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Period Start** – The start date of the allotment validity.
* **Period Stop** – The end date of the allotment validity.
* **Room** – The room type (e.g., Double Room, Suite, Family Room) defined in the system.
* **Min. Stay** – Minimum nights required for booking this room. `0` means no restriction.
* **Board Basis** – This is the board basis of the room. The cost of the board basis is included in the room cost.
* **No.** – The total number of rooms available in the allotment for the defined period.
* **Secured** – Number of rooms contractually secured from the hotel.
* **Guaranteed** – Number of rooms financially guaranteed (must be paid even if unsold).
* **Copy** – Select to include this line when duplicating periods.
* **Generate** – Generates the allotment so it can be used in bookings.
* **Allotment status / Extend** –
  * **Calendar icon**: Shows the last generated date.
  * **Extend**: Extends the allotment beyond **Period Stop**.
* **Delete (trash icon)** – Deletes the selected allotment line.

Click **Save** to store your changes.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Rooms cannot be used in bookings until the allotment is **generated**.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The **Extend** button lets you extend the same allotment line without creating a new row. Enter a new **Period Stop** date and click **Extend**.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Hotel allotment control

Hotel room availability can be limited per transport. This is set on the transport’s price list rule.

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Example:

* Total rooms on the allotment line: **20**
* Transport limit: **5**
* Already sold on this transport: **3**

Rooms left for this transport: **2** (`5 - 3`).

Other transports use their own limit. If no limit is set, sales follow the allotment’s **No.** value.

#### Generate all allotments

Use **Generate All** to generate every allotment line in one action. This is useful when a hotel has many lines to generate.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Click **Generate All**, then click **OK** to confirm.
