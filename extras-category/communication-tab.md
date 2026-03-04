# Communication Tab

### Overview

The **Communication** tab inside the _Edit Extras Category_ page is used to configure automated communication and reporting related to a specific Extras Category.

This functionality allows the system to:

* Generate scheduled reports
* Send automated email notifications
* Trigger PDF exports
* Control timing before departure
* Manage communication frequency (daily, weekly, monthly, annually, or custom)

Each row in this section represents a scheduled communication rule.

### Purpose

The Communication configuration ensures:

* Operational teams receive necessary extras lists.
* Suppliers receive timely passenger or service information.
* Reports are generated automatically before departure.
* Manual workload is reduced.
* Deadlines are respected.

This feature is typically used for:

* Activity providers
* Equipment rental suppliers
* Transfer services
* Homebound or outbound extras management

<figure><img src="../.gitbook/assets/image (683).png" alt=""><figcaption></figcaption></figure>

The Communication tab contains:

* A list of configured communication intervals
* Edit and Delete options
* A **Create** button to add a new communication rule

Each communication entry includes scheduling, delivery method, and reporting type.

1. **Interval** - Determines how often the lists are sent:

Examples:

* Custom Interval, 3 Days
* Annually (specific date) - Lists are sent on a specific calendar date for departures happening within _X_ days.
* Monthly (specific day) - Lists are sent on a selected day of the month (1–31) for departures happening within _X_ days.
* Weekly (specific weekday) - Lists are sent once a week on a selected day (e.g., Monday) for departures happening within _X_ days.
* Daily - Lists are sent daily for departures occurring within X days prior t&#x6F;_&#x58;_ days before the send date.

This determines the recurrence pattern.

2. **Days Before Departure** - Specifies how many days before departure the report should be generated or sent.

Examples:

* 0 = same day as departure
* 1 = one day before departure
* 2 = two days before departure

This ensures suppliers receive information in advance.

3. **Hour** - The exact hour (in Denmark time) when the list is automatically sent.
4. **Email** - The recipient email address where the report or communication will be sent. Multiple recipients may be configured depending on system capabilities.
5.  **FTP** - Indicates whether the communication is sent via FTP.

    * ✔ = Enabled
    * ✖ = Disabled

    Used when automated file transfer to external systems is required.
6. **Communication** - Contains a **View** link. This allows reviewing communication details
7. **Reporting** - Specifies the report template being generated.

Example:\
Homebound Extras List PDF

8. **Empty List** - If checked, the system will send an empty list even when there are no bookings.
   * ✔ = Send even if empty
   * ✖ = Do not send if empty
9. **Generate Dep date Only** - The report will include bookings only from the departure date and not from the entire interval (the interval starting from the current date until departure date set in " Days Before Departure").
10. **Edit icon (Pencil)** - Allows modification of an existing communication rule.
11. **Delete Icon (Trash**) - Removes the communication rule.

Once the communication rule is set and saved, the system will automatically generate and send the lists according to the defined schedule. Sent communications can be reviewed in the **Communication** log.

### Example Configuration

#### Example: Weekly Activity Supplier Report

| Field                   | Value                     |
| ----------------------- | ------------------------- |
| Interval                | Weekly, Monday            |
| Days Before Departure   | 2                         |
| Hour                    | 10:00                     |
| Email                   | supplier@activity.com     |
| FTP                     | Disabled                  |
| Reporting               | Homebound Extras List PDF |
| Empty List              | No                        |
| Generate Dep. Date Only | Yes                       |

#### Result:

* Every Monday at 10:00
* The system sends a PDF report
* Includes bookings departing in 2 days
* Only includes relevant departure date data
* No report generated if no extras exist
