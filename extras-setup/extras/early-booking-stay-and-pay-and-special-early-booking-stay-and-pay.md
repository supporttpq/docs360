# Early booking/Stay and pay and Special Early Booking/Stay and pay

These features allow the supplier to give discounts to the agency for the sold products. They work in the same way as the **Early Booking/Stay and pay** and **Special Early Booking/Stay and pay** from the hotel. For more information on this you can check [Room Cost](../../hotel/hotel-creation/room-cost/) **Early booking cost-discount rules** section.

<figure><img src="../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

### **Overview**

The **EB/SP** tab allows configuration of pricing rules for promotional scenarios, such as Early Booking Discounts and Stay & Pay campaigns. These rules incentivize customers to book early or to stay longer.

***

### **Tabs within EB/SP Section**

#### 1. **Early Booking Cost Discount Rules**

This section allows the setup of promotional discounts for early bookers.

#### 2. **Stay And Pay Cost Rules**

(Displayed but not selected in the screenshot — used for configuring “Stay X, Pay Y” offers.)

***

## **1. Early Booking Cost Discount Rule Configuration**

This area defines the conditions under which a discount applies based on early reservation criteria.

| Field                                                     | Description                                                                                            |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Stay Start**                                            | The start date of the stay period the discount applies to                                              |
| **Stay End**                                              | The end date of the stay period                                                                        |
| **Booking Start**                                         | The first date on which bookings are eligible for this discount                                        |
| **Booking End**                                           | The last date on which bookings can be made to receive the discount                                    |
| **Days of the week**                                      | Select days of the week the discount is valid.                                                         |
| From age / To age                                         | Specify an optimal age range for the Early Booking Discount. (Leave the field empty to accept any age) |
| **Price**                                                 | The discount amount                                                                                    |
| **Is Percent**                                            | Indicates whether the discount is a percentage. A check mark means yes (✅).                            |
| **Days No Before Arrival**                                |  This could restrict how close to the arrival date the discount applies.                               |
| **S\&P (Stay and Pay)**                                   | Whether this discount is linked with a Stay & Pay rule. A cross (❌) indicates it is not.               |
| **Send List Date**, **Deposit Date**, **Deposit Percent** | Optional fields for controlling list communication or partial payments.                                |

***

### **Actions**

* **Edit** (✏️): Modify the existing rule.
* **Delete** (🗑️): Remove the rule permanently.
* **Add Early Booking**: Button to create a new discount rule.

***

### **Best Practices**

* Ensure booking dates and stay periods don’t overlap with other discounts to avoid conflicts.
* Use the “Is Percent” checkbox carefully to differentiate between fixed amount and percentage discounts.
* Regularly review discount rules ahead of seasonal offers to align with marketing strategy.
* Use “Days No Before Arrival” if you want to block last-minute bookings from receiving discounts.

***

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

## 2. Stay And Pay Cost Rules

This section allows you to define "Stay and Pay" conditions that encourage longer stays by offering a set number of paid days within a longer booking.

***

### Rule Configuration Table

| Field                      | Description                                                                                                                  |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Stay Start**             | The first eligible date a guest must start their stay.                                                                       |
| **Stay End**               | The last eligible date for the stay to end.                                                                                  |
| **Booking Start**          | The earliest date a booking must be made to be eligible.                                                                     |
| **Booking End**            | The last date on which a booking can be made for the rule to apply                                                           |
| **Stay Days**              | Total number of nights required for the rule to apply.                                                                       |
| **Pay Days**               | Number of days the guest is charged for                                                                                      |
| **Days No Before Arrival** | Minimum number of days between booking and check-in date.                                                                    |
| **EB (Early Booking)**     | Indicates whether the rule is marked as Early Booking. The warning icon (⚠️) suggests that this rule is not marked as an EB. |
| **Contract**               | Denotes whether a contract is attached to this rule. Empty, so no contract linked.                                           |

### Add Stay\&Pay Button

The **Add Stay\&Pay** button in the top right allows administrators to create a new Stay and Pay rule, defining new promotional conditions for other stay periods or products.

***

### &#x20;Edit and Delete

* **✏️ Pencil Icon:** Edit existing rule parameters.
* **🗑️ Trash Icon:** Delete the rule from the list.

***

## 3. Special Early Booking&#x20;

### **Overview**

The **Special EB/SP** tab allows administrators to define **special early booking discounts** and **stay-and-pay promotions**. These rules determine when and how discounts are applied to bookings, based on stay dates, booking dates, age ranges, and other configurable conditions.

This setup ensures that promotional campaigns (e.g., _Book early and save 20%_) are automatically applied during the booking process.

***

### **Purpose**

The feature is used to:

* Create **time-bound discounts** for early bookings
* Configure **age-specific promotions** (e.g., discounts for children or seniors)
* Define **deposit requirements** and deadlines for early bookings
* Manage **stay-and-pay** offers (e.g., _Stay 7 nights, pay for 6_)

