# Edit Transport Rule

### **Overview**

The **Edit Transport Rule** function allows administrators to modify an existing Transport Rule that controls how transports are generated and named within the system. A Transport Rule defines the structure, logic, and naming convention for the transport legs associated with a specific route or operational configuration.\
Through this interface, users can update the rule name and ensure that all previously generated transports remain consistent with the naming logic.

### **Purpose**

The purpose of editing a Transport Rule is to maintain accurate, consistent, and operationally correct route definitions. Editing is typically required when:

* The original rule name was created incorrectly.
* The naming convention changes and the rule must follow updated internal standards.
* A mistake in the configuration must be corrected.
* Operational changes require renaming existing generated transports.

A key system requirement is **uniqueness**:\
➡️ _Two Transport Rules cannot have the same name._

Additionally, when a rule name is updated:\
➡️ _All transports previously generated based on that rule must be automatically renamed to follow the new naming convention._

This ensures data integrity throughout the operational flow and prevents mismatches between Transport Rule names and underlying transport entries.

### **Preconditions**

Before editing a Transport Rule, ensure that:

1. You have **permission** to manage Transport Rules (usually an admin or configuration-level role).
2. The new Transport Rule name is known and confirmed.
3. You verify that **no other existing rule** already uses the intended new name.
4. The system is not actively generating transports based on the rule at the exact moment of editing.
5. Any teams dependent on the rule (transport, planning, ops) are informed if the rename affects their processes.

#### Editing Transport Rule Names

Transport Rule names can be edited at any time. Renaming a Transport Rule will automatically update the names of all transports generated from it, ensuring they continue to follow the established naming convention.

To maintain data consistency, the system does not allow two Transport Rules to share the same name.

<figure><img src="../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Example:**\
If a Transport Rule was initially created as `CPH_CHQ`, but the correct naming should be `CPH_CHQ_T1`, updating the rule name will also rename all associated generated transports accordingly.

#### Auto-Selecting Stay Days When Adding New Entries

When a user clicks the **“+”** button to add new stay days, the system automatically preselects the first available stay day from the drop-down list.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This behavior allows users to repeatedly press **“+”** and quickly add all remaining stay days in sequence, creating a faster and more efficient workflow.

#### Displaying Generated Transport Names in the Stay Days Table

In the Stay Days table, an additional column is introduced to display the name of the generated transport associated with each stay day.

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

The transport name is a clickable link. Selecting this link opens the corresponding generated transport in a new browser tab, allowing users to review or manage it without losing their place in the current view.

<figure><img src="../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

After the new Stay Days have been added, click the "Generate" button at the bottom right of the screen to generate eligible transports for them.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### Editing Dates Before Transport Generation

Users can modify the selected dates after the initial save, provided the transports have not yet been generated.\
This ensures flexibility during setup while still preserving data integrity once the generation process begins.

#### Extending Season Dates

The system allows users to extend the season by adjusting the start or end dates, as needed:

* **Extending the end of the season:** Users can add additional weeks at the end if the season is prolonged.
* **Extending the beginning of the season:** Users can add earlier weeks if the season starts sooner than originally planned.

When extending an existing season by adding only a few additional weeks, the system will **reuse the same fixed quota**.\
However, if a completely new season period is added, the system will **generate a new fixed quota**.

### Automatic Extension of Generated Quotas

Transport Rules can be configured far in advance to support long-term planning, including GDS transports defined several years ahead. To avoid unnecessary system load, generated quotas are limited in range and extended automatically over time.

#### How It Works

*   Transport Rules may be defined with dates far in the future.

    <figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
* The system generates quotas only for the **next 500 days**.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* A background service runs **once per week** and automatically extends the generated quotas, ensuring that quotas always exist up to **500 days ahead** of the current date.
* This automatic extension applies **only to Dynamic and CAR Transport Rules**.
* The 500-day limit is aligned with the existing limit used by the **price list generator**.

If a Transport Rule has valid dates and allotment defined in the future, the service ensures that its quotas continue to be extended without manual intervention.

### Add Season Support

#### Overview

Transport Rules support multiple seasons within the same rule. This allows long-term planning while keeping a single Transport Rule and consistent names for both the rule itself and all generated transports.

Each season represents a specific date period with its own pricing and travel configuration.

#### Purpose

The goal of season support is to address daily operational challenges and allow transport configurations to vary over time without duplicating Transport Rules.

This makes it possible to:

* Manage multiple seasonal setups under one Transport Rule
* Keep generated transport names consistent
* Adjust prices, stay days, and directions per season

#### How It Works

A single Transport Rule can contain several **date periods (seasons)**. For each season, the following can be configured independently:

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

For every season, the following shall be specified:

* **Start date**
* **End date**
* **Infant price**
* **Outbound settings**
* **Homebound settings**
* **Stay days**

{% hint style="warning" %}
Date periods must not overlap. If date periods are overlapping, you will not be able to save it, and the date box that makes the overlap will be marked red.&#x20;
{% endhint %}

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

#### Page Structure

The page is divided into two main sections:

**Top Section: Global Configuration**

This section contains settings that apply to the Transport Rule regardless of season.

It includes:

* Code
* Departure
* Arrival
* Transportation

The **Settings** section contains:

* **Status** – Defines the rule’s visibility in the system (e.g., Visible / Hidden).
* **Hide as filter on lists** – If checked, this rule will not appear as a filter option in lists.
* **Cancelation condition\*** - Select the cancellation condition that applies to this transport rule (mandatory).
* **Payment Rule** – Select a payment rule applicable to this transport.
* **Use change rule service** – If checked, activates the change rule service for this transport

**Bottom Section: Season-Specific Configuration**

The lower part of the page contains all data that varies per season.

**Date Period Table**

A table lists all configured date periods:

* Date periods are sorted with the **oldest at the top**
* New date periods are added at the **bottom**
* Date periods must **not overlap**

**Managing Date Periods**

* A date period can be **deleted** only if it is newly created and no data has been generated yet.
* The **Edit Quota** button opens the quota editor for the selected period.
* The **Edit Quota** button is shown only when a quota exists for that period.

When a new season is added, it is configured on the same Transport Rule page. The system reuses the **same transports** from the previous season and generates a **new fixed quota** for the newly created season.

This means the system does not create new transports for each season. Instead, it keeps the existing transport and adds a new fixed quota that applies only to the new season.

### FAQ

#### Can two Transport Rules have the same name?

No. Transport Rule names must be unique.

#### What happens when I rename a Transport Rule?

The system renames all previously generated transports based on that rule.

#### Can I change stay days or dates after saving?

Yes, as long as transports have not been generated yet.

#### Why can’t date periods overlap?

Overlaps would create ambiguous season logic. The system blocks it.

#### Why do quotas only exist 500 days ahead?

To reduce system load. A weekly background service extends quotas automatically.
