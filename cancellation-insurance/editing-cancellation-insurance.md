# Editing Cancellation Insurance

### Overview

After booking a trip, a customer may decide to cancel the booking. **Cancellation insurance** represents the amount paid by the customer to receive reimbursement for a portion of the total booking cost in case of cancellation.

This form is used to **configure the rules** for how cancellation insurance prices are calculated, based on various factors such as brand, destination, travel type, and pricing criteria.

### Purpose

The purpose of this configuration is to define flexible pricing rules for cancellation insurance. This ensures that insurance costs can be automatically adjusted according to different booking parameters—making the process consistent and reducing manual setup.

### Instructions

There are **four available methods** for defining the price of cancellation insurance:

1. **Based on Passenger Price**
   * The fee depends on the total amount the passenger pays for the trip.
   * Up to **four different price ranges** can be defined.
   * Example: If the passenger’s trip price falls within the first range, a specific fee applies; if it falls in the second range, another fee applies, and so on.
2. **Based on Trip Duration**
   * The fee depends on how long the trip lasts.
   * Up to **four duration ranges** can be configured, each with a corresponding insurance fee.
3. **Based on Percentage of Passenger Price**
   * The insurance fee is calculated as a **percentage** of the total passenger price.
   * Example: If the percentage is 5% and the trip price is €1000, the insurance fee will be €50.
4. **Based on Transport Mode**
   * The fee depends on the **type of transport** used (e.g., flight, bus, or ferry).

**Cancellation Fee Application**

When a booking is canceled and **cancellation insurance has been paid**, the user can choose whether the insurance **covers** the cancellation:

* If the insurance **covers** the cancellation, the **cancellation fee** equals the **price of the cancellation insurance**.

<figure><img src="../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

### **Main Configuration**

| **Field**                 | **Description**                                                                                                                                                                                                                                                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Brand**\*               | Select the brand to which this cancellation insurance rule will apply. Mandatory field.                                                                                                                                                                                                                                 |
| **Arr. dest**\*           | Choose the arrival destination (e.g., Dubai). This is the location where the customer is traveling to. Mandatory field.                                                                                                                                                                                                 |
| **Booking start**\*       | Set the start date when the cancellation insurance becomes valid. Only bookings made after this date will be covered.                                                                                                                                                                                                   |
| **Booking end**\*         | Set the end date after which the cancellation insurance will no longer apply.                                                                                                                                                                                                                                           |
| **Type of rule**          | <p>Determines how the cancellation insurance is calculated. Options may include:<br>- <strong>Related to basic price</strong><br>- <strong>Related to transport type</strong><br>- <strong>Related to length of travel                                                         - Percentage of basic price</strong></p> |
| **Currency**              | Defines the currency used in all related price inputs (e.g., DKK - Danish Krone).                                                                                                                                                                                                                                       |
| **External Cancellation** | Allows linking to an external cancellation policy or provider (if integrated).                                                              - Gouda                                                                                         - Europieske                                                                |

***

### **Pricing Rules**

#### **Percentage of Basic Price**

| **Field**      | **Description**                                                                                                               |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Percentage** | Enter a percentage value. The cancellation insurance will be calculated as this percent of the basic travel price (e.g., 6%). |

***

#### **Related to Transport Type**

| **Field**  | **Description**                                                           |
| ---------- | ------------------------------------------------------------------------- |
| **Flight** | Enter a fixed insurance price (in DKK) when the transport type is flight. |
| **Bus**    | Enter a fixed insurance price for bus transportation.                     |
| **Train**  | Enter a fixed insurance price for train transportation.                   |

***

#### **Related to Length of Travel**

This section defines insurance pricing rules based on the length (duration) of the travel.

| **Fields**          | **Description**                                                                |
| ------------------- | ------------------------------------------------------------------------------ |
| **From(X) - To(X)** | Specify the number of days (length of travel). E.g., 1–7 days, 8–14 days, etc. |
| **Price**           | Fixed price amount charged for this duration range.                            |
| **Percent**         | Percentage of basic price                                                      |

> Only one of **Price** or **Percent** should be filled per row.

***

#### **Related to Basic Price**

This section allows creating tiered pricing based on the base booking price.

| **Fields**          | **Description**                                                               |
| ------------------- | ----------------------------------------------------------------------------- |
| **From(X) - To(X)** | Define price ranges (e.g., 0 to 99999 DKK).                                   |
| **Price**           | The cancellation insurance cost for bookings falling within this price range. |

***



