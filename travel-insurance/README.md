# Travel Insurance

Applies for Administrator

The system must provide travel insurances for the passengers that make bookings. A passenger can opt for a travel insurance provided by the system, or he can use his own travel insurance and give the necessary information (like company insurance and policy number).

The inserted travel insurances will belong to a precise travel insurance provider. Travel insurance automate reporting will daily select these insurances and send them to the insurances providers (for a better understanding of how the process work, please refer to Travel insurance automate reporting specification)

The following is an extract from the information that must be available for a travel insurance asset:

* Travel insurance name
* Travel insurance code
* Product code\* Used to map the travel insurance asset inserted in the system with the correspondent product exposed by the travel insurance provider
* Maximum days number cover
* Description
* Europæiske extensions
  * These extensions are filled only for the travel insurances that correspond to products provided by Europæiske
  * The extensions are: 5 codes(1,2,3, 4 and 5) and trip type
* Gouda extensions:
  * These extensions are filled in only for the travel insurances that correspond to products provided by Gouda
  * The extensions are:
    * Cover: indicates what the insurance applies to—either a single person or a group. Values that indicate a group are 6, 10, and 18. These values are not sent directly to Gouda.
    * Tax: the fee charged by Gouda for their services, defaults to 1.1% of the insurance price.
    * Optionals:
      * 1 = Personal Property
      * 2 = Ski
      * 3 = Excess
      * 4 = Accident
      * 5 = Accident + Personal Property
  * Product version
  * 1 year available
* Countries
* Specifies the country/countries covered by the travel insurance
* Prices for different periods of time The prices must be inserted taking into account the insurance area and age.
  * Adult Basic price for Scandinavia
  * Adult price per day for Scandinavia
  * Child basic price for Scandinavia
  * Child price per day for Scandinavia
  * Adult Basic price for Europe
  * Adult price per day for Europe
  * Child basic price for Europe
  * Child price per day for Europe
  * Adult Basic price for World
  * Adult price per day for World
  * Child basic price for World
  * Child price per day for World
* Photos

Example:

| Travel insurance name               | Travel insurance code | Product code | Max days cover number | Description | Countries |
| ----------------------------------- | --------------------- | ------------ | --------------------- | ----------- | --------- |
| Årsrejsef.EU(Husst.)m.gratis  Total | ÅEH                   | AREU         | 365                   | Bulgary     | Kreta     |

Let’s suppose that this travel insurance corresponds to a product provided by Gouda, so Gouda extensions should be filled in:

| Cover | Optionals | Product version |
| ----- | --------- | --------------- |
| 6     | 0         | 4.0             |

The correspondent prices:

| Bkg start date | Bkg end date | Sc. basic price adult | Sc. basid price child | Sc. adult price per day | Sc. child price per day | Eur. basic price adult | Eur. basic price child | Eur. adult price per day | Eur. child price per day | W. basic price adult | W. basic price child | W. adult price per day | W. child price per day |
| -------------- | ------------ | --------------------- | --------------------- | ----------------------- | ----------------------- | ---------------------- | ---------------------- | ------------------------ | ------------------------ | -------------------- | -------------------- | ---------------------- | ---------------------- |
| 01-12-2009     | 01-12-2011   | 0                     | 0                     | 0                       | 0                       | 350                    | 0                      | 350                      | 0                        | 0                    | 0                    | 0                      | 0                      |

The total price for an insurance will be calculated like this:

Total price = Basic price + trip length \* price per day

As it has been mentioned before, the passenger can opt to use his own travel insurance. The system should provide a record for this case also. In this particulary case, Product code will not correspond to a certain product from a travel insurance provider and Europæiske or Gouda extensions don’t need to be filled in.
