# Transport Reporting

Transport Reporting is a way to send the passenger name list (**PNL**) to the airline. There are multiple methods to send the PNL.

The default reporting method is set in **Transport → General tab**. A tour operator code is required for some reporting types.

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

Another reporting method can be set from the **Timetable**. This will override the method selected in the **Transport → General tab** for the duration of the flights.

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

The last reporting method can be set up from the **Communication** tab.

By clicking **Add schedule**, you can define rules that send communication files to the specified email address.

**Defining separate rules for each departure date**

The rules shown in the image below will send communication files to the configured email address for all bookings on the selected transport, **20**, **10**, and **1** day(s) before departure.

<figure><img src="../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

**Defining one rule for an interval of days**

You can combine many rules into one using **Departure Date End**. Define an interval (**Departure Date** to **Departure Date End**). If you also use the **Minutes** interval, communication files are sent every N minutes. The rule shown below sends communication files to the configured email address for the selected transport every **60 minutes** for all bookings with **1, 2, 3...50** days before departure.

<figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

When you use **Departure Date End**, you cannot copy the rule to create a new one.

It is also possible to define rules like the one below (using **Hour**):

<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

Rules 1, 2, and 3 are overridden by the last rule. The only difference is the email address to which the communication files are sent. This method can also override previously selected methods of defining communication files.

## **Communication Schedule – Handling Changed Passenger Seating After Departure**

### **Overview / Purpose**

This rule ensures that changes to passenger seating made **after departure** are still communicated to transport suppliers. It is specifically useful for **one-way homebound transports**, where new passengers may be added or existing ones removed after the outbound trip has already departed.

<figure><img src="../../.gitbook/assets/image (350).png" alt=""><figcaption></figcaption></figure>

### **How It Works**

* Normally, communication schedules are set to capture bookings before departure.
* For one-way homebound trips, bookings created after the outbound departure might be missed in the initial communication.
* By creating a **communication scheduler with a -6 days offset**, the system can capture bookings made during the travel period and re-send updated lists to suppliers.
* This ensures suppliers (e.g., Paxport) receive the latest **Passenger Name List (PNL)** with accurate seat assignments before the homebound departure.

### **Key Features / Functions**

* **Catches late bookings or seating changes** for passengers on one-way homebound transports.
* **Re-sends communication** to suppliers so they always have the latest seating information.
* Works in conjunction with existing outbound and homebound schedulers.

### **Examples / Scenarios**

* **Example 1:**
  * Outbound: 01-07-2026
  * Homebound: 07-07-2026
  * A passenger books only a one-way homebound trip on 03-07-2026.
  * Since the outbound list was sent earlier, the passenger would normally not appear.
  * With a -6 days scheduler, the booking is captured and included in the updated PNL.
* **Example 2:**
  * A passenger cancels their homebound seat after departure.
  * The updated communication ensures the transport supplier sees the removal in time.

### **Notes / Best Practices**

* Always set up the **-6 days before departure scheduler** for one-way homebound transports.
* Coordinate with suppliers (e.g., Paxport) to confirm they accept and process re-sent lists.
* Avoid overlapping or redundant schedulers that might generate duplicate messages.
* Regularly test communication rules to ensure last-minute seating changes are reflected correctly.

Reporting is managed by a **Windows Service** that checks for schedulers every **9 minutes**. Schedulers are set up in the **Transport → Communication tab**.

**Fields**:

* Departure date: number of days before departure when the report will be sent
* Hour: the hour at which the report will be sent
* Minutes: the report will be sent every N minutes
* Email: the email address that will receive the report
* Stop sale: if checked, no more bookings can be made on the flight
* Communication: allows the user to view sent lists
* Alternative reporting: list type to be sent

> 📝 **Note:** Minutes and Hour cannot be set on the same rule.

**Resend passenger list**

Allows you to resend the passenger list from a selected date to a specified email address without creating a schedule.

Alternative reporting types:

* Passenger list with addresses
* Passenger name list (Air)
* Inflight
* Bus Feed
* Gate Gourmet
* Infection Detection
* AirSeven Full

**Important**

To use reporting types, email templates must be created in the email center.

**Sent emails are not saved anywhere.**

**Radix Data** and **Inflight Service** require credentials that are entered in **System Setup**. Credentials are obtained from the respective companies.

### Resend transport reporting <a href="#resend-transport-reporting" id="resend-transport-reporting"></a>

This feature permits the user:

* To have a better overview of the transport reporting communication rules.
* To resend a full transport reporting.

It can be accessed from **Transport → Resend Transport Reporting**.

<figure><img src="../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

Available filters:

* Reporting type - This field indicates the source or category of the flight information. It might distinguish between scheduled flight plans, real-time tracking data, or historical records.
* Departure Date - This field specifies the calendar date on which the flight is scheduled to depart from its origin airport.
* Departure Airport - This field identifies the airport from which the flight originates. It is often represented by a standard airport code, such as an IATA code.
* Arrival Airport - This field identifies the airport where the flight is scheduled to land. It is also typically represented by a standard airport code.
* Airlines - This field indicates the airline operating the flight. It can be represented by the airline's name or its designated airline code.

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

**Resending section**

* Override Reporting - overrides the reporting type set on the transport
* Email - destination email address
* Do not send on FTP - sends the report by email only (no FTP/SFTP upload)

**Authentication**

A Secure Shell (SSH) public-private key pair is used to authenticate. The private key is generated by the tour operator and remains secret. The public key is shared with Transavia. When an SSH client connects, it sends a message with the public key and signature. Transavia validates the message and checks that the user and key are recognized.

