# Questionnaire - Display

### **Overview**

The **Display** tab  is used to configure when and how the questionnaire is presented to customers. This is part of the customer feedback process used by an agency to assess customer satisfaction after their return from a trip.

This tab defines the date conditions and display timing for the questionnaire. It helps ensure that the form is made available at the right moment, maximizing response rates and ensuring relevance.

***

### **Purpose**

The purpose of this section is to:

* Determine **which date** should be used as a reference point for displaying the questionnaire.
* Define **how long before or after** the selected date the questionnaire should be shown.
* Control the **duration** of its availability (in days).

***

### **Preconditions**

Before configuring this section:

* The questionnaire should already be created under the **General** and **Question** tabs.
* The return date or any other reference date (like booking or departure) should be correctly stored in the system.
* You must have editing access to the **Spørgeskema (Welcome Home)** configuration interface.

***

### **Field Descriptions and Instructions**

#### **1. Date (Dropdown)**

* **Description**: This required dropdown allows you to select the reference date that the system will use to determine when the questionnaire should be displayed. (Return home date, Departure date, Booking date, Deposit payment date)

***

#### **2. Days b/a**

* **Description**: This field defines how many days _before_ or _after_ the selected reference date the questionnaire should be displayed.
* **Positive value**: Number of days **after** the selected date (e.g., "100" means show it 100 days after return home).
* **Negative value**: Number of days **before** the selected date (e.g., "-5" means show it 5 days before return home).

***

#### **3. Days no**

* **Description**: This field defines the number of consecutive days the questionnaire will remain visible and accessible to the user.
* **Default value**: `0` means the form will only be shown on the calculated display date.
* **Positive value**: Duration in days the questionnaire stays available (e.g., "7" means it can be accessed for 7 days).
* **Instructions**: Enter the number of days the questionnaire should remain active. Adjust according to feedback cycle and response expectations.

***

### **Example Configuration**

* **Date**: Return home date
* **Days b/a**: 2
* **Days no**: 5

➡️ The questionnaire will be displayed **2 days after** the user returns home and remain accessible for **5 days**.

***

### **Best Practices**

* Use a **reasonable delay** (1–3 days after return) to give customers time to settle before requesting feedback.
* Keep the form **open for at least 3–5 days** to maximize response rate.
* Monitor response timing trends and adjust values based on customer engagement data.
