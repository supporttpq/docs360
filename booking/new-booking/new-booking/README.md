# New Booking

### **Overview**

The **New Booking** functionality in Tourpaq allows users to create a booking by selecting a brand, adding transport and hotel options, managing passengers, and customizing extras, discounts, and supplements. It also includes advanced tools such as **passenger import** and **package product handling**.

### **Purpose**

This tool is designed to:

* Create new bookings from scratch.
* Assign transport, accommodation, and optional services.
* Manage passenger data individually or via file import.
* Apply complex product logic such as packages, extras, discounts, and insurance.

***

### **Preconditions**

Before creating a booking, ensure:

* You are logged in with permission to create bookings.
* All relevant products (transport, hotels, extras) are configured and active in the system.
* You have customer data ready.

<figure><img src="https://sonat.com/api/Document/Image/19670ef0-8b8a-4cda-8eb6-249681e07016/60a72aeb-a272-4428-a118-b6074b1b35b5/095769e7-32fd-4f22-8e55-e504ab071f34.webp?width=1915" alt="" width="900"><figcaption></figcaption></figure>

### **Instructions**

***

### 🔹 1. Create a New Booking

**Navigation:**\
Go to **Booking menu → Click on “New Booking”**

#### Steps:

1. **Choose the Brand.**
2. **Insert the customer’s mobile number** to identify or create a customer. ![](<../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png>)
3.  **Add Passenger Count** – Select the number of:

    * Adults
    * Children
    * Infants

    <figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### 🔹 2. Add Transport

1. Click on **Edit** in the Transport section.
2. **Select the Period** (departure/arrival range) to check availability.
3. Click **Search** to retrieve available transports.
   * Each result includes **transport allotment** and a hoverable **popup** showing extra quotas.
4. Select the **desired transport**.
5. Set the **trip interval** (duration in days).

