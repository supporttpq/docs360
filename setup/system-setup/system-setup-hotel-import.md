# System Setup – Hotel Import

#### **Overview**

The **Hotel Import** section under the **System Setup** module allows the system administrator to configure default settings for hotel-related imports and pricing adjustments. These settings help standardize pricing calculations for single rooms, board supplements, and gala dinners, and define the default release hour for hotel bookings in the system.

***

#### **Purpose**

The purpose of this section is to ensure that all hotel imports into the system follow consistent pricing rules and time standards. This helps:

* Automate price adjustments for certain services.
* Maintain uniformity in hotel booking releases.
* Reduce manual errors when processing hotel data.

***

#### **Preconditions**

Before configuring the **Hotel Import** settings:

1. The user must have **administrator access** to the System Setup module.
2. Basic hotel data should already exist in the system or be ready for import.
3. You should understand the company’s pricing policies for single rooms, board supplements, and gala dinners.

***

#### **Fields and Instructions**

<figure><img src="../../.gitbook/assets/image (393).png" alt=""><figcaption></figcaption></figure>

1. **Hotel Release Hour**
   * **Description:** Set the hour to use for imported hotel releases. If not set, a system default (07:00) will be used.
   * **Format:** 24-hour time (HH:MM)
   * **Instruction:** Enter the default hour for the import hotel release. Example: `06:00` means that all imported hotels will be released at 6 AM.
2. **Single Room Supplement Price**
   * **Description:** Defines the percentage increase in price applied to bookings of single rooms.
   * **Format:** Percentage (%)
   * **Instruction:** Enter the standard markup percentage for single room bookings. Example: `2` means a 2% increase over the base price.
3. **Board Supplement Price**
   * **Description:** Defines the percentage increase applied for board (meal plan) supplements.
   * **Format:** Percentage (%)
   * **Instruction:** Enter the default markup percentage for board supplements. Example: `2` means a 2% increase on top of the base room price.
4. **Gala Dinner Price**
   * **Description:** Specifies the percentage increase for including gala dinner events in hotel bookings.
   * **Format:** Percentage (%)
   * **Instruction:** Enter the default markup percentage for gala dinner pricing. Example: `2` means a 2% increase on the booking price when a gala dinner is included.
5. Do not create extras for board basis

* Description: Check this if no extras shall be created for board basis during the import of a hotel contract. This is relevant for companies that do not need the board basis extras.
* Format: Checkbox

***

#### **Instructions for Use**

1. Navigate to **System Setup → Hotel Import**.
2. Set the **Hotel Release Hour** according to company standards.
3. Enter the percentage values for **Single Room Supplement**, **Board Supplement**, and **Gala Dinner Price** as per pricing policy.
4. Save the changes to ensure these defaults are applied to all imported hotel bookings.

***

This setup ensures that hotel prices are automatically adjusted according to company rules and that hotel availability is released consistently at the configured time.
