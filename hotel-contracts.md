# Hotel Contracts

Hotel Contract is used for defining contract between one agency and one hotel.

### Settings

The mandatory fields for creating a new contract are:

* Agency
* Resort&#x20;
* **Hotel**&#x20;
* **Contract Name**
* **Supplier**&#x20;
* **Creditor**&#x20;
* **Date Start**&#x20;
* **Date End**&#x20;
* **Contract Type**&#x20;
* **At least one room type**

Resort dropdown contains all available resorts defined per company.

<figure><img src=".gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After selecting one resort, hotel list is populated.

<figure><img src=".gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You have 2 options:

&#x20;**- choose one existing hotel.** If selected hotel already has one of the following fields filled (Supplier, Creditor, Code), you are not allowed to change them.

&#x20;**- create a new Hotel**

Contract Details:

<figure><img src=".gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* **Name** - represent name of the contract
* **Creditor** - Hotel Contract currency = Creditor's currency
* **Star Date** - start date of the hotel contract
* **Date end** - date when the contract will expire
* **Contract typ**e - type of the contract (Allotment, Guarantee, Allotemnt/Guarantee)
* **Auto Biling**&#x20;
* **Bulk guarantee room -** select this option to creaet Room Cost based on deposit. Room Cost will be ignored
* **Combine EB with SO** - combine Earlybooking with Special Offer

### Room type <a href="#room-type" id="room-type"></a>

You have 3 options to define a room type:

* **Add New Room Type** - create a new base room type per company

<figure><img src=".gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

All fields will be available to fill in. When importing in Tourpaq, a new base room type is created.

* **Import New Room Type in Tourpaq**

<figure><img src=".gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

No. ordinary beds is calculated in this way: Minimum - Max. Extra Adult - Max. Extra Child

* **Add New Room Type From Existing** - choose one of the exiting base room types defined per company

<figure><img src=".gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When you use this option, Room Type Code, Room Type Name, Minimim, Maximum, Max. Adult and Max. Child can not be changed. These were defined in Base Room Type.

* **Maximum beds -** Maximum column from Hotel Contract is calculated in this way: No. ordinary beds + Extra beds + Extra beds child
* **Add New Room Type From Hote**l - choose one of the exiting base room types defined per selected hotel

For each option, you need to fill in Number of unit (Allotment and Guarantee) and Price for period. You can also define a new Period and for each period add as many intervals as you want. Periods and intervals can be deleted.

### Supplements <a href="#supplements" id="supplements"></a>

You can choose from 2 categories:

* **Room Type Supplement**- Double as Single. Each room from "Room Type" can be sold as Single.

<figure><img src=".gitbook/assets/image (11) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Age and Rank are not allowed for selecting.&#x20;

If "Per Pax" is checked, price cost is applied per pax, otherwise is applied per night.

If "%" is checked, room cost represents percent cost from parent base room type.

It is mandatory a mapping between standard room type and shared room type:

<figure><img src=".gitbook/assets/image (12) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Room Code represents room sold as single Room. Room Above represents parent room.

**This works only for one shared room. If more shared rooms are added, the cost will be taken from the first shared room listed**

* **Product Supplement** - Mini All Inclusive, All Inclusive, Ultra All Inclusive, Breakfast, Diner, Half Board. You can select one of these options as Supplement.

<figure><img src=".gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Mandatories fields:

* Age (From - To) Example 12-99
* Rank (From - To) (Example 1-3 From the 1st passenger till the 3rd will receive the supplement). A product should be selected for this category type:

<figure><img src=".gitbook/assets/image (14) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After selecting one category, product list is populated. You can choose from existing one, or you can define a new product. When importing in

* **Over Nights** - This option is used when hotel asks you to pay a supplement for each passenger, but only after a defined number of nights.

<figure><img src=".gitbook/assets/image (15) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Reductions <a href="#reductions" id="reductions"></a>

You can choose from 2 categories:

* **Extra Bed Cost** Infant, Child, Adult Age and Rank are required.
* **Product Supplement** - Mini All Inclusive

<figure><img src=".gitbook/assets/image (17) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Important <a href="#important" id="important"></a>

