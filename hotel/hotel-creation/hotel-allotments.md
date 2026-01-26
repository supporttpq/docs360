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

<figure><img src="../../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure>

* **Period Start** – The start date of the allotment validity.
* **Period Stop** – The end date of the allotment validity.
* **Room** – The room type (e.g., Double Room, Suite, Family Room) defined in the system.
* **Min. Stay** – Minimum nights required for booking this room. `0` means no restriction.
* **Board** – The default board type for the room. The board price is included in the room cost.
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

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Rooms cannot be used in bookings until the allotment is **generated**.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The **Extend** button lets you extend the same allotment line without creating a new row. Enter a new **Period Stop** date and click **Extend**.

<figure><img src="../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Hotel allotment control

Hotel room availability can be limited per transport. This is set on the transport’s price list rule.

<figure><img src="../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Example:

* Total rooms on the allotment line: **20**
* Transport limit: **5**
* Already sold on this transport: **3**

Rooms left for this transport: **2** (`5 - 3`).

Other transports use their own limit. If no limit is set, sales follow the allotment’s **No.** value.

#### Generate all allotments

Use **Generate All** to generate every allotment line in one action. This is useful when a hotel has many lines to generate.

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Click **Generate All**, then click **OK** to confirm.

### FAQ

<details>

<summary>Why can’t I select the room in booking?</summary>

The allotment line is not enough.

You must click **Generate** (or **Generate All**) so the system creates the bookable allotment.

</details>

<details>

<summary>What’s the difference between <strong>No.</strong>, <strong>Secured</strong>, and <strong>Guaranteed</strong>?</summary>

**No.** is the total rooms you plan to sell in the period.

**Secured** is what the hotel has committed to allocate.

**Guaranteed** is what you will pay for even if unsold.

</details>

<details>

<summary>Do <strong>Secured</strong> and <strong>Guaranteed</strong> need to match <strong>No.</strong>?</summary>

Keep them consistent with your contract.

In most setups, **Secured** and **Guaranteed** should not exceed **No.**

</details>

<details>

<summary>What does <strong>Min. Stay</strong> do?</summary>

It enforces a minimum number of nights for bookings using that room/allotment.

Set it to `0` to allow any stay length.

</details>

<details>

<summary>How does the <strong>Board</strong> field affect pricing?</summary>

The selected board is treated as the default board for the allotment.

Its price is included in the room cost. See [Board Type - Hotel allotment / Ticket](../../board-type/board-type-hotel-allotment-ticket.md).

</details>

<details>

<summary>When should I use <strong>Extend</strong> vs creating a new allotment line?</summary>

Use **Extend** when only the end date changes.

Create a new line when room, board, quantities, or rules change.

</details>

<details>

<summary>I clicked <strong>Extend</strong> but the room still isn’t available for the new dates. Why?</summary>

Check the calendar icon to see the last generated date.

Then generate again so availability is created up to the new **Period Stop**.

</details>

<details>

<summary>What’s the difference between <strong>Generate</strong> and <strong>Generate All</strong>?</summary>

**Generate** generates only the selected line.

**Generate All** generates every line on the page.

</details>

<details>

<summary>Can I limit room sales per transport?</summary>

Yes.

Use the transport’s price list rule to set a max room allotment for that transport.

</details>

<details>

<summary>Should I avoid overlapping allotment periods?</summary>

Yes, especially for the same room + board combination.

Overlaps can make availability harder to predict and troubleshoot.

</details>
