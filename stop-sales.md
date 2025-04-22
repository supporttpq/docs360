# Stop Sales

### Definition <a href="#definition" id="definition"></a>

A supplier can remove a hotel room from selling by creating a stop sale for that room. He can do that by going to the Stop Sale page and filling in the filters for that room and the period. The stop sale will run for each date and reduce the number of rooms available.

<figure><img src=".gitbook/assets/image (65) (1).png" alt=""><figcaption></figcaption></figure>

If the guaranteed rooms are filled and are more than the booked rooms number, the available rooms number is reduced to the guaranteed rooms number. If the guaranteed rooms are not filled or the booked rooms number is bigger, the available rooms number is reduced to the booked rooms number.

### **Scenarios**

| Available rooms before stop sale | Guarantied rooms number | Booked rooms Number | Available rooms after stop sale |
| -------------------------------- | ----------------------- | ------------------- | ------------------------------- |
| 10                               | 5                       | 4                   | 5                               |
| 10                               | 5                       | 6                   | 6                               |
| 10                               | -                       | 6                   | 6                               |
| 10                               | -                       | 10                  | 10                              |

After the 'Stop Sale' is created, the supplier will be redirected automatically to the 'Hotel Allotment' page so he can see the changes that have been made. Here the filter will be autofilled.

<figure><img src=".gitbook/assets/image (66) (1).png" alt=""><figcaption></figcaption></figure>

A stop sale can be made for all the rooms of the hotel, but the system will treat and save every room as a separate stop sale.

### **Stop Sale Service**

There is a new service that verifies all stop sales created, which includes future dates, and checks if a room (or more) has been canceled. If this is the case, it reduced the rooms available after the rules displayed earlier. To filter out a specific stop sale from the service, go to the "Hotel" menu, Stop Sales page, and click "Disable" for that stop sale.

### **Stop Sale Log**

As an administrator, you can see the stop sales changes and logs from the release/stop sale logs from the hotel tab. The last column specifies if the log has been made from the release, from the stop sale, or from the stop sale service.

<figure><img src=".gitbook/assets/image (67) (1).png" alt=""><figcaption></figcaption></figure>

### **Stop Sale on Notification**

There is a new tab in the notification where the new stop sales created are listed.

<figure><img src=".gitbook/assets/image (68) (1).png" alt=""><figcaption></figcaption></figure>

In this tab you can see all the stop sales created. For each one, you have the option to **view details**.

<figure><img src=".gitbook/assets/image (69) (1).png" alt=""><figcaption></figcaption></figure>

If you choose the **View Details** for one of those stop sales, the system will redirect you to the log page, fill the filters with data from the stop sale, and display the changes.

### **Stop sales in Admin**

<figure><img src=".gitbook/assets/image (70) (1).png" alt=""><figcaption></figcaption></figure>

seen that In the "Stop Sale" page from the hotel menu, it can be seen that all the stop sales, including the ignored ones, can be seen. The ignored "stop sales" can be seen with a red background. Here you can disable/enable a stop sale. If you disable a stop sale, the stop sale service filters it out so that the allotments of the hotel can be changed.

### **Stop sales in Supplier**

<figure><img src=".gitbook/assets/image (71) (1).png" alt=""><figcaption></figcaption></figure>

A supplier, if it has the "Allow to make stop sale" right activated, can see his stop sales in the "Agent" menu, "Stop sales list" page. A supplier can only disable/enable a service.

### **Stop Sale Mail**

After a new stop sale is made, an email is sent to the company with the stop sale filters. For this functionality to be available, there are two things that must be set:

1. In **system setup**, each company must fill in the **email address for stop sale**.

<figure><img src=".gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>

2. Each agency must create the **email template** for this from the email center.

<figure><img src=".gitbook/assets/image (73) (1).png" alt=""><figcaption></figcaption></figure>

### **Stop Sale Room Reservation**

We'll add a stop sale option per hotel that will

* Do not allow either the customer on web booking or the salesperson in the office to make room selection during the stop sale hours if they do not already have anything chosen.
* Do not allow either the customer on web booking or the salesperson in the office to make changes to the room selection during the stop sale hours if they have already made the selection.

<figure><img src=".gitbook/assets/image (74) (1).png" alt=""><figcaption></figcaption></figure>
