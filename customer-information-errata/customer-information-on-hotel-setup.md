# Customer Information on Hotel setup

### Overview

Use **Passenger Information** on a hotel to add **customer-facing messages** that apply when a guest books that hotel (optionally limited by **travel dates**, **booking dates**, and **room type**).

Typical use cases:

* Renovations, pool closures, or seasonal facilities
* Local tourist tax information
* Check-in/check-out rules
* Mandatory terms the customer must acknowledge before booking can be completed

{% hint style="info" %}
You configure these messages per hotel in the back office:

**Hotel → Hotels → open a hotel → Passenger Information**
{% endhint %}

***

### What the customer sees

Depending on your setup, the **Information for customer** text can be shown in one or more places:

* In the booking flow in Tourpaq Office (for example when taking allotment)
* In WebBooking, typically in the final confirmation/summary step
* On customer documents (for example ticket/voucher), depending on your configuration

If **Acknowledge** is enabled, the booking flow requires the user/customer to confirm the message before they can proceed.

***

### Before you start

Make sure:

* The hotel already has the relevant **room types** configured (the rule must be linked to a room type).
* You have permission to edit hotel setup.

***

### Add customer information to a hotel

{% stepper %}
{% step %}
### 1) Open the hotel

1. Go to **Hotel → Hotels**.
2. Click the hotel you want to maintain.

You are now on the hotel edit page.
{% endstep %}

{% step %}
### 2) Open **Passenger Information**

1. Open the **Passenger Information** tab.

You will see a list of existing rules:

* The list is paginated (25 entries per page).
* If there are no rules, you’ll see **There are no entries to show**.
* Newer entries are shown first.
{% endstep %}

{% step %}
### 3) Choose where the text should apply (Default vs brand)

At the top you can typically switch between:

* **Default text**: applies across brands
* **Brand tabs**: only available if the hotel/brand is configured to use custom text

Select the tab you want to edit before creating a new rule.
{% endstep %}

{% step %}
### 4) Create the rule

1. Click **Create**.
2. Fill in the rule fields.

#### Fields explained

* **From / To (travel dates)**
  * Defines the travel period where the message applies.
  * **To** must be after **From**.
* **Booking Date From / To** (optional)
  * Limits the message to bookings created within a specific booking period.
  * Leave empty if booking date should not matter.
* **Room type**
  * Select which room type the message applies to.
* **Information for customer**
  * The message shown to the user/customer.
  * Enter the text in the pop-up editor (multi-line supported).
* **Acknowledge**
  * If enabled, the message becomes mandatory to confirm.
  * The UI shows an info tooltip describing the requirement.
{% endstep %}

{% step %}
### 5) Save

1. Click **Save**.

Expected result:

* The rule is saved and appears in the list.
* A confirmation message is shown.

If the rule breaks validation rules, you will see a warning message and the rule will not be saved.
{% endstep %}
{% endstepper %}

***

### Edit or delete an existing rule

#### Edit

1. In **Passenger Information**, find the rule.
2. Click **Edit**.
3. Update the fields.
4. Click **Save**.

#### Delete

1. Click **Delete** on the rule.
2. Confirm deletion in the pop-up dialog.

***

### Validation rules (important)

Tourpaq validates the rule before saving:

* **From/To is required**, and **To** must be later than **From**.
* **Booking dates are optional.** If you leave booking dates empty, the rule is evaluated only by travel dates (and room type).
* **Room type is required.**
* **Duplicate/overlapping rules are restricted** when they have the same combination of:
  * travel dates
  * booking dates
  * room type

You can create two rules for the same travel period if they apply to **different room types**.

***

### Brand-specific configuration

Some hotels support different text per brand.

* **Default text** is the shared baseline.
* A **brand tab** lets you maintain a brand-specific version.

To update brand-specific content:

1. Select the brand tab.
2. Edit or create rules the same way as in **Default text**.
3. Save.

***

### Troubleshooting

#### I can’t save my rule

Check these common causes:

* **To** date is earlier than (or the same as) **From**.
* A rule already exists that overlaps with the same travel/booking period and room type.
* A required field is missing (especially **From/To**, **Room type**, or **Information for customer**).

#### I don’t see a brand tab

Brand tabs only appear when **custom text** is enabled for that hotel/brand.

***

### See also

* [Hotels](../hotel/hotels.md)
* [Hotel Web](../hotel/hotel-creation/hotel-web.md) (general hotel text shown online)
* [Customer Information Booking Flow](customer-information-booking-flow.md) (how acknowledgements are enforced during booking)

***

### FAQ

<details>

<summary><strong>What is the difference between “Passenger Information” and “Customer Info” on the hotel Web tab?</strong></summary>

* **Passenger Information** (this page) controls conditional, rule-based messages shown during booking (and potentially on documents), and can require acknowledgment.
* **Customer Info** on the hotel’s **Web** tab is general hotel text used for online presentation and/or vouchers depending on configuration. See: [Hotel Web](../hotel/hotel-creation/hotel-web.md)

If you’re unsure which one to use, choose **Passenger Information** when the message must apply only for certain dates or room types, or when it must be acknowledged.

</details>

<details>

<summary><strong>Should I always enable “Acknowledge”?</strong></summary>

Enable **Acknowledge** when:

* The message is a mandatory condition (for example construction notice, local tax, special check-in requirements).
* You want to ensure the user/customer actively confirms they have read it.

Leave it disabled for purely informational notes.

</details>

<details>

<summary><strong>When should I use booking dates?</strong></summary>

Use **Booking Date From/To** when the message depends on when the booking was created.

Example: “Bookings made before 1 May include free dinner.”

If the message should apply to everyone traveling in a period (regardless of booking date), leave booking dates empty.

</details>

<details>

<summary><strong>Can I create the same message for multiple room types?</strong></summary>

Yes, but you must create a separate rule per **room type**.

</details>

<details>

<summary><strong>Why does Tourpaq prevent overlapping rules?</strong></summary>

Overlapping rules with identical conditions can lead to ambiguity about which message should apply. The system therefore restricts duplicates/overlaps for the same combination of travel period, booking period, and room type.

</details>

<details>

<summary><strong>What happens if booking dates are empty?</strong></summary>

If booking dates are empty, the rule is evaluated using only:

* Travel dates (From/To)
* Room type

</details>

<details>

<summary><strong>I deleted a rule by mistake—can I restore it?</strong></summary>

There is no in-page “undo”. Recreate the rule manually with the same dates, room type, and text.

If you need audit/history for who changed what and when, check whether your setup includes an activity log for hotel configuration.

</details>
