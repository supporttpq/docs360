# Questionnaire - Resource

### ✅ Overview - Survey resources

The **Survey Resources** tab in the Tourpaq "Welcome Home" questionnaire module allows administrators to control **where and when** a specific survey will be sent. Each entry defines a **resource mapping** between an agency, transport (optional), and time interval. This allows **precise targeting** of survey delivery based on travel context.

<figure><img src="../../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

***

### 🧭 Purpose

To define **which travelers** (based on their agency, travel period, and transport) should receive the selected questionnaire, ensuring relevant and timely feedback collection.

***

### 📋 Screen Elements

| Column          | Description                                                                                                                                                                                        |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Resource ID** | Unique system-generated identifier for each resource entry. Used internally for reference.                                                                                                         |
| **Agency**      | The tour operator or brand (e.g., **Tourpaq DK**) responsible for the bookings included in the survey.                                                                                             |
| **Transport**   | (Optional) Filter that allows targeting surveys to passengers using specific transport methods (e.g., charter flights). If empty, applies to all transports.                                       |
| **Interval**    | The date range during which **arrival dates** must fall to trigger the survey. For example, `26 Jun - 29 Jun` means that only travelers arriving within that range will receive the questionnaire. |

***

### ➕ Actions

#### 🟦 Create Button

* Opens a form to **add a new survey resource rule**.

<figure><img src="../../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure>

* You must define:
  * Agency
  * Date interval (arrival period)
  * (Optional) Transport, Resort, Hotel, Room

#### 🗑️ Delete Icon

* Removes the survey resource rule.

***

### 📌 Best Practices

* Always define **non-overlapping intervals** to prevent multiple surveys from being sent to the same passenger.
* If you work with multiple brands or transport types, use **multiple entries** to target them properly.
* Regularly review and **update intervals** before high season to keep the survey distribution relevant.



### ✅ Overview - Question resources

The **Question Resources** section allows the admin to define specific **questions** included in the Welcome Home survey and how these questions behave in different booking contexts. This ensures that feedback is gathered in a relevant, personalized, and conditional manner.

Each row in this view maps a **question to a specific logic condition**, such as only showing it if a related question was answered in a certain way (e.g., "Yes").

***

### 🧭 Purpose

* To manage and assign questions dynamically in a survey.
* To define **conditional questions** that are shown only when certain criteria are met.
* To tailor the survey experience to the **traveler's booking attributes**, such as type of meal plan or use of the mobile app.

***

### 📋 Interface Explanation

| Column                | Description                                                                                                                                                      |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Resource ID**       | Internal unique identifier for the question resource (used for tracking and debugging).                                                                          |
| **Question**          | The content of the question that will appear in the questionnaire, usually phrased in the customer’s language.                                                   |
| **Related Question**  | Defines a condition: the current question will be shown only if the traveler gave a specific answer to the listed related question. This allows dynamic surveys. |
| **Accepted Response** | The expected response to the **related question** that triggers this question to appear (e.g., “Yes”, “Morgenmad”, “All Inklusive”).                             |
| 🗑️ **Delete Icon**   | Removes the question from the current questionnaire structure.                                                                                                   |

***

### 🛠️ Actions

#### 🟦 Create Button

Opens a form to add a new question resource. You’ll define:

<figure><img src="../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>

* Question - select question
* Show only if on related question - Cannot set this for "free text answer" question. Please do not condition listing of one question to a question just before it. They should be listed on separate screens under Web Customer Center. This usually means they should be 3 questions distance apart.
* It is given this accepted response - allow the desired response depending the selected question
* Rooms - select the room type

#### 🗑️ Delete Button

Removes the question resource from the list. ⚠️ Use with care — this will remove the question from being asked in future surveys tied to this schema.

***
