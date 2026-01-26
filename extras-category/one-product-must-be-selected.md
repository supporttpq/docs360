# One product must be selected

Applies to Administrator

### Overview

Some extras, such as pension or board options, require that **exactly one option is always selected** during the booking process.

Allowing users to deselect all options can result in invalid selections, incorrect tickets, or blocked bookings during allotment confirmation.

This feature ensures that a valid extra option is always selected when required.

See also: [Extra Category Overview](extra-category-overview.md).

### Purpose

The purpose of the **One product must be selected** option is to:

* Prevent users from selecting an empty or invalid extra option
* Ensure tickets and booking data remain correct
* Support extras where one option is mandatory, such as pension or board options
* Provide consistent behavior across Tourpaq Office booking and WebBooking

### Configuration

Enable this setting on the **extras category**.

{% stepper %}
{% step %}
### Open the extras category

Go to `Extras Setup > Extras Category`, then open the relevant category.
{% endstep %}

{% step %}
### Enable the option

Enable **One product must be selected**.
{% endstep %}

{% step %}
### Save and test

Create a test booking and verify you can only switch between options.
{% endstep %}
{% endstepper %}

**Field: One product must be selected**

* Type: Checkbox
* Location:\
  `Extras Setup > Extras Category`

### Booking Behavior

#### General Rules

When **One product must be selected** is enabled for an extras category:

* The user cannot deselect all options
* An empty choice (for example `---`) is never shown
* The user may only switch between available extras in the category

#### Auto-select Logic

* If one or more extras are marked **Auto-select**, one of them is automatically selected
* If no extra is marked **Auto-select**, the system automatically selects the **first listed extra**

This ensures that a valid selection always exists.

{% hint style="warning" %}
If the selected extra has no availability (for example due to allotment), the booking can be blocked when confirming allotment.
{% endhint %}

**Example: booking blocked at Take Allotment when “One product must be selected” is enabled**

* When the extra category "Gala Dinner" has the option enabled:

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

* And an extra in that category is available for booking:

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* If a user tries to make a booking where the extra must be selected, it will be blocked at **Take Allotment**:

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
