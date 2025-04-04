# Payment rate rules

## Payment rate rules

* Deposit value - amount of the first payment per passenger
* Deposit percentage - When is set, deposit is calculated based on percentage from base price(without other extras/supplement). Payment simulation will use deposit value!
* Second payment value
* Deposit due - number of days after booking the deposit must be paid
* Second payment due - number of days before departure the second payment must be paid
* Last payment due - number of days before departure the last payment must be paid

### Exception rules: <a href="#exception-rules" id="exception-rules"></a>

* If second payment due date / rest of payment due date < booking date + deposit due, then second payment due date / rest of payment due date = booking date + 2, except if departure date < booking date + 14
* If departure date < booking date + 14, then second payment due date / rest of payment due date = booking date + 1, except if departure date < booking date + 3
* If departure date < booking date + 3, then second payment due date / rest of payment due date = booking date
*
  * If second payment due date < deposit due date, then second payment due date = deposit due date
  * If rest of payment due date < second payment due date, then rest of payment due date = second payment due date

> 📝 **Note:** the deposit value will be higher since the Cancellation Insurance will also be included, and certain products may be set to be paid within the deposit payment.

**Supporting payment rules in the past (specific date intervals)**

Tourpaq supports having a company/system "history" for deposit values in different booking date intervals/seasons. When updating a booking within a specific interval (changing the passenger structure, updating products, etc) the system will recalculate the payment rates/deposit according to the corresponding deposit default value (and other rule attributes).

* Current default deposit per passenger value (and due dates) will continue to be used from field #1.
* We added a new field named "Deposit percentage", When is set, deposit is calculated based on percentage from base price(without other extras/supplement).Payment simulation will use deposit value!
*   We have a setting tab named "Deposit rules" where previous deposit default values can be entered.

    * **Please note!** If we enter a rule today, it will automatically set the rule with today's date.

    <figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption><p>#1 / #2</p></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>
* The behavior it produces is that all the bookings made up until **today INCLUDED** will use the deposit value (and due dates) in the relevant rule from #3.
* Only starting from **tomorrow**, all bookings will use the default deposit value in field #1.
* We can have multiple rules in the list from #2 and #3. They will affect bookings made within the date intervals determined by several deposit rules, like in example #3.

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption><p>#3</p></figcaption></figure>

📝 **Note:**

* We now have a "history" for the System/Company default deposit values.

This deposit value can be **overwritten by**:

* Agency specific deposit rules:

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

* Each transport can use custom payment rules that **overwrite both the company setting and the agency** setting.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

> 📝 **Note:** We do not currently have support for previous deposit values from rules set under agency and transport
