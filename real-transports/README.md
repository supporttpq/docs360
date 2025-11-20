# Real Transports

Real Transports can be found in **Transports/Real Transports**. They are a special case and as such are somewhat difficult to create.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (3).png" alt=""><figcaption></figcaption></figure>

1. Just like any transport, the user has to write it's code and select the departure and arrival. Unlike any transport, it is imperative to select the **Reporting Type**. After the actions have been completed, the user can click the **Save** button and proceed to the next step.

<figure><img src="../.gitbook/assets/image (7) (1) (2).png" alt=""><figcaption></figcaption></figure>

2. The next step is to configure the transport's timetable. This process has the same steps as a normal transport, as in filling star and end dates, departure and arrival times, but now is mandatory to fill the **Flight No.** case. To complete the action the user has to press **Insert**.

<figure><img src="../.gitbook/assets/image (8) (1) (3).png" alt=""><figcaption></figcaption></figure>

3. The last step in creating a real transport is setting up it's allotments from **All.Manager**. The user will have to fill in the start and end dates, the number of days between flights, the number of seats and guaranteed seat, as well as the seat price. To complete this stage, the user has to press **Create** and after that **Generate**.

<figure><img src="../.gitbook/assets/image (10) (1) (3).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

4. The only problem with a real transport is the fact that the user has to create one for outbound and one for homebound. So in the end the user wil have created 2 Real Transports for use on one Normal Transport.

## Real Transport <a href="#real-transport" id="real-transport"></a>

To properly use a real transport, the user must have a normal transport linked to it. A normal transport cannot be edited for this purpose. A new transport has to be created specifically for that purpose.

**These settings also apply to GDS.**

1. The user creates the transport as usual, with a significant change. He will check the case for **Dynamic Itineraries**.

<figure><img src="../.gitbook/assets/image (12) (2).png" alt=""><figcaption></figcaption></figure>

2. For this step, the user must create an interval and assign the transport to a brand.
3. This step creates the link between a normal and real transports. For this, the user has to go to **Legs** and click on **New Leg** button.

<figure><img src="../.gitbook/assets/image (13) (2).png" alt=""><figcaption></figcaption></figure>

4. Next the user has to set the departure and arrival, as well as the days between flights and click **Save**

<figure><img src="../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

This action has to be repeated but with the departure and arrival places inversed. So that in the end it will look like this.

<figure><img src="../.gitbook/assets/image (14) (2).png" alt=""><figcaption></figcaption></figure>

5. Another thing the user has to do is check the **OwnDatabase** and **OneWay** boxes and then click **Save**.

<figure><img src="../.gitbook/assets/image (15) (2).png" alt=""><figcaption></figcaption></figure>

6. Last thing to do in this section is to setup the flights. Press the **Configure** button, select the departure date and then press **Test Search**

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

The **Test Search** will display all available real transports flights. The user can narrow them down if they are too many, using the filters.&#x20;

<figure><img src="../.gitbook/assets/image (16) (3).png" alt=""><figcaption></figcaption></figure>

After the user has found the real transport it wanted, the settings can be saved. The same thing must be done for the second leg.

And lastly, after all these have been made, the user has to press **Update Flight Data** for both legs.

<figure><img src="../.gitbook/assets/image (17) (2).png" alt=""><figcaption></figcaption></figure>

7. From this point on everything is done like in the case of a normal transport. The user can proceed to create a fix quota, save the transport, reset the cache and start booking.
