# Add room cost rule with "Per Room Per Stay" with a specific stay days value

### ✅ Overview

This page outlines how to **configure and test hotel room cost rules** in the booking system. You'll learn how to define cost rules based on stay intervals, validate that they apply correctly to bookings, and observe how they respond to different travel intervals.

The process is used to ensure that only **valid, matching cost rules** are applied to bookings and that mismatches result in no costs being allocated.

***

### 🎯 Purpose

The goal of this workflow is to:

* Ensure that room cost rules apply **only** when booking intervals match their configured periods.
* Validate that rule changes take effect without system errors.
* Confirm that the system correctly **includes or excludes costs** based on input data.

This testing is important to guarantee **financial accuracy** and **logic reliability** when travel agents or systems create real bookings.

***

### ⚙️ Preconditions

Before beginning this test, ensure:

* You have access to the **Hotel** and **Booking** modules.
* A hotel is available in the system.
* You have permission to create and edit room cost rules.
* The system has transport options with varying travel intervals.

***

### 🔄 Step-by-Step Instructions & Field Explanations

#### 1. Access the **Hotel → Hotels** Page

* **Action**: Open the Hotels section from the main navigation.
* **Expected**: A list of all configured hotels appears.
* **Purpose**: Begin the room cost configuration.

***

#### 2. Select a Hotel

* **Action**: Click on a hotel name.
* **Expected**: The hotel details page opens.

***

#### 3. Click on the **Room Costs** Section

* **Action**: Navigate to the "Room Costs" tab within hotel details.
* **Expected**: All existing room cost rules are shown.

***

#### 4. Click on **Create**

* **Action**: Click the "Create" or "+" button.
* **Expected**: A new row for a rule appears.

***

#### 5. Add Details for the Rule

* **Action**: Enter:
  * Cost value
  * Currency
  * Validity period (start and end dates)
  * Room type
  * Transport interval
* **Expected**: The entered values appear in the respective fields.

***

#### 6. For **Stay Type**, Select **Per Room Per Stay**

* **Explanation**: This rule type applies one total cost regardless of the number of nights.
* **Expected**: A new field called **Stay Days No** becomes visible.

***

#### 7. In the **Stay Days No** Field, Enter a Value

* **Action**: Enter a number (e.g., 5 for a 5-day rule).
* **Expected**: Value is shown in the input.

***

#### 8. Click on the **Save Icon**

* **Action**: Click the disk or save icon to commit the rule.
* **Expected**: A success notification appears.

***

#### 9. Create a New Booking Using a Transport Option with an Interval That Matches the Rule

* **Action**: Make a booking where the stay duration equals the `Stay Days No` defined earlier.
* **Expected**: Booking status is set to **OK**.
* **Why**: The rule should match this booking.

***

#### 10. Click on **Profit**

* **Action**: Open the booking and go to the **Profit** tab.
* **Expected**: Profit breakdown is displayed.

***

#### 11. Click on **Hotel Cost**

* **Action**: Go to the **Hotel Cost** section.
* **Expected**: All hotel-related cost lines are visible.

***

#### 12. Check the **Room Cost** Row

* **Expected**: Cost is correctly divided by the number of days for internal calculations.

***

#### 13. Return to the Hotel Details Page

* **Action**: Go back to the selected hotel.
* **Purpose**: To update the existing rule for additional testing.

***

#### 14. Click on the **Room Costs** Section Again

* **Action**: Return to the same rule configuration page.
* **Expected**: Room cost rules are visible.

***

#### 15. Edit the Existing Rule

* **Action**: Change the **Stay Days No** to a **different value**.
* **Expected**: Input updates visibly.

***

#### 16. Click on the **Save Icon**

* **Action**: Save the updated rule.
* **Expected**: A success alert is displayed.

***

#### 17. Create a New Booking with a **Different Interval**

* **Action**: Make a new booking with a stay length that **does NOT match** the updated `Stay Days No`.
* **Expected**: Booking status is still **OK**, but the cost rule should not apply.

***

#### 18. Click on **Profit**

* **Action**: Open the profit details for the new booking.
* **Expected**: The profit section loads correctly.

***

#### 19. Click on **Hotel Cost**

* **Expected**: Hotel cost section opens.

***

#### 20. Check the **Room Cost** Row

* **Expected**: **No cost is listed** — the rule does not apply due to interval mismatch.

***

### 🔍 Summary of Field Behavior

| Field / Action         | Behavior / Description                                              |
| ---------------------- | ------------------------------------------------------------------- |
| **Stay Type**          | Defines rule calculation method (Per Stay vs. Per Day)              |
| **Stay Days No**       | Limits rule to bookings with this exact stay duration               |
| **Transport Interval** | Defines arrival/departure match criteria                            |
| **Room Cost Row**      | Appears in Hotel Cost if rule matches booking                       |
| **Booking Profit**     | Reflects accurate margins only when a matching cost rule is applied |

***

### ✅ Outcome

By completing this process, you'll confirm that:

* Room cost rules apply only under valid conditions.
* Changes to rules dynamically affect future bookings.
* The system prevents mismatched rules from affecting cost calculations.
