# Export

It is needed that Tourpaq Office implements general exporting features of the application activity during a given period of time and customized by transport, country, resort or hotel criteria. The export should be produced in the XML format to allow further manipulation of the data in other client systems.

Based on various export interests, the development should implement multiple export templates. Each of these templates will be structured and will contain relevant data for different active players in the system: hotel suppliers will be interested in a room and hotel export list, guides will be interested in an export that provides guide relevant data etc. Considering this it should be possible to export:

* hotel list export: it will contain a report of the bookings made in a given period per each hotel of the chosen agency, grouped by stay intervals and room types,
* rooming list: similar to the hotel list export only detailing each passenger in a booking,
* guide list: will detail passenger detail, contact data and comments etc.,
* passengers list: list passenger data according to stay period and then grouped by hotel,
* canceled booking list: listing all the canceled bookings (that do not appear in all the above exports) grouped by hotels first, stay periods and then room types.
* The filters that must be available for use when producing an export file will be:
* company's brand/agency to export data for,
* an interval period of arrival dates: arrival date from and arrival date to (filters bookings with arrival at destination somewhere inside this time frame),
* a booking interval: booking date from and booking date to (filters the bookings that were made during this interval of time),
* the report type that is going to be generated (see above for details)
* transport filters that will allow selecting multiple options and filter the bookings by the transport they use,
* country destination of the holiday package that was booked – multiple choice selector,
* multiple resort filter to include in the report only the bookings that have been made to the selected resorts,
* hotel selector for the filtering of the bookings that hosted passenger to certain hotels,
* (optional) available only for the canceled booking export template – it will limit the returned bookings to be canceled somewhere in the period from the set date up until today.

The data structure of a Hotel List export file should be a repetition of hotel blocks listing data on the next columns:

* holiday interval period,
* room code,
* room name,
* room units that have been booked,
* passengers contained in the booking,
* booking number and
* booking data.

The header of the repeatable hotel block must contain information regarding the agency that the export was made for, the email address of the hotel supplier representative, creation date, hotel name and code and the chosen export period. There is also needed to include a footer passengers total of the hotel block. These header and footer are requested to appear on most of the repeating blocks of the export templates in Tourpaq Office.

All of the export templates will basically be focused on the booking or passenger entities and produce groupings of them per rooms, holiday periods, hotels etc. The above groupings of the bookings that fit in the used filtering criteria are (in the top-down priority):

* grouping the bookings made by hotels,
* per each hotel group, it will split the selected period into complete holiday stays (ex: 7 days, 14 days or other system period),
* per each holiday period it will group the bookings by room type,
* per each room type it will list all the bookings made, the number of passengers in each booking number and date it was placed.

The data structure of the Rooming List export is similar to the one of Hotel List export, only that adds to each booking the notion of passenger entity, not only number. So it will list a column for each of the name and surname of each passenger, gender, age, booking number and date, flight out and returning flight numbers. It should also list a number of columns that are differing from one company to another according to system settings. One of them could list extra pension name and code, extra car name and code, tours name and code while other could list extra V.I.P. name and package code, extra party name and package code and may list common columns, but still by settings made in the system, for example the tours name and code. See data structure of the export template above.

The guide list export is suitable for guide interests and groups data the same mode, firstly by hotels, then by stay period, and room types. The extra data here should be the details of chosen supplements, status of transfer option during the trip, travel insurance code and possible transport comments. Also important data for guides would be customer email address and telephone number, as well as comments made by the client regarding the hotel accommodation or room positioning preferences. There are also present the optional columns mentioned above, per each company. Here is an example of the columns that need to be included in the export, followed by a worksheet example of the repetitive basic structure:

* stay period / transport interval,
* one column for each of room code and name,
* room units that have been booked,
* passengers included in the booking,
* each column for booking number and date,
* flight number out/return,
* the room number inside the booking (the way the passengers will be accommodate in the possible multiple rooms of a booking),
* passenger's age,
* passenger's gender,
* passenger's first name,
* last name,
* optional changeable from company to company columns (example: extra pension code, extra pension name, extra car code, extra car name, tours code, tours name),
* supplement code,
* transfer status inside the booking,
* presence of travel insurance,
* comments related to the transport.

