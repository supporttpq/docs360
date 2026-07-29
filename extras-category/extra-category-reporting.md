# Extra Category Reporting

## Extra Category Reporting

### Overview

The **Extras Category Reporting** feature automatically generates and sends a list of passengers who purchased extras from a specific category. For example, it can send a report daily for passengers returning home 4 days after their trip. The report is sent as a PDF via email.

### Purpose

This functionality provides timely information about passenger extras. It supports tracking, communication, and service follow-up.

### Requirements

* Confirm with the Web Master that the Windows service scheduler runs.
* Ensure the **Extras Category Reporting Service** is active.

### Configuration

#### Configure Email Center

In **Setup → E-mail Center**, configure the email sent by the service:

1. Select the relevant brand in the brand selector.
2. Select **Extra Category Reporting** in the **Email Type** dropdown.
3. Complete all required fields.
4. Click **Activate**.
5. Include a confirmation link if required:

```
http://emailtracking.tourpaq.com/EmailConfirmation.aspx?messageID=[MessageID]
```

The service does not send reports until the email is active.

#### Configure scheduler

In **Extras Setup → Extras Categories → Edit**, create a scheduler record:

1. Open the [**Communication** tab](extra-category-overview/communication-tab.md).
2. Click **Create**.
3. Configure the scheduler record.

For example, configure a daily 10:30 report. Include passengers returning home after four days.

The service produces the report as a PDF file.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (12).png" alt="Communication tab showing a reporting scheduler record"><figcaption></figcaption></figure></div>

### View sent emails

In **Tickets → E-ticket Overview**, review sent reporting emails:

1. Select the review period.
2. Click **Show default communication email types**.
3. Select **Extras Category Reporting** in the **Email Type** dropdown.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="E-ticket Overview showing Extras Category Reporting emails"><figcaption></figcaption></figure></div>