![](https://docs.tourpaq.com/assets/images/TransportSelection-5b73846c23a09de529f49fee092d6c1d.png?width=1917)



![](https://docs.tourpaq.com/assets/images/TransportSelectionExtraPopUp-1cc416ad6d600130fcea3e1a7b7f752d.png?width=1918)

### 🔹 3. Add Hotel & Room

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Click on the **Hotel** section.
2. Filter by **Resort** or **Hotel** if needed.
3. Click **Search** to show available options.
4. Choose the best **Room Type**.
5. Click **Select**.
6. Click **Take Allotment** to lock the room for the booking.

***

### 🔹 4. Passenger Information

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Edit **Passenger Details**:
   * Gender, First Name, Last Name, Age
2. **Add Extras**:
   * Per passenger, or use the **yellow “C” icon** to apply extras to all eligible passengers.
3. **Add Discounts/Supplements**:
   * Click **Show/Hide Discount/Supplements**
   * Click **Add Discount/Supplement**
   * Select available options for one or all passengers
   * Multiple discounts or supplements can be added simultaneously.
4. Click **Save Passenger** to save changes.

***

### 🔹 5.  Booking Totals

The **Booking panel** provides a quick summary of financial details, booking metadata, and status indicators for a reservation. It is used by staff to monitor pricing, profitability, and the confirmation state of related services (hotel, transfer, etc.).

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Field Explanations**

#### **Financial Summary (Green Area)**

* **Total amount** – The final selling price of the booking (after discounts).
* **Normal Price** – The price, calculated using P prices (both adult and child). Discounts are not included.
* **Discount** –Represents the discount from the normal price
* **Selling price** – The actual price charged to the customer.
* **Total Profit** – The margin earned after subtracting supplier costs from the selling price.

#### **Booking Details**

* **Booking Number** – The unique identifier for the booking. In the example: `5585 + 1` (the `+1` indicate a sub-booking).
* **Status** – The current state of the booking (e.g., _OK_, _Pending_, _Cancelled_).
* **User** – The system user or agent who created/owns the booking. Example: `RWBTPO`.
* **Added** – The date when the booking was created.
* **Updated** – The date when the booking was last modified.

#### **Flags (Checkbox Options)**

* **Is Group Booking** – Indicates if the booking is part of a group reservation.
* **Remember Extras** – Ensures that selected extras (e.g., transport, insurance) are saved for future modifications.
* **Hotel Confirmed** – Marks whether the accommodation portion of the booking has been confirmed.
* **Transfer Confirmed** – Marks whether the transport/transfer services have been confirmed.

### 🔹 6. Finalize Booking

1. Review all details.
2. Click **Save** to complete the booking.
3. Send the ticket:
   * Click **Send Email** to send manually, or
   * Let the system auto-generate and send it.

***

### &#x20;  Import Passengers (Optional)

You can import multiple passengers via an Excel file.

#### Accepted File Format:

* Only **Excel files (.xlsx)** are supported.
* Required static columns:
  * `TITLE`, `F NAME`, `L NAME`, `DATE OF BIRTH`
* Optional static columns:
  * `CCL. INS.`, `INSURANCE`
* **Dynamic columns**:
  * Each column must match the **Extras Category Name**
  * Values must be **Extras Codes**

#### Behavior:

* If import **fails**: all changes are reverted.
* If import **succeeds with warnings**:
  * Rows are **highlighted**.
  * Hover over **info icon** to view warning tooltips.

**⚠️ Common Warnings:**

* Selected extra is unavailable for that category.
* Cancellation or travel insurance cannot be selected.
* The category does not support multi-select (only first value used).

***

### **Static Columns**

The columns **TITLE**, **F NAME**, **L NAME**, and **DATE OF BIRTH** **must always** be included in the import file and must match the exact names specified. The optional columns **CCL. INS.** and **INSURANCE** may be included if applicable but are not required.

| **Column Name**   | **Description**                                                                       |
| ----------------- | ------------------------------------------------------------------------------------- |
| **TITLE**         | The title of the passenger. This must be a value selected from a dropdown list.       |
| **F NAME**        | The first name of the passenger. Any string value is acceptable.                      |
| **L NAME**        | The last name of the passenger. Any string value is acceptable.                       |
| **DATE OF BIRTH** | The passenger’s date of birth in the format `dd-mm-yyyy`.                             |
| **CCL. INS.**     | The cancellation insurance for the passenger. This should be a value from a dropdown. |
| **INSURANCE**     | The travel insurance code for the passenger. This should be a value from a dropdown.  |

### **Dynamic Columns (Extras)**

Dynamic columns allow additional optional information about passenger extras. Each dynamic column corresponds to an **Extras Category Name** (case-insensitive) and requires the corresponding **Extras Code** value.

| **Extras Category Name**                      | **Extras Code**                                                                               |
| --------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **Extras Category Name (as in table header)** | The code(s) selected from the dropdown, separated by commas (optional). It can be left empty. |

**Usage:**

| Column Name           | Value                            |
| --------------------- | -------------------------------- |
| **EXTRAS\_CATEGORY1** | **EXTRAS\_CODE**                 |
| **EXTRAS\_CATEGORY2** | **EXTRAS\_CODE1, EXTRAS\_CODE2** |
| **EXTRAS\_CATEGORY3** |                                  |

### **Import Behavior**

1. **If the import fails:**
   * All changes to the passengers will be **reverted**.
2. **If the import succeeds but contains warnings:**
   * Rows with warnings will be **highlighted** with a specific color.
   * An **info icon** will appear for these rows, displaying all warnings as a tooltip.
   * Common warnings include:
     * The selected category is not available for selection.
     * The selected extra is not available for the category.
     * Cancellation insurance is not available for selection.
     * Travel insurance is not available for selection.
     * This category does not support multiselect. Only the first value from the list will be selected.

![](https://docs.tourpaq.com/assets/images/row_with_warnings-19946acdb755f600a02305f2edcef55e.png?width=1754)

An example file for importing passengers can include columns in the following format:

|       |        |        |               |           |           |                       |                        |
| ----- | ------ | ------ | ------------- | --------- | --------- | --------------------- | ---------------------- |
| TITLE | F NAME | L NAME | DATE OF BIRTH | CCL. INS. | INSURANCE | Morgenmad på værelset | BAGGAGE                |
| MR    | TBA1   | TBA1   | 19-11-1988    | 399       |           | MESS\_EX              | BAG-20, BAG-30, BAG-40 |
| MS    | TBA2   | TBA2   | 03-01-1926    |           | AUS       |                       | BAG-20                 |

### **Package products**

When selecting a product that is flagged as a package for a passenger, all the products that are inside the package will be selected after saving the passenger, but with a price of 0, only the package will have the price set.

For a product to be set as package, you need to check the option inside **Edit Product Page** -> **Basic Setup** -> **Other Settings** -> **Package Type**

![](https://docs.tourpaq.com/assets/images/package_and_product_example-fb064df3c22226835850f8ad23aef525.png?width=1645)

For a product to be set as a content type of a package, you need to check the option inside **Edit Product Page** -> **Basic Setup** -> **Other Settings** -> **Content Type**

![](https://docs.tourpaq.com/assets/images/package_and_product_example-fb064df3c22226835850f8ad23aef525.png?width=1645)

You can modify the products that are inside the package inside **Edit Product Page** -> **Package Content** tab

![](https://docs.tourpaq.com/assets/images/package_and_product_example3-83e4c48b16f44d9028b8a8ffcff1d567.png?width=1665)

<mark style="color:red;">**Warning messages**</mark>

* If you select the package, you can't select the products inside the package as well, as you will get a warning message that looks like this one:

![](https://docs.tourpaq.com/assets/images/package_and_product_warning-ecd616e463d185d98ad5ac65be13b1a3.png?width=1797)

* All the products inside the package have to be eligible so that the package can be selected. If they are not all eligible, you will get this warning message:

![](https://docs.tourpaq.com/assets/images/package_and_product_warning_2-182f4c506926ede24ffbcb6c77f7a3c9.png?width=1809)
