# Transfer listing

Available to Admin user type.

To use this feature, please contact Tourpaq Support.

This feature enables the managing of passenger transfer between arrivals and resort.

The first step in using this feature is to create a Transport Operator. This is done in **Transport/Flight transfer/Transport Operators**

A new Transport Operator is defined with the **New Transport Operator** button on the right side of the screen.

### Transport Operators​ <a href="#transport-operators" id="transport-operators"></a>

A Transport Operator provides means of transport from the arrival place to the resort and viceversa.

Fields for creating a new Transport Operator:

* Name - Name of the operator
* Address - Adress of the operator
* Phone - Phone of the operator
* Email - email of the operator
* Airports - airports assigned to this operator

<figure><img src="../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After this, in the **Bus Catalogue** you can define the means of transport at the disposal of the operator. They can be cars, vans, buses etc.

<figure><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Routes​ <a href="#routes" id="routes"></a>

Routes are a combination of arrivals and resorts set in the required order. Every entity set in there is a checkpoint where **Stops** are made by the transport vehicle to load or unload passengers.

There is order set as this decision is left to the users needs.

A route can be made from:

* Arrival to Resorts
* Resort to Resort
* Resort to Arrival
* Arrival to Resorts to Arrival
* Resorts to Arrival to Resorts
* any combination that meets the needs of the users

When selecting the **Arrival**, you are given the option to choose between all **Arrivals** available to the Company.

When selecting the **Resort**, you are given the option to choose between all **Resorts** available to the Company.

You can assign more than one **Transport operator** per route.

<figure><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Route names and codes are created by adding the names and codes of the **Arrivals** and **Resorts** in the order they have been set on the route.

<figure><img src="../.gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Stops​ <a href="#stops" id="stops"></a>

Stops are the places where passengers are loaded or unloaded on the transport.

They are defined on a resort basis. Each **Stop** can have one or more hotels assigned to it based on the hotels from the resort.

Likewise, a **Resort** can have more than 1 **Stop**

<figure><img src="../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When adding a hotel, you have to also select the direction. This can be

* Outbound
* Homebound
* Both

<figure><img src="../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

It is recommended if you have more than 1 **Stop** per resort to give them different names in order to differentiate them.

<figure><img src="../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Route prices​ <a href="#route-prices" id="route-prices"></a>

This is the amount the company pays for the services of the transport operator.

They can be defined per Agency, Operator, Bus and Route.

<figure><img src="../.gitbook/assets/image (15) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Flight Transfers​ <a href="#flight-transfers" id="flight-transfers"></a>

This part handles the planning for each bus in particular.

<figure><img src="../.gitbook/assets/image (16) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Airport - the Arrival for the planning
* Departure Date: - date for the planning
* Operator - Transport Operator assigned for the planning
* Bus Type - Bus Type assigned for the planning
* Route - Route assigned to the planning
* Driver Name - (optional - if you want to know the driver name)
* Guide Name - (optional - if you want to assign a guide to the bus)
* Guides Out:
* Guides Home:
* Max Seats - number of seats available for the bus
* Bus Number - the number of the bus
* Resort H Time - is the departure time of the bus from Resort (optional - can be left as default and will take first stop time value from the list of stop times for homebound.)
* Time Airport - is the time when the flight transfer bus arrives in the airport, it needs to be filled manually
* Resort O Time - is the arrival time of the bus back at the resort(optional - can be left as default and will take the last stop time value from the list of stop times for outbound)
* Confirmed- checkbox for confirming the transfer bus and will be shown on the OK column in the Flight Transfer Buses page view.

When creating a new plan, the default option is the one selected, but it can be changed in the Airport drop down.

When an Airport is selected, the system will automatically load the first **Transport Operator**, first **Bus type** and first **Route** created in the system by default along with the **Max Seats**.

After the plan has been created, it can be expanded from the blue arrow at the front of the line. From there you can plan the route of the bus in detail and manage the passengers that are loaded and unloaded into it along the way.

<figure><img src="../.gitbook/assets/image (17) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The feature was developed with the resort as the point of departure. As such the first column is the **Homebound** column, used for planning the route from the resorts to the airport. The **Outbound** column is used to plan the route from the airport to the resorts.

The columns contain the resorts define on the route, flight numbers of the transports that are connected to the resorts, the time transports arrive at/leave from the airport, the number of passengers that have **Booked transfer extras** from each resort. The user can also insert how many passengers from the flight will use that bus and plan the rest for another bus with the help of **ALLOC H** and **ALLOC O** columns.

After all these details have been inserted, the schedule fro stops can be made, meaning the time the buss bill arrive at each of the stops along the way. This is done with the help of the **Stop Times** buttons for each column.

<figure><img src="../.gitbook/assets/image (19) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Also, passengers can be assigned to the bus with the **Seating** button.

<figure><img src="../.gitbook/assets/image (20) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Once a passenger has been checked, his name will disappear from the list showing that he has been seated in the bus.
