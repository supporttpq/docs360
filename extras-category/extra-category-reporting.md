# Extra Category Reporting

#### Overview

The **Extras Category Reporting** feature automatically generates and sends a list of passengers who purchased extras from a specific category. For example, it can send a report daily for passengers returning home 4 days after their trip. The report is sent as a PDF via email.

#### Purpose

This functionality ensures your company has timely information about extras purchased by passengers, enabling better tracking, communication, and service follow-up.

#### Instructions

**1. Configuration**

To enable Extras Reporting:

1. Confirm with the \[\[Web Master]] that the Windows service scheduler is running for your company.
2. Ensure the **Extras Category Reporting Service** is active.

**2. Email Center Setup**

Configure the email that the service will send:

1. Navigate to **Setup → E-mail Center**.
2. Select the relevant brand from the upper-right corner.
3. Choose **Extra Category Reporting** in the **Email Type** dropdown.
4. Fill in all required fields.
5. **Activate** the email—if not activated, the report will not be sent.
6. _(Optional)_ Include a confirmation link in the email:

```
http://emailtracking.tourpaq.com/EmailConfirmation.aspx?messageID=[MessageID]
```

**3. Scheduler Setup**

To add a new scheduler:

1. Navigate to **Extras Setup → Extras Categories → Edit**.
2. Open the **Communication** tab.
3. Click **Create** to add a new scheduler record.

> Example: This scheduler can send a daily report at 10:30 for passengers who purchased extras in this category and are returning home 4 days later.

**Note:** The service produces the report as a PDF file.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**4. Viewing Sent Emails in E-ticket Overview**

1. Navigate to **Tickets → E-ticket Overview**.
2. Select the period you want to review.
3. Click **Show default communication email types** to see all types in the **Email Type** dropdown.
4. Select **Extras Category Reporting** to view the emails sent.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
