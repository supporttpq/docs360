# Stop Sales

### Definition <a href="#definition" id="definition"></a>

A supplier can remove a hotel room from selling by creating a stop sale for that room. He can do that by going to the Stop sale page and fill the filters for that room and the period. The stop sale will run for each date and reduce the number of rooms available.

<figure><img src=".gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

If the guarantied rooms is filled and is bigger then the booked rooms number, the available rooms number is reduced to the guarantied rooms number. If the guarantied rooms is not filled, or the booked rooms number is bigger, the available rooms number is reduced to the booked rooms number.

### **Scenarious**

| Available rooms before stop sale | Guarantied rooms number | Booked rooms Number | Available rooms after stop sale |
| -------------------------------- | ----------------------- | ------------------- | ------------------------------- |
| 10                               | 5                       | 4                   | 5                               |
| 10                               | 5                       | 6                   | 6                               |
| 10                               | -                       | 6                   | 6                               |
| 10                               | -                       | 10                  | 10                              |

After the 'Stop Sale' is created, the supplier will be redirected automaticaly to the 'Hotel Allotment' page, so he can see the changes that have been made. Here the filter will be autofilled.

<figure><img src=".gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

A Stop Sale can be made for all the rooms of the hotel, but the system will treat and save every room as a separate Stop Sales.

### **Stop Sale Service**

There is a new service that verify all stop sales created, that includes future dates, and check if a room( or more) has been canceled. If this is the case, it reduced the rooms available, after the rules displayed earlier. To filter out a specific stop sale from the service, go to the "Hotel" menu, Stop sales page and click "Disable" to that stop sale.

### **Stop Sale Log**

As an administrator, you can see the Stop Sales changes and logs from the Release/Stop sale logs, from the hotel tab. The last column specify if the log has been made from the release, from the stop sale or from the stop sale service.

<figure><img src=".gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

### **Stop Sale on Notification**

There is a new tab in the Notification, where are listed the new stop sales created.

<figure><img src=".gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

In this tab you can see all the stop sales created. For each one you have the option to **View Details**.

<figure><img src=".gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

If you chose the **View Details** for one of those stop sales, the system will redirect you to the log page, fill the filtes with data from the stop sale and display the changes.

### **Stop sales in Admin**

<figure><img src=".gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

In the "Stop sales" page from the Hotel menu, it can be seen all the Stop Sales including the ignored ones. The Ignored "Stop sales" can be seen with a red background. Here you can disable/enable a stops sale. If you disable a stop sale, the Stop sale service filters out it so that the allotments of the Hotel can be changed.

### **Stop sales in Supplier**

<figure><img src=".gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

A Supplier, if it has the "Allow to make stop sale" right activated, he can see his stop sales in the "Agent" menu, "Stop sales list" page. A Supplier can only Disable/Enable a service.

### **Stop Sale Mail**

After a new Stop Sale is made, a mail is send to the company, with the stop sale filters. For this functionality to be available, there are two things that must be setted:

1. In **system setup**, each company must fill the **Email address for stop sale**.

<figure><img src=".gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

2. Each agency must create the **email template** for this, from E-mail center.

<figure><img src=".gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

### **Stop Sale Room Reservation**

We'll add a stop sale option per hotel that will:

* Not allow either the customer on web booking or the salesperson in Office to make room selection during the stop sale hours if they are not having anything already chosen.
* Not allow either the customer on web booking or the salesperson in Office to make changes of the room selection during the stop sale hours if they have already the selection made.

<figure><img src=".gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>
