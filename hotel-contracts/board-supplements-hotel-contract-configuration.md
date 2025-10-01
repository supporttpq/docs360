# Board Supplements - Hotel Contract Configuration

### Board Supplements

#### 🧾 **Overview**

The **Board Supplements** tab it is used to configure additional board options for a hotel contract. These supplements allow different pricing or availability based on the guest’s age, board type, or other custom criteria.

***

#### 🎯 **Purpose**

To define **extra board-related charges** or **variations** applicable to hotel guests beyond the default board package, such as upgrades to All-Inclusive or Half-Board, including conditions like age restrictions or specific categories (e.g., child, adult).

***

#### ✅ **Preconditions**

Before adding board supplements:

1. The hotel contract must already be created.
2. The standard **Board Types** must be set up in the system.
3. The relevant **periods and room types** should be configured to ensure supplements are aligned with the valid stay dates.

<figure><img src="../.gitbook/assets/image (289).png" alt=""><figcaption></figcaption></figure>

***

#### 🛠️ **Instructions & Field Descriptions**

| **Field**                   | **Description**                                                                                                                        |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **BOARD**                   | Dropdown to select the base board type. This indicates the board level the supplement is related to.                                   |
| **FROM / TO (AGE)**         | Define the applicable **age range** for the supplement. Guests whose age falls within this range will be eligible for this supplement. |
| **EXTRA CATEGORY**          | Select extra category.                                                                                                                 |
| **PRODUCT**                 | A dropdown to associate a **specific product or service** (e.g., "All-Inclusive Upgrade") offered as a supplement.                     |
| **NAME**                    | Internal or display **name of the supplement** (e.g., AI for All-Inclusive). Helps in identifying the supplement in listings.          |
| **CODE**                    | Unique **code identifier** for the supplement, often used for internal reference.                                                      |
| **CLEAR (✕)**               | This icon clears the row’s input fields, allowing a quick reset without deletion.                                                      |
| **TRASH BIN ICON (🗑️)**    | Permanently deletes the row from the list of supplements. Use with caution.                                                            |
| **ADD SUPPLEMENT (Button)** | Once the row is filled out, press this to **save** the supplement. New rows can be added with each click.                              |

***

### Board Basis - Board Supplememts

#### **Overview**

**Board Basis**: Define supplements per board type and age category.

<figure><img src="../.gitbook/assets/image (295).png" alt=""><figcaption></figcaption></figure>

#### Fields and Definitions

| Field              | Description                                                                                                                   |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| **Board Type**     | Select the board for which the supplement applies (e.g., AI - All Inclusive, HB - Half Board).                                |
| **From / To Age**  | Define the age range for which this supplement cost is valid (e.g., 3 to 5 years).                                            |
| **Extra Category** | Select the extra category                                                                                                     |
| **Product**        | Select a related product/service if this supplement is linked to one                                                          |
| **Name**           | Internal or display **name of the supplement** (e.g., AI for All-Inclusive). Helps in identifying the supplement in listings. |
| **Code**           | Reference code used for exports, contracts, or internal tracking.                                                             |
| **Clear (×)**      | Removes the entry row.                                                                                                        |
| **Period ID**      | Indicates the validity period for the cost. These IDs map to the ones defined in the **Periods** tab.                         |
| **Cost**           | Amount charged as supplement for the specified board, age, and period.                                                        |
| **Rooms**          | Room codes where this supplement applies.                                                                                     |

***

#### How It Works

1. For each **board type**, define supplements by **age range** and **period**.
2. Assign a **cost** per period and specify the **rooms** it applies to.
3. Optionally, link supplements to **products** and assign codes for contract exports.

Note: If in System Setup / [Hotel Import](../setup/system-setup/system-setup-hotel-import.md) is checked the option 'Do not create extras for board basis', the Board Basis will not be displayed in the menu and also the Extras from the Board Basis will not be created (display) in the imported hotel contract.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Gala Dinner – Board Supplements

#### Purpose

The **Gala Dinner** tab is used to configure mandatory or optional special occasion supplements, such as New Year’s Eve or Christmas dinners. These supplements are often age-dependent and may vary by board type, extra category, or product association.

***

<figure><img src="../.gitbook/assets/image (297).png" alt=""><figcaption></figcaption></figure>

***

#### Fields and Descriptions

| Field                     | Description                                                                        |
| ------------------------- | ---------------------------------------------------------------------------------- |
| **Board Type**            | Select the board type the gala dinner applies to (e.g., AIP – All Inclusive Plus). |
| **Age From / To**         | Define the age range of guests this cost applies to.                               |
| **Extra Category**        | Tag the supplement for categorization (e.g., "Pension").                           |
| **Product**               | Associate a product with the gala dinner (e.g., "All Inclusive").                  |
| **Name**                  | Display name of the gala dinner event (e.g., "All Inclusive").                     |
| **Code**                  | Internal or contractual reference code (e.g., "AI MANA").                          |
| **Start Date / End Date** | Define the date(s) for the dinner (e.g., 17-12-2025).                              |
| **Cost**                  | Amount charged to applicable guests.                                               |
| **Clear (×)**             | Clears the entry from the row.                                                     |
| **Delete (🗑️)**          | Removes the row from the list.                                                     |

***

#### How to Add a Gala Dinner

1. Click **Add Gala Dinner**.
2. Select a **Board Type**.
3. Define the **age range** to apply the supplement.
4. Select an **Extra Category** and **Product**.
5. The **Name** and **Code is autocompleted**.
6. Choose a **Start** and **End Date** (usually a single day).
7. Specify the **Cost**.
8. Save the entry. The system will apply this charge during bookings matching the criteria.

***

#### Related Workflows

* The **Gala Dinner** supplement is automatically added to the price during booking creation if the stay includes the defined date.
* Supplements are visible in pricing breakdowns, exports, and customer invoices depending on system configuration.

***

#### Tips

* Use meaningful **codes** for easy contract reference.
* Multiple gala dinners can be added for different dates or age categories.

