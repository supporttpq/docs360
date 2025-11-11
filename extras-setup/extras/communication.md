# Communication

**Overview**\
The _Extras Communication_ feature is used to automatically send lists to suppliers and hotels with details about the extra products booked by guests. These lists help external partners prepare and manage guest services efficiently before arrival.

**Purpose**\
This functionality ensures that suppliers and hotels receive up-to-date booking information according to a defined schedule. It automates repetitive communication tasks, reduces manual effort, and helps prevent missing or outdated information.

<figure><img src="../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**How to Use**

1. **Access the Setup**\
   Navigate to **Extras → Communication** in Tourpaq Office.
2. **Configure Communication Rules and Filters**\
   Define how and when the communication lists should be generated and sent:
   * **Interval** – Determines how often the lists are sent:
     * **Daily** – Lists are sent daily for departures occurring within X days prior t&#x6F;_&#x58;_ days before the send date.\
       &#xNAN;_&#x45;xample:_ If **Days after = 3**, the list includes departures from today and the next two days.
     * **Weekly** – Lists are sent once a week on a selected day (e.g., Monday) for departures happening within _X_ days.\
       &#xNAN;_&#x45;xample:_ If **Weekday = Monday** and **Days after = 2**, the list sent every Monday includes departures for Monday and Tuesday.
     * **Monthly** – Lists are sent on a selected day of the month (1–31) for departures happening within _X_ days.\
       &#xNAN;_&#x45;xample:_ If **Month day = 1** and **Days after = 3**, the list sent on the 1st includes departures for the 1st–3rd.
     * **Yearly** – Lists are sent on a specific calendar date for departures happening within _X_ days.\
       &#xNAN;_&#x45;xample:_ If **Date = 01.04.2025** and **Days after = 1**, the list includes departures for April 1–2, 2025.
3. **Set Additional Parameters**
   * **Days after** – Defines the departure range (how many days ahead the list should cover).
   * **Hour** – The exact hour (in Denmark time) when the list is automatically sent.
   * **E-mail** – The recipient address where the list should be delivered.
   * **Reporting** – Selects the type of list (e.g., hotel, supplier, or extras overview).
   * **Empty list** – If checked, the system will send an empty list even when there are no bookings.
   * **Communication** – Displays a log of the lists that have been sent.
4. **Save and Monitor**\
   Once the communication rule is set and saved, the system will automatically generate and send the lists according to the defined schedule. Sent communications can be reviewed in the **Communication** log.
