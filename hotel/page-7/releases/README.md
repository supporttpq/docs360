# Releases

In order for the automatic release of hotel rooms, the service needs to rely on hotel release rules that can be set by the company's administrator in Tourpaq Office side of the application. The release rules that can be set are going to depend on a hotel, no rule can be applied to two or more hotels in the same time. Also, they must be able to apply the release rules at a certain provided date or prior to that date with a given amount of days.

There will be two types of release rules that can be set (thus two subtabs to list in the hotel releases tab) by the type of room release that they will provide:

* general release rule: that can release all the rooms of a hotel at a certain date, or with a given number of days before a certain date;
* specificrelease rule: that can release only one type of room at a time, but can do this during a period of days, that can be set along with the rule. This is the automatic equivalent of the previous rule type, only applied to a specific hotel room.

### General release rule <a href="#general-release-rule" id="general-release-rule"></a>

A general hotel room release rule is must contain a release date, a number of days to make the release in advance and an email address (of the hotel supplier) to send the release report email to.

### Specific release rule <a href="#specific-release-rule" id="specific-release-rule"></a>

A specific hotel room release rule should contain a period to function in, period determined by a start date and end date, the specific room to be released, the number of days to make the release in advance and the email address(of the hotel supplier) to send the report to.

Examples:

Assuming that:

* today's date is 15-05-2009;
* Hotel “Grand Palace” has provided Tourpaq with availability of booking three types of rooms: 1S, 2C and 3F during the whole period of 01-04-2009 to 01-09-2009.

Having this scenario in mind, here is how the Hotel Release Service should function for each release rule type.

**General release rule** with start date set to 20-05-2009, number of days to make to release in advance is set to 5, and email address is set to “[admin@grandpalacehotel.com](mailto:admin@grandpalacehotel.com)”.

When the service runs, the above rule should release all the rooms of the hotel (allotment bookings) for today, compute the number of rooms that were released, create a log file for these room releases(1S, 2C, 3F) and send an email to the admin.

**Notes:**

* if the release rule is not supplied with a start date, then the rule should apply each day the service runs, and will release all the rooms of the hotel for a date after 5 days from today.
* if a release rule is not provided with a number of days, then the above logic remains the same, only that it consider the days number to be 0 (zero).

**Specific release rule** with start date set to 01-05-2009, end date set to 01-06-2009, room type 2C, days number set to 3 and email address to “[admin@grandpalacehotel.com](mailto:admin@grandpalacehotel.com)”.

When the service runs, the above rule should release the 2C room type for the 18-05-2009, compute the number of rooms that were released, save a log file for the action and send an email to the hotel supplier.

**Notes:**

* if today's date is 27-05-2009, then the general release rule cannot release any rooms because the date prior with 5 days to 27-05-2009 is not 20-05-2009 as the rule states.
* if today's date is 30-05-2009, then the specific release rule cannot release any rooms because computing 3 days after today, the date is not inside the release rule period.

The hotel supplier can log into a special Tourpaq Office supplier account and manage the rooms that have been set as “available for release”. By managing them it should be understood that he/she can decide if the number of rooms that are available for release will be removed from the Tourpaq Booking System and reused in other ways.

The supplier administration of hotel room releases must provide a filter to search by hotel, room types and time periods.

The result of the hotel supplier's actions may be reviewed by the company administrator in the “Releases log” submenu under Hotel Tourpaq menu. This will also allow the company admin to filter the history of releases made by the following criteria: suppliers, brands, hotels, room types, and periods.

If a release rule is edited, while still in effect, the new rule will start to take effect after the effects of the previous rule.

Example: A release rule of 10 days is changed to 4 days during the season. Since the rule already was in effect, the new rule will start 7 days after the editing, as the effects of the older rule are still there.