Product Supplement could be defined as Supplement and also as Reduction. For both situations, prices from selected product will be imported and hotel is added in the Resources tab of the product.

<figure><img src=".gitbook/assets/image (16) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The difference is when we define Product Supplement as Reduction. For each room cost, value of product cost is also defined in "Included Cost".

<figure><img src=".gitbook/assets/image (18) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Extra cost rule <a href="#extra-cost-rule" id="extra-cost-rule"></a>

There are 2 extra cost rules:

* Final cleaning
* Bed Linen/Towels

Both of them cannot be used for the same type of room.

<figure><img src=".gitbook/assets/image (19) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Early Booking Discount <a href="#early-booking-discount" id="early-booking-discount"></a>

You can define Early Booking Discounts

<figure><img src=".gitbook/assets/image (20) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

After importing in Tourpaq the results are:

<figure><img src=".gitbook/assets/image (21) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Payment Plan

The **Payment Plan** section allows users to define multiple payment milestones for a hotel contract. Each payment&#x20;

| Field Name       | Description                                                                                                                                                 |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Deposit Date** | The date when the payment is initially made (input format: DD-MM-YYYY).                                                                                     |
| **Payback Date** | The date when the payment is expected to be returned or reconciled. This is optional and shown as a calendar input.                                         |
| **Tot Amount**   | The total monetary value of the payment. This is input manually or pulled from contract terms.                                                              |
| **Currency**     | The currency of the transaction (e.g., EUR). Currently fixed per contract.                                                                                  |
| **Year**         | Represents the year after which the grouping is done. This is selected from a dropdown list. It is used for grouping the plans in the Hotel Contract export |

This section is crucial for financial tracking, forecasting, and ensuring accurate settlements between the travel agency and the hotel.

<figure><img src=".gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (1) (1) (1).png" alt=""><figcaption><p>Payment Plan Grouping by years</p></figcaption></figure>

### Remarks

This is an optional text and is displayed in Export Contract pdf

<figure><img src=".gitbook/assets/image (23) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (24) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Rules <a href="#rules" id="rules"></a>

* **How to define**&#x20;

You can define as many rules as you want from main Menu: "Hotel -> Hotel Contract Rules"

<figure><img src=".gitbook/assets/image (25) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Facilities <a href="#facilities" id="facilities"></a>

You are allowed to select a single template per contract. Templates are defined per company.

<figure><img src=".gitbook/assets/image (26) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### View selected Rules and Facilities <a href="#view-selected-rules-and-facilities" id="view-selected-rules-and-facilities"></a>

A summary of selected rules and facilities is found on bottom of the page:

<figure><img src=".gitbook/assets/image (27) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (28) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Send Email <a href="#send-email" id="send-email"></a>

You have the possibility to send created contract to supplier and also as many emails address you want. The supplier has the possibility to accept or reject hotel contract.

<figure><img src=".gitbook/assets/image (29) (1) (1).png" alt=""><figcaption></figcaption></figure>

To be able to use this function is required to create an email template for Hotel Contract, otherwise an warning will be displayed.

### Create a new contract from an existing one <a href="#create-a-new-contract-from-an-existing-one" id="create-a-new-contract-from-an-existing-one"></a>

A new contract can be created from an existing one. On the top right side of the screen a new button will be available **Create New**.

<figure><img src=".gitbook/assets/image (30) (1) (1).png" alt=""><figcaption></figcaption></figure>

A pop-up will appear with a dropdown for the year to be inserted and a discount rate box.

The value inserted in the **Discount rate** box is set as percentage (5 will be 5%). If no sign is set for the value inserted in the **Discount rate** box, all values already existing in Tourpaq will be increased with the set percentage. If "-" is set, all values will be decreased by the inserted percentage.

After this a new page will be displayed, where all details inserted in the previous contract are present and the costs have been changed according to the inserted values.

**Important:** The user will have to manually edit the **Start Date** and **Date End** of the contract!

The new contract can be edited according to the new specifications (Eg: new rooms added, new reductions or payment rules).

The new contract need to be saved and imported in order to produce effects in Tourpaq.