Another export template is the passenger list one. The passenger list export template should be a bit different than the previous ones by the fact that it is primarily focused on listing the passengers of the selected period of time and group them by stay periods. There will not be a repetitive block used here and the passengers and bookings groupings will be made by transport intervals first and then by hotel. This should be useful to manage data from the stay period's point of view. The header of the export will include values of the used filters to produce the export: chosen country resort and flight.

Each of the transport period will then be listing the passengers per each hotel that have received tourists then.

The export columns should be the following:

* stay period / transport interval,
* hotel code and hotel name,
* booking number and date,
* flight number out/return,
* passenger gender, age, first and last name,
* if the booking contains transfer or not.

This export must display at the end of it various useful total statistics:

* a total of passengers per transport, with detailing on the age group components of the transport: how many adults, children or infants,
* a total of passengers that have been accommodated to each hotel,
* a total of passengers grouped by transfer presence in their package or not.

Below is an example of the needed structure for passenger list export as seen in a worksheet document.

A very useful export template will be the canceled bookings one because in all the above export templates no canceled booking was considered, only completed ones. It will respect the most common standards of the other templates and it will not include passenger details. The booking groupings will be done in the first place by hotels, then by stay periods and finally by room types. It is needed to display the following information as columns:

* stay period interval,
* room code,
* room name,
* booked room unit number,
* passengers number in booking package,
* booking number,
* booking name and
* cancellation date of the booking.

**Bookings Change List**

This section is part of Exports, where a new option should appear in Report Type drop-down list. The option should be named Change List. By choosing this type of report, together with the others filters, the application needs to output an Excel XML Document File providing information for hotel suppliers.

The hotel suppliers should be able to see, starting with a chosen date (a new filter is introduced: Changes from) the newly created bookings, the canceled bookings and what changes has been made to all the bookings of a hotel until the current date.

**New bookings**

The export will output all bookings that have been made since Changes from. We consider as new bookings not only those that have been created before the selected date, but also those that before this date were in ERROR status and their status became OK in the given interval.

**Canceled bookings**

The canceled bookings should be reported also. Similar to the new bookings, the export should not consider a booking as canceled only if it is canceled. If a booking has been made before the chosen date, its status was OK, but in the export date is ERROR, then it is considered as canceled.

If a booking is created after the chosen date, but is later canceled (or ERROR status), it should not be included in report since between the export start date and today(date of export) nothing new happened that changes hotel allotments.

**Changed bookings**

The export will output all changes made for a booking starting with a given date. These changes should be taken from the booking history module. In order to make this happen, it is required to make sure that all types of changes are tracked and saved in database.

It will be needed to take only those changes for the bookings that are not newly created and not canceled. Also, development logic should not take into consideration the changes that are saved for a booking while its version is -1 (the booking is not fully completed, status is ERROR).

The Excel sheet is structured as follows:

* All the changes should be grouped first by hotel
* Each hotel’s changes are grouped also by their period (arrival and return date)
* Each period’s changes are grouped by each booking made in the interval. Here we should display the booking date and number for each change (Bookingno and Bookingdate)
* For each change we should display the date of change (Changedate), the type of change (Change of what). Also, Excel export should display the old changed field value (From) and the new value (To). For both values (From and To) we should display the Code and Name of the changed element (if possible).

This is a list of the changes that should be reported in the export:

* Hotel – this change should be displayed for both hotels; also, the room change (the rooms of the old hotel will be removed from booking) should be displayed only for the old hotel;
* Rooms – the number and type of rooms that are booked or removed from booking (e.g. Rooms(+1), or Rooms(-2));
* Period – if the departure date or the period (1, 2, 3, 4) is changed, this change should be reported. If the departure date is changed, this implies that the arrival at hotel is also changed; also, if the period (1, 2, 3, 4) is changed, this implies that the return date is changed. Here we should display also the old period (From period, both the old arrival and return date).

The following changes are to be recorded at passenger level. Each row of change will be followed by passenger’s gender, age, first name and last name, in order to easily see for which passenger the change was made.

* passenger added/canceled/change of gender, age, first name, last name;
* transfer added or removed;
* discount or supplement added or removed;
* extras products to the base package (car, pension, catering, vip, party package) added or removed.
