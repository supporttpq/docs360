# Name change rule

Some airlines (e.g. own charter flights) allow name changes until departure, while other airlines don't allow name changes at all or only up to 1 month before arrival.

### Overview

The **Name Change Rule** section allows you to control whether passenger name changes are permitted for a given transport booking.\
This rule helps define clear restrictions and deadlines for handling name change requests, both internally (by office staff) and externally (via the web booking).

### Purpose

The purpose of this functionality is to:

* Ensure consistent handling of name change requests.
* Limit name changes close to departure, avoiding operational or financial issues with suppliers (e.g., airlines, bus companies).
* Distinguish between changes allowed by office staff versus those made online by customers.

### Preconditions

* A transport option must already be created in the system.
* Applicable policies regarding name changes should be known before configuration.

### Instructions

1. Navigate to the transport setup section.
2. Open the **Name Change Rule** tab.
3. Configure the fields according to your company’s or supplier’s policy.
4. Save changes.

### Field Descriptions

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| Field                                            | Description                                                                                                                                                                                              |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Do Not Allow Name Change Office**              | When checked, office staff (back office users) are not allowed to change passenger names for this transport. This rule will apply after payment has been made.                                           |
| **Do Not Allow Name Change Web**                 | When checked, customers booking online via the web are not allowed to change passenger names.                                                                                                            |
| **Name change deadline (days before departure)** | Defines the last number of days before departure when a name change is permitted. Example: if set to **7**, name changes are allowed up to 7 days before departure. After that, no changes are possible. |
