---
description: >-
  The Generate Price List Service automatically creates price lists based on a
  resort or transport.
---

# Price List Generator

### **Overview**

The **Generate Price List** page allows users to create, view, and manage scheduled or manually generated price lists for different destinations, transports, and hotels.\
This functionality is essential for maintaining accurate and consistent pricing across all travel products in the system.

Importantly, this feature **enables the automatic creation of large numbers of price lists**, ensuring that pricing updates are performed systematically across multiple destinations and date ranges — **significantly reducing manual work** and minimizing the risk of human error.

***

### **Purpose**

The purpose of this page is to:

* Automate the creation of price lists for different markets, destinations, and transports.
* Provide visibility over all existing and scheduled price generation rules.
* Ensure that all active transport and accommodation combinations have valid pricing for the defined periods.
* **Reduce repetitive manual tasks** by allowing bulk and scheduled price generation based on configurable rules.

By using this tool, users can efficiently maintain pricing structures across the entire product portfolio without needing to manually update each route or resort.

***

### **Filters and Fields**

<figure><img src=".gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| **Field / Control** | **Description**                                                                           |
| ------------------- | ----------------------------------------------------------------------------------------- |
| **Departure from**  | Select the **departure start date**                                                       |
| **Departure to**    | Select the **departure end date**                                                         |
| **Arrivals**        | Filter by a specific **arrival point.**                                                   |
| **Resorts**         | Choose one or more **resorts** for which the price list should be displayed or generated. |
| **Transports**      | Filter by a specific **transport**.                                                       |
| **Display**         | After setting filters, click this button to display matching entries in the list below.   |
| **Clear**           | Resets all applied filters and displays all available records.                            |

***

### **Table Columns**

| **Column**              | **Description**                                                                                                                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Agency**              | The agency responsible for generating the price list (e.g., _Tourpaq DK_).                                                                                                                        |
| **Arrival**             | The destination city where the transport arrives (e.g., _Chania_, _Barcelona_). Mandatory field                                                                                                   |
| **Resort**              | The resort associated with the destination (e.g., _CHQ – Chania Resort_).                                                                                                                         |
| **Hotel**               | The specific hotel included in the price list generation rule.                                                                                                                                    |
| **Departure From / To** | Defines the valid departure date range for the transport or stay.                                                                                                                                 |
| **Transport**           | Shows the transport identifier or code (e.g., _BLL–CHQ–OLI+471b7671_).                                                                                                                            |
| **Fix Quotas**          | Displays the date range for which the quota and prices are fixed. These are the validity periods for generated prices. Mandatory if a Transport is selected.                                      |
| **Actions (Icons)**     | <p>- <strong>🖉 Edit</strong>: Opens the selected record for editing.<br>- <strong>🗑 Delete</strong>: Deletes the selected rule.<br>- History: Shows what changes have been made to the rule</p> |

***

### **Buttons**

| **Button**                                 | **Function**                                                                                                                                                                                                             |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Create**                                 | Opens a new line to create a **price list generation rule** manually. The user can define agency, resort, date ranges, or transport before saving.                                                                       |
| **Scheduled Rules to Generate Price List** | Opens an overview of **scheduled rules** that automatically trigger the generation of price lists according to pre-set conditions. This is the primary mechanism that allows **automatic mass creation** of price lists. |

***

### **Highlighted Rows**

Rows with a **red background** indicate records that are scheduled rules to generate pricelists. Each rule is scheduled when allotment from Hotel is generated or extended.

***

### **Edit a rule**

1. **Filter the records:**
   * Use the filters (Departure from, Resort, Transports, etc.) to narrow the list of relevant entries.
   * Click **Display** to show results.
2. **Review existing price list rules:**
   * Check if a rule already exists for the required date range.
   * Look for outdated or overlapping periods.
3. **Edit a rule:**
   * Click on the Pencil on the left, on the line you want to edit
   * Click on Fix Quota to define Price List rules
   * Save the rule.
4. **Generate or regenerate price lists:**
   * Click on the Save icon on the left to save the rule
   * The new rule will be placed in the schedule queue, waiting for the service to run. (The rule will be on the red background until the service has run, and the rule will become active).
5. **Verify fixed quotas:**
   * Ensure the **Fix Quotas** dates align with the season or travel period you want to price.

### **Steps to Add a Generation Rule**

1. Click on **Create** to add a new rule
2. Define all necessary fields (departure, arrival, resort, transport, and date range)  – After defining the basic resort and transport, save the rule to continue.
3. **Select Fix Quota** – Choose any available fix quota. Each fix quota is unique, and an interval can be set for it.
   * The **new interval** must be included within the parent fix quota.
4. **Add Rule to System** – Once added, the rule is active.
5. **Generate Price List** – The system will generate price lists for the current combination&#x20;

{% hint style="warning" %}
**This feature doesn't create prices; it only creates pricelists.**
{% endhint %}

***

### **Key Benefits**

* **Automatic generation** of multiple price lists across destinations and date ranges.
* **Reduced manual work** for administrators and pricing managers.
* **Increased accuracy** by minimizing manual input and ensuring consistent price coverage.
* **Faster seasonal updates**, as recurring rules handle repetitive price list creation.

***

### **Best Practices**

* Regularly review scheduled rules to ensure they reflect current transport and hotel combinations.
* Avoid overlapping date ranges to prevent pricing conflicts.
* Schedule updates ahead of major sales periods or seasonal rollouts.
* Maintain clear naming conventions for transports and resorts to simplify tracking.
