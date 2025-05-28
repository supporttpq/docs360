# Extra Category Reporting

A list of passengers that purchased extras from a specific extras category are sent for ex. every day 4 days before arriving home from the trip.

#### Configuration[​](https://docs.tourpaq.com/docs/documentation/extra-category-reporting#configuration) <a href="#configuration" id="configuration"></a>

In order for the Extras Reporting to be up and running for your company check with the \[\[Web Master]] to see it the windows service scheduler is running for your company, specifically //Extras Category Reporting Service//.

**Email Center**[**​**](https://docs.tourpaq.com/docs/documentation/extra-category-reporting#email-center)

The email that will be sent by the service can be configured like this:

1. Navigate to **Setup** -> **E-mail center**
2. First Select the brand from upper right corner
3. Choose **Extra Category Reporting** in **Email type** drop down
4. Fill the form with the required data

Note: If the email is not Activate the reporting will not be sent.

Optional: You can add a confirmation link in the email.

[http://emailtracking.tourpaq.com/EmailConfirmation.aspx?messageID=\[MessageID](http://emailtracking.tourpaq.com/EmailConfirmation.aspx?messageID=%5BMessageID)]

**Setup Scheduler**[**​**](https://docs.tourpaq.com/docs/documentation/extra-category-reporting#setup-scheduler)

To add a new scheduler

1. Navigate to **Extras Setup** -> **Extras Categories** -> **Edit**
2. Select the Communication tab
3. When click Create a new record will be added in the row
4. In Figure 1 you can see a sample. If this rule is set the service will try to send arriving a list every day at 10:30 with passengers that has purchased an extras within this category and are arrive home 4 days after the list has been sent.

Note: The service will produce an PDF file.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**E-ticket Overview**[**​**](https://docs.tourpaq.com/docs/documentation/extra-category-reporting#e-ticket-overview)

The emails that are sent are stored in e-ticket overview. To view the emails

1. Navigate to **Tickets** -> **E-ticket overview**
2. Select the period within you like to search
3. By clicking //Show default communication email types// you will see int the **Email type** drop down the types for communication
4. Select in the **Email type** drop down **Extras Category Reporting**

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
