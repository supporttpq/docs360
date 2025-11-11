# Factor Matrix Template

#### **Overview**

The **Factor Matrix Templates** page provides an overview of predefined templates used to manage factor matrices within the system.

A _factor matrix_ is typically used to determine various load factors. This matrix provides an overview of expected transport occupancy, based on the relationship between departure weeks and the number of weeks remaining until departure.

#### **Purpose**

The purpose of **Factor Matrix Templates** is to:

* Store and manage reusable templates for transport matrix configurations.
* Maintain historical versions or separate templates for different campaigns, years, or destinations.

By using templates, administrators can quickly apply consistent pricing factors without manually recreating them for each new setup.

#### **Page Structure**

<figure><img src=".gitbook/assets/image (434).png" alt=""><figcaption></figcaption></figure>

| Column     | Description                                                                                                                                                                |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**   | Displays the name of the factor matrix template. The name should clearly describe the purpose or period it applies to (e.g., _Normal_, _Winter 2013_, _2012 Rhodes 26/6_). |
| **Delete** | The trash icon allows deletion of a template that is no longer required. Templates currently in use cannot be deleted.                                                     |

***

#### **Buttons and Actions**

| Button     | Description                                                                                                                                        |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Create** | Opens a new form for creating a **Factor Matrix Template**. You can define factors that will be applied when this template is selected.            |
| **Delete** | Removes the template from the list. This action should be performed only if the template is not referenced in active factor matrix configurations. |

#### **Example Use Cases**

* **Seasonal Templates** – Define templates such as _Summer 2025_ or _Winter 2025_ to handle seasonal factor differences.
* **Destination Templates** – Create separate templates for destinations like _Rhodes_ or _Alanya_ if each requires unique adjustment factors.
* **Testing and Historical Data** – Preserve old templates (e.g., _2012 Alanya 26/6_) for reference or auditing of past configurations.

#### **Instructions**

1. Navigate to **Transport → Factor Matrix Templates**.
2. To create a new template, click **Create**.
3. Fill in the relevant details for the template (name, associated factors, and configuration).
4. Click **Save** to finalize.
5. The new template will appear in the list and can later be selected when creating or updating a Factor Matrix.
