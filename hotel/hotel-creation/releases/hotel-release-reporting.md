# Hotel release - Reporting

### Overview

The **Hotel Release Reporting Scheduler** is a set of configurable rules that are executed periodically by a Windows service. The scheduler automates the release of hotel rooms according to the rules defined in Tourpaq Office, ensuring timely notifications to suppliers and proper management of allotments.

### Purpose

The scheduler allows administrators to:

* Automate hotel room release reports on a daily, weekly, monthly, or annual basis.
* Ensure consistent and timely execution of release rules.
* Reduce manual work for hotel release management.

### How to Add a New Rule

To configure a release reporting rule for a hotel:

1. Navigate to **Dashboard → Hotel → Release Tab → Scheduler**.
2. Click **Add Record** to create a new scheduler row.
3. Enter the required details for the scheduler (hotel, dates, frequency, etc.).
4. Click **Insert** to save the new scheduler row.
5. To modify an existing scheduler row, edit the row directly in the grid and click **Update** to save changes.

<table><thead><tr><th width="208.4444580078125">Column name</th><th>Description</th></tr></thead><tbody><tr><td>Interval</td><td><p>Interval specifies how often the scheduler it will be send.</p><ul><li>If <strong>Daily</strong> is chosen the scheduler will run every day. Next to interval drop down is a date field and if chosen it will run the scheduler not before that date.</li><li>If <strong>Weekly</strong> the scheduler will run every week at a mandatory day specified right next to the interval drop down.</li><li>If <strong>Monthly</strong> is chosen the scheduler will run every month on a day specified right next to interval drop down.</li><li>If <strong>Annually</strong> is chosen the scheduler will run every year on a day specified right next to interval drop down.</li></ul></td></tr><tr><td>Days After</td><td>The value specifies the number of days after the release date. Ex.: If the scheduler is set to be sent every Friday (10.01.2014) and the Days after is 7 days then the the release will be made in the interval 10.01.2014 to 17.01.2014.</td></tr><tr><td>Hour</td><td>The hour when the hotel allotment list will be send. The field is mandatory</td></tr><tr><td>Email</td><td>The email address that will receive the list.</td></tr><tr><td>Room</td><td>Is a dynamic list of room assigned to the current hotel. If not chosen the rule will apply for all rooms.</td></tr><tr><td>Start Period</td><td>The allotment will be released not before the Start Period.</td></tr><tr><td>End Period</td><td>The allotment will be released not after the End Period.</td></tr><tr><td>Cut Down Allotments</td><td>If On the available rooms will set equal with booked rooms and free rooms will be zero. Otherwise the room availability will not be modified.</td></tr></tbody></table>

### Scheduler Types

**1. Daily Release Scheduler**

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs **every day** starting from the first execution date.
* Example:
  * Service first runs on **24.03.2025** for interval **24.03.2025 – 31.03.2025**.
  * The rule’s allowed interval is **27.03.2025 – 31.03.2025**, so only dates **27 – 31.03.2025** are released.

2. **Weekly Release Scheduler**

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs **once a week** on a specific day of the week.
* Useful for hotels that want to release rooms on a consistent weekly schedule.

3. **Monthly Release Scheduler**

<figure><img src="../../../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs **once a month** on a specific day of the month.
* Ideal for monthly batch updates of hotel room availability.

4. **Annual Release Scheduler**

<figure><img src="../../../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Runs **once a year** for the entire specified start–end period.
* 📝 **Note:** In annual mode, the **“Days after”** field is ignored.

#### Notes

* Each scheduler is linked to a **specific hotel** and cannot apply to multiple hotels simultaneously.
* Scheduler execution is handled by the Windows service; administrators only need to configure rules in Tourpaq Office.
* Logs and reports for each run are generated automatically and can be reviewed for auditing purposes.

