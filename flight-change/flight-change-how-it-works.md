# Flight Change - How it Works

#### **Overview**

When a change is made to a flight (e.g., a schedule adjustment or flight number update), the system automatically identifies the change and assigns a **Flight Change Type**.\
This type can be reviewed and manually edited if needed before proceeding.

#### **Steps to Process a Flight Change**

1. **Edit the Flight Details**\
   When a modification is made to a flight, the **Flight Change Type** field is automatically filled in based on the detected change (e.g., Tiny, Small, Large).\
   The user can manually adjust this field if necessary.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. **Save the Timetable Changes**\
   Select the row(s) where changes were made. Two options will appear:

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| **Option**              | **Description**                                                                                                                                                               |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Send Flight Change**  | Saves the changes to the timetable and immediately sends an email notification to all bookings affected by the changes.                                                       |
| **Queue Flight Change** | Saves the changes to the timetable but places the update in the **Flight Change Queue**. The change type is set according to the _Flight Change Type_ field in the timetable. |

3. **Manage Flight Changes**\
   After saving or queuing the changes, go to the[ **Flight Change**](./) menu to continue processing.
   * Select one or more flight changes (only those **in the queue**) and send the corresponding notification using the **Send Email** or **Send SMS** buttons.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;   4\. **Drop a Flight Change (Optional)**

* If a flight change is selected and the **Drop** button is used, that change is marked as **completed**, and **no further emails or SMS messages** can be sent for it.

#### **Flight Change Statuses**

| **Status**        | **Description**                                                                                                                          |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Queued**        | Initial state — the flight change has been created but not yet processed.                                                                |
| **Sent**          | The first notification (email or SMS) has been sent manually, and the process is now active.                                             |
| **Resend First**  | The first reminder email is sent if the passenger has not confirmed the initial notification. Timing is based on configuration settings. |
| **Resend Second** | A second reminder email is sent if no confirmation is received after the first resend.                                                   |
| **SMS**           | If the user has still not confirmed, an SMS is sent a specific number of hours before departure (as configured).                         |
| **Confirmed**     | The passenger has confirmed receipt of the flight change via the confirmation link in the email.                                         |
| **Dropped**       | The process was manually stopped. No additional notifications will be sent, and the change will not proceed further.                     |

#### **Summary**

This process ensures that:

* All passengers are properly informed of any flight updates.
* Communication is consistent and automated through the configured templates.
* Unresponsive passengers can be followed up through automated resends and SMS reminders.