**Generating SSH public-private keypair**

Online there are multiple guides that explain how to generate an SSH public-private key pair. We recommend using ssh-keygen ([https://www.ssh.com/academy/ssh/keygen](https://www.ssh.com/academy/ssh/keygen)). To create an SSH public-private key pair on your local computer using the ssh-keygen command from PowerShell or a command prompt, type the following: `ssh-keygen -m PEM -t rsa -b 4096`. Enter a filename and a passphrase for the file.

**Supported SSH key formats**

We currently support SSH protocol 2 (SSH-2) RSA public-private key pairs with a minimum length of 2048 bits. Other key formats such as ED25519 and ECDSA are not supported.

**Confirmation e-mail**

Once Transavia has configured the public key, a confirmation email is sent to the email address you used to share the public key. This confirmation email is sent by [team\_allotment@transavia.com](mailto:team_allotment@transavia.com). The confirmation email contains the information you need to connect to SFTP, including a username, host, and port.

**Workflow**

1. Generate an SSH public-private key pair.
2. Share the public key via email with technical partner support: [technical.partnersupport@transavia.com](mailto:technical.partnersupport@transavia.com).
3. Await the confirmation email containing connection information.
4. Connect to SFTP using the username, key file, and passphrase.
5. Upload PAX data files to the root directory.

After a PAX data file is uploaded, Transavia automatically picks it up for processing. If the file is removed from your directory, it is being processed.

### Transport Supplier <a href="#transport-supplier" id="transport-supplier"></a>

The Transport Supplier allows sharing the same communication for one transport supplier across several transports.

One transport may have a single Transport Supplier for all rotations in the fix quota(s), but another transport may have several transport suppliers for a single fix quota.

Transport Supplier can be found in **Edit Transport → Communication tab**:

<figure><img src="../../.gitbook/assets/transportSupplierTabLocation-956e7aac017ec67cc51896a22b5c413b.png" alt=""><figcaption></figcaption></figure>

This tab shows the list of communication triggered by the rules from the Transport Supplier.

<figure><img src="../../.gitbook/assets/transportSupplierTabList-e396a773c38ce57854d0a7cbe90b5761.png" alt=""><figcaption></figcaption></figure>

This list can be ordered by Reporting Method, Transport Supplier and Period.

You can filter this list by using Start Date, End Date and Reporting method. Start date and End date will return a list that has the period inside the interval set by these two fields.

This table contains the following columns:

* Out/Home - transport PNL ways
* Reporting Method - Describes **how information is submitted or reported** (e.g., automatically via API, manually via upload, email, or through a platform).
* Transport Supplier - Refers to the **company or vendor providing the transport service**, such as airlines, bus companies, or shuttle services.
* Period - Could refer to the **reporting or scheduling time frame** (e.g., daily, weekly, monthly) or the specific **date range** covered by the report or operation.
* Hour - Most likely relates to the **time of day** for the transport, scheduling, or when a report is due or generated.
* Email - Field to input one or more **email addresses** where notifications, reports, or PNL documents are sent.
* Communications - link to PNL data files (clicking opens a modal window with file links; each link opens in a new tab).

<figure><img src="../../.gitbook/assets/transportSupplierTabModal-a9bb0c7ec87df174f925a60f198ee44f.png" alt=""><figcaption></figcaption></figure>

### FAQ

**Where do I set the default reporting type?**\
Set it on the transport in **Transport → General tab**.\
Example: Set **Passenger name list (Air)** as the default for all departures on that transport.

**How do I override reporting for specific departures?**\
Set a reporting type on the **Timetable**. It overrides the transport default for the flight period.\
Example: Use **Paxport** only for a specific season, while the transport default stays as **Passenger name list (Air)**.

**Where do I configure schedules for sending PNL files?**\
Use **Transport → Communication tab** and click **Add schedule**.\
Example: Create a schedule with **Departure date = 10** to send the PNL 10 days before each departure.

**Why can’t I copy a schedule rule that uses Departure Date End?**\
Rules that use **Departure Date End** cannot be copied by design.\
Example: A rule like **Departure date = 1** and **Departure Date End = 50** (with **Minutes = 60**) must be recreated manually if you want a similar rule.

**What is the -6 days scheduler used for?**\
It helps capture late bookings or seat changes made after outbound departure for one-way homebound transports.\
Example:\\

* Outbound: 01-07-2026\\
* Homebound: 07-07-2026\\
* One-way homebound passenger is added on 03-07-2026\\
* The -6 days scheduler makes sure the updated list is re-sent, so the supplier has the latest seating before 07-07-2026.

**Why are my emails “missing” later?**\
Sent emails are **not saved**. Use the **Communication** field to view sent lists/files instead.\
Example: If a recipient says they did not receive an email, open the **Communication** view and verify whether the file/list was generated and sent.

**What do I need before using a reporting type?**\
You must have the required **email templates** created in the email center. Some vendors also require credentials in **System Setup**.\
Example: **Radix Data** and **Inflight Service** will not work until credentials are configured in **System Setup**.

**Should I use Hour or Minutes?**\
Use **Hour** when you want one send per day at a fixed time. Use **Minutes** when you want repeated sends. You cannot set both on the same rule.\
Examples:\\

* **Hour = 09**: send once at 09:00 (per applicable departure offset).\\
* **Minutes = 60**: re-send every 60 minutes (for example, during the last day before departure).
