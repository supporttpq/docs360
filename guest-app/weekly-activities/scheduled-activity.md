# Scheduled Activity

#### **Overview**

The **Scheduled Activity** tab allows users to configure recurring or one-time activities for specific hotels and dates within a selected time range.\
It provides more granular control compared to **Weekly Activity**, as each day of the week can have its own configuration — such as different times or service phone availability.

This tab is typically used to plan and display activities or service phone hours visible in the **Guest App** for guests staying in those hotels.

#### **Purpose**

The purpose of the **Scheduled Activity** configuration is to:

* Define daily service or activity schedules for selected hotels.
* Allow flexible per-day setup within a given date range.
* Support guide and customer service visibility in the **Guest App**.
* Synchronize service availability and timing for different resorts and hotels.

#### **Form Fields**

<figure><img src="../../.gitbook/assets/image (435).png" alt=""><figcaption></figcaption></figure>

| **Field**                | **Description**                                                                                      |
| ------------------------ | ---------------------------------------------------------------------------------------------------- |
| **Start Date**\*         | Defines when the scheduled activity period begins.                                                   |
| **End Date**\*           | Defines when the scheduled activity period ends.                                                     |
| **Title**\*              | Name of the scheduled activity (e.g., “Christmas Party”, “Service Phone”).                           |
| **Resort**\*             | Choose one or multiple resorts included in this activity.                                            |
| **Hotels**               | Select specific hotels to apply the activity to.                                                     |
| **Service Phone Text**\* | Add the message or description that will be displayed in the Guest App (e.g., “Service Phone text”). |

\*Fields marked with an asterisk (\*) are mandatory.

#### **Daily Setup Table**

Below the main fields, users can define specific configurations per **hotel** and **day of the week**.

| **Column**                      | **Description**                                                                                                                                              |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Show**                        | Show/Hide Hotel for dates in grid                                                                                                                            |
| **Hotel Name / Code**           | Displays the hotel name and internal hotel code.                                                                                                             |
| **Description**                 | Optional note related to that hotel’s activity.                                                                                                              |
| **Day Columns (Monday–Sunday)** | Each day of the week is represented by a column, showing the exact date and week number. Users can enable “Service Phone” or define a specific time per day. |

**Available options per day:**

* ✅ **Service Phone** — Enables service phone for that day.
* 🕒 **Time Field** — Defines a specific start time (e.g., 14:00) for that activity or service.
* Empty — No service or activity is set for that day.

This allows maximum flexibility — for example, a service can run daily for one hotel, but only twice a week for another.

#### **Example**

In the screenshot above:

* **Title:** Christmas Party
* **Date Range:** 01-12-2025 → 31-12-2025
* **Resorts:** Multiple selected
* **Hotels:** PAR SES, Ramada
* **Service Phone Text:** “Service Phone text”

**Configuration details:**

* For **PAR SES**, Service Phone is enabled daily (Monday to Sunday).
* For **Ramada**, Service Phone is active with a specific time (14:00) on selected days.

This setup ensures that guests staying at these hotels will see a consistent service phone schedule in the Guest App during the configured period.

***

#### **Save or Cancel**

After all settings are configured:

* Click **Save** to confirm and activate the schedule.
* Click **Cancel** to discard the changes.

***

#### **Visibility and Access**

As with Weekly Activities:

* **Admin Users** can manage all scheduled activities across all resorts and agencies.
* **Guide Users** can view or manage scheduled activities **only if they have access to all the resorts** linked to those activities.