***

### **Preconditions**

Before defining rules in this screen:

* The **contract (hotel or extra)** must already be created.
* You must have **Administrator** or **Financial** access.
* You should know the **validity period, discount values, and conditions** for the promotion.
* Ensure alignment with the company’s **commercial agreements** and policies.

***

### **Fields Explained**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| **Field**                  | **Description**                                                                                                                                                                        |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stay Start**             | The first date when the stay must begin for the discount to apply.                                                                                                                     |
| **Stay End**               | The last date when the stay must end for the discount to apply.                                                                                                                        |
| **Booking Start**          | The first date when bookings must be made to qualify for the discount.                                                                                                                 |
| **Booking End**            | The last date when bookings can be made to qualify for the discount.                                                                                                                   |
| **Days of the Week**       | Restrict the discount to specific weekdays (e.g., only arrivals on Monday).                                                                                                            |
| **From Age**               | Minimum passenger age required for the discount.                                                                                                                                       |
| **To Age**                 | Maximum passenger age eligible for the discount.                                                                                                                                       |
| **Price**                  | Discount value. Can represent a fixed amount or percentage (see _Is Percent_).                                                                                                         |
| **Is Percent**             | Checkbox to indicate if the discount is a **percentage** instead of a fixed amount.                                                                                                    |
| **Days No Before Arrival** | Number of days before arrival that the booking must be made to qualify.                                                                                                                |
| **S\&P** (Stay & Pay)      | Marks the rule as a **Stay-and-Pay promotion** instead of a standard discount.                                                                                                         |
| **Send List Date**         | Defines when a list of bookings under this promotion should be sent.                                                                                                                   |
| **Deposit Date**           | Specific date by which a deposit must be paid.                                                                                                                                         |
| **Deposit Percent**        | The percentage of the booking cost that must be paid as a deposit.                                                                                                                     |
| Note                       | Add note to Special EB/SP - It will be visible in the Notification page , The Extras page  ![](<../../.gitbook/assets/image (364).png>)   ![](<../../.gitbook/assets/image (368).png>) |
| **Rejected**               | Marks the rule as rejected.                                                                                                                                                            |

***

### **Instructions: Adding a Special Early Booking Rule**

1. Navigate to the hotel and open the **Special EB/SP** tab.
2. Click **Add Special EB**.
3. Fill in the required fields:
   * Define **stay and booking periods**.
   * Choose whether the discount applies as a **fixed value or percentage**.
   * Set **deposit conditions** if applicable.
   * Apply **age restrictions** or weekday restrictions if needed.
4. Save the rule.
5. The rule will now automatically apply to qualifying bookings.

***

## 4. Special Stay And Pay Cost Rules

### Overview

The **Special Stay And Pay Cost Rules** tab allows you to configure _“Stay X nights, Pay Y nights”_ rules.\
These rules are commonly used in hotel contracts to provide special discounts to customers who stay for multiple nights.

### Purpose

The purpose of this functionality is to automate the application of promotional offers for accommodations.\
Examples:

* “Stay 7 nights, pay only 6”
* “Stay 14 nights, pay only 12”

The system will automatically calculate the correct price based on the rules defined here.

### Preconditions

* The hotel/extra must already be created in the system.
* The user must have edit rights on the contract.
* Commercial conditions (validity period, applicable days, type of offer) must be known.

### Instructions

1. Open the hotel/extra section.
2. Navigate to the **Special EB/SP** → **Special Stay And Pay Cost Rules** tab.
3. Click **Add Special SP** to create a new rule.
4. Fill in the available fields according to the contract conditions.
5. Save the changes.

### Field Descriptions

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| Field                           | Description                                                                                                                                                                                                      |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Stay Start / Stay End**       | Period of stay during which the rule applies.                                                                                                                                                                    |
| **Booking Start / Booking End** | Period when the booking must be made in order for the rule to apply.                                                                                                                                             |
| **Days of the Week**            | Select specific days of the week when the rule is valid (if restrictions apply).                                                                                                                                 |
| **Stay Days**                   | Minimum/maximum number of nights required to benefit from the offer.                                                                                                                                             |
| **Pay Days**                    | Number of nights the customer will actually pay (e.g., 7 nights stay, 6 nights paid).                                                                                                                            |
| **Days No Before Arrival**      | Number of days before arrival that the rule can be applied.                                                                                                                                                      |
| **EB**                          | Checkbox to link the rule to an Early Booking campaign.                                                                                                                                                          |
| **Contract**                    | Field to associate the rule with a specific contract.                                                                                                                                                            |
| Note                            | Add note to Special EB/SP - It will be visible in the Notification page , The Extras page   ![](<../../.gitbook/assets/image (365).png>)                            ![](<../../.gitbook/assets/image (367).png>) |
| **Rejected**                    | Marks the rule as rejected/deactivated (it will not apply).                                                                                                                                                      |
