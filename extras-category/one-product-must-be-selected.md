# One product must be selected

### Overview

Some extras, such as pension or board options, require that **exactly one option is always selected** during the booking process.\
Allowing users to deselect all options can result in invalid selections, incorrect tickets, or blocked bookings during allotment confirmation.

This feature ensures that a valid extra option is always selected when required.

***

### Purpose

The purpose of the **One product must be selected** option is to:

* Prevent users from selecting an empty or invalid extra option
* Ensure tickets and booking data remain correct
* Support extras where one option is mandatory, such as pension or board
* Provide consistent behavior across Office Booking and Web Booking

***

### Configuration

#### Extras Setup | Extras Category

A new option is available at category level.

**Field: One product must be selected**

* Type: Checkbox
* Location:\
  `Extras Setup > Extras Category`

### Booking Behavior

#### General Rules

When **One product must be selected** is enabled for an Extras Category:

* The user cannot deselect all extras
* An empty choice (for example `---`) is never shown
* The user may only switch between available extras in the category

***

#### Auto-select Logic

* If one or more extras are marked **Auto-select**, one of them is automatically selected
* If no extra is marked **Auto-select**, the system automatically selects the **first listed extra**

This ensures that a valid selection always exists.

**Example in Booking - Selecting the "One product must be selected" option for an extra block the booking on Take Allotment**

* When the extra category "Galla Dinner" has the option selected:&#x20;

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

* And we have an extra available in that category for bookings:&#x20;

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* If an user tries to make a booking where the extra must be selected, it will be blocked on **Take Allotment:**

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
