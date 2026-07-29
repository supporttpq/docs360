# Create an extra with stay days functionality and select it in bookings

## Create an extra with Stay Days functionality and select it in bookings

### Overview

This guide describes how to set up an extra with _Stay Days_ functionality and how to select it within a booking.\
The _Stay Days_ feature allows the price of an extra to be calculated dynamically based on the guest’s actual stay duration.

### Step-by-step configuration

#### Step 1: Access the Extras page

**Navigation:**\
`Extras Setup → Extras`

The page displays all available extras configured in the system.

#### Step 2: Create a new extra

Click **Create** to open a new extra configuration form.

#### Step 3: Enter extra details

Fill in all required fields, such as:

* **Name**
* **Category**
* **Price**
* Any other mandatory parameters relevant to the extra type

#### Step 4: Enable Stay Days functionality

1. Expand the **Other Settings** section.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Other Settings section"><figcaption></figcaption></figure></div>

2.  Tick the checkbox **Use Stay Dates in Prices**.

    ✅ _Result:_ The checkbox appears as selected, enabling the Stay Days functionality for this extra.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)   (7).png" alt="Use Stay Dates in Prices checkbox"><figcaption></figcaption></figure></div>

#### Step 5: Configure prices

1. Go to the **Prices** tab.
2. Click **Create** to add a new price line.
3. Define your pricing rules, ensuring the **Stay Date** columns are visible.
4. Set the required price and cost details.

The system applies price rules based on the customer’s stay period.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) ( (1).png" alt="Prices tab with Stay Date columns"><figcaption></figcaption></figure></div>

#### Step 6: Save the configuration

Click the **Save** icon. A success confirmation appears, and the system stores the new price rule.

### Test the Stay Days setup in bookings

#### Step 7: Create a new booking

1. Open the **Booking** module.
2. Create a new booking and ensure it has status **OK**.

#### Step 8: Edit the booking

1. Click **Edit Passengers**.
2. Open the **Extra category** used during setup.
3. Select the extra you configured with _Stay Days_ functionality.

The extra is visible and selectable within the booking.

### Notes

* Ensure the extra’s **price rule date** falls within the booking’s stay interval.
* This setup allows **dynamic pricing** based on the actual stay dates, improving pricing flexibility and accuracy.
