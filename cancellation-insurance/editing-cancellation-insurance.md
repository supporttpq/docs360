# Editing Cancellation Insurance

After booking a trip, the customer might want to cancel the booking. Cancellation insurance is the amount the customer pays for this case.

This form is used to configure cancellation insurance rules based on various criteria such as brand, destination, travel type, and pricing factors.

There are 4 ways to set the price for the cancellation insurance:

* Bulleted list item The first method would take into account the price that a passenger pays for the trip. It should be possible to insert 4 different ranges for the price. For instance: if the passenger’s price will fit in the first range, the cancellation insurance will have a value; if it fits in the second range, it will have another value, and so on.
* Bulleted list item The second method would take into account the duration of the trip. It should also be possible to insert 4 different ranges for the duration.
* Bulleted list item The third method would set the fee using a given percentage. In this case, the fee will be the percentage of the passenger’s price.
* Bulleted list item The fourth method would take into account the transport mode.

If cancellation insurance is paid, when cancelling the passengers, we can opt that the cancellation insurance will cover it. In this case, the cancellation fee will be equal to the price of the cancellation insurance.

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



