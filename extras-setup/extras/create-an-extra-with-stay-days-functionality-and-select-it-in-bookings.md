# Create an extra with stay days functionality and select it in bookings

This guide describes the steps required to configure an extra with _stay days functionality_ and how to select it within bookings.

***

### 🛠 Step-by-Step Configuration

#### 1. Access the Extras Page

* **Navigate to:** `Extra Setup → Extras -` The page displays all available extras.

***

#### 2. Create a New Extra

* **Click on:** `Create` button.

***

#### 3. Fill in Extra Details

* Add required input for the extra (e.g., name, category, price, etc.)

***

#### 4. Enable Stay Days Functionality

*   **Action:**

    * Expand the **Other Settings** section

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    * Tick the checkbox **Use Stay Dates in Prices**

    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
* **Expected Result:** The checkbox should appear as selected.

***

### 🧪 Test the Stay Days Setup in Bookings

#### 5. Access Prices Section

* **Click on:** `Prices -`The prices configuration page opens.

***

#### 6. Add a New Price Rule

* **Click on:** `Create -`A new row for the price rule is displayed.

***

#### 7. Configure the Rule with Stay Dates

*   **Action:**

    * Ensure columns for **stay date** appear
    * Add values for **payment rule**

    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
* The columns and selected options will be visible in the input fields.

***

#### 8. Save the Price Rule

* **Click on:** `Save` icon - A success popup appears and the row is saved correctly.

***

### ✅ Booking Verification

#### 9. Create a New Booking

* The booking should have status `OK`.

***

#### 10. Edit the Booking

* **Click on:** `Edit Passengers`

***

#### 11. Assign the Extra

* **Click on:** `Extra category` used during creation -  The list of available extras appears.
* **Select the Extra -** The created extra should be listed and selectable.

***

### 📌 Notes

* Ensure the extra’s **price rule date** falls within the **booking stay interval**.
* This setup allows dynamic pricing based on the actual stay dates, offering better flexibility and price accuracy.
