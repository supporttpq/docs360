# Flight Transfer

**Applies to:** Administrator

### Overview

The **Flight Transfer** feature allows administrators to manage passenger transfers between **arrivals** and **resorts**. It helps organize and control how passengers are transported after landing, ensuring smooth logistics.

⚠️ **Important:** This feature requires activation. Please contact **Tourpaq Support** to enable it for your company.

### Purpose

* Streamline passenger transfers from the airport to the resort.
* Centralize transfer management under a **Transport Operator**.
* Improve operational efficiency by using standardized transfer handling.

### Instructions

#### Step 1 – Create a Transport Operator

Before using the Flight Transfer feature, a **Transport Operator** must be created.

1. Navigate to:\
   **Transport → Flight Transfer → Transport Operators**
2. Add a new Transport Operator by filling in the required details.
3. Save the operator.

Once a Transport Operator is defined, you can proceed with configuring and managing passenger transfers.

### Transport Operators <a href="#transport-operators" id="transport-operators"></a>

A Transport Operator provides means of transport from the arrival place to the resort and viceversa.

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Fields for creating a new Transport Operator:

* Name - Name of the operator
* Address - Address of the operator
* Phone - Phone of the operator
* Email - email of the operator
* Airports - airports assigned to this operator

After this, in the **Bus Catalogue,** you can define the means of transport at the disposal of the operator. They can be cars, vans, buses, etc.

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Routes <a href="#routes" id="routes"></a>

Routes are a combination of an arrival and the resorts connected to it set in the required order. Every entity set in there is a checkpoint where **Stops** are made by the transport vehicle to load or unload passengers.

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

<figure><img src="../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Route names and codes are created by adding the names and codes of the **Arrivals** and **Resorts** in the order they have been set on the route. The flow for creating a route is the following:

* user decides if the route starts with an airport or a resort by selecting from the drop-down “Select Airport” or “Select Resort”. This will enable the next drop-down dedicated to a resort or airport from where the user can select the entity;
* after selection of a resort/airport, the button “Add to Route” will become active, and the user can add the selected entity to the route;
* after “Add to Route” is clicked, at “Route” region below it will be added the first component of the route. “Add to Route” button and Airports/Resorts drop-downs become inactive;
* next, the user can choose to select a new resort and add it to the route
* route should have a minimum two components so it should not be possible to create a route with only one Airport selected, for instance;
* route can be in different configurations and can have more than one resort but only one airport.

### Stops <a href="#stops" id="stops"></a>

Stops are the places where passengers are loaded or unloaded on the transport.

They are defined on a resort basis. Each **Stop** can have one or more hotels assigned to it based on the hotels from the resort.

Likewise, a **Resort** can have more than 1 **Stop**

<figure><img src="../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

It is recommended that if you have more than 1 **Stop** per resort, to give them different names to differentiate them.

### Route prices <a href="#route-prices" id="route-prices"></a>

This is the amount the company pays for the services of the transport operator.

They can be defined per Agency, Operator, Bus and Route.

<figure><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Flight Transfers <a href="#flight-transfers" id="flight-transfers"></a>

This part handles the planning for each bus in particular.

* Airport - the Arrival for the planning
* Departure Date: - date for the planning
* Operator - Transport Operator assigned for the planning
* Bus Type - Bus Type assigned for the planning
* Route - Route assigned to the planning
* Driver Name - (optional - if you want to know the driver name)
* Guide Name - (optional - if you want to assign a guide to the bus)
* Guides Out - number of guides that are on the transfer from airport to resort (number of guides is not included in the number of passengers)
* Guides Home - number of guides that are on the transfer from resort to airport
* Max Seats - number of seats available for the bus
* Bus Number - the number of the bus
* Resort H Time - is the departure time of the bus from Resort (optional - can be left as default and will take the first stop time value from the list of stop times for homebound).
* Time Airport - is the time when the flight transfer bus arrives in the airport, it needs to be filled manually
* Resort O Time - is the arrival time of the bus back at the resort(optional - can be left as default and will take the last stop time value from the list of stop times for outbound)
* Confirmed- checkbox for confirming the transfer bus and will be shown on the OK column in the Flight Transfer Buses page view.

When creating a new plan, the default option is the one selected, but it can be changed in the Airport drop-down.

When an Airport is selected, the system will automatically load the first **Transport Operator**, first **Bus type,,** and first **Route** created in the system by default, along with the **Max Seats**.

After the flight transfer bus has been created, it can be expanded from the blue arrow at the front of the line. From there you can plan the route of the bus in detail and manage the passengers that are loaded and unloaded into it along the way.
