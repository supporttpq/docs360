# Priceing per pax on extras

### Overview

The **Pricing per Pax on Extras** functionality allows extras to be priced dynamically based on the number of passengers selecting the service. This setup is commonly used for activities such as ski school, guided tours, lessons, or other extras where the price depends on the number of participants.&#x20;

For using pricing per pax on extras, the extras has to be assigned to an extras category with Category Type "ActivityPricedPerPax". This category should be created from Extras->Extras Category:

<figure><img src="../../.gitbook/assets/extra categ actpriceperpax.png" alt=""><figcaption></figcaption></figure>

## Purpose

This feature provides flexible pricing management for extras where:

* Pricing changes depending on how many passengers join
* Individual passengers may pay different amounts
* Hourly pricing may apply
* Different brands can have different pricing structures

It ensures that the correct total and per-passenger price is automatically calculated during booking creation.

## Configuration Setup

### Step 1 – Create the Extras Category

Navigate to: **Extras → Extras Category**

Create a category with:

| Field         | Value                  |
| ------------- | ---------------------- |
| Category Type | `ActivityPricedPerPax` |

<figure><img src="../../.gitbook/assets/extra categ actpriceperpax.png" alt=""><figcaption></figcaption></figure>

This category enables the pricing-per-passenger logic for all extras assigned to it.

## Step 2 – Create the Extra

When creating an extra with the type: `ActivityPricedPerPax,` additional configuration fields become available.

<figure><img src="../../.gitbook/assets/extras activity (1).png" alt=""><figcaption></figcaption></figure>

| Field                              | Description                                                                                                                                                                                                                                                                                                                      |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Minimum pax**                    | Defines the minimum number of passengers required for the extra to be selected in a booking.                                                                                                                                                                                                                                     |
| **Maximum pax**                    | Defines the maximum number of passengers allowed for the extra.                                                                                                                                                                                                                                                                  |
| **Individual price by pax number** | If enabled, the system calculates pricing using the individual price assigned to each passenger count. The final amount is calculated as the sum of the individual prices divided by the total number of passengers booking the extra. If disabled, every passenger pays the same price based on the total number of passengers. |
| **Per Hour**                       | If enabled, the defined price is multiplied by the selected number of hours. If disabled, the price applies for the full day.                                                                                                                                                                                                    |

***

## Extras Prices Configuration

Inside the **Prices** tab, users can define prices per passenger count.

The system allows pricing configuration from:

* 1 passenger
* up to the value defined in **Maximum pax**

<figure><img src="../../.gitbook/assets/extras activity price.png" alt=""><figcaption></figcaption></figure>

Additionally:

* Different prices can be configured for different brands.

***

## Extras Selection in Office

### Availability

If one or more extras are eligible for the booking:

* After **Save Passengers**
* And once the booking status becomes **OK**

a new booking tab using the category tab name becomes visible in the booking.

<figure><img src="../../.gitbook/assets/activity in booking.png" alt=""><figcaption></figcaption></figure>

***

### Selecting Extras

Inside the extras tab, the user can:

* Select the extra from the dropdown list
* Choose the passengers for the extra
* Define the number of hours (if hourly pricing is enabled)

The **Price Rules** section displays the available pricing rules for the selected extra.

As passengers are selected:

* The price is automatically calculated next to each passenger
* The total price is displayed immediately

<figure><img src="../../.gitbook/assets/activity in booking 2.png" alt=""><figcaption></figcaption></figure>

***

### Saving the Selection

After completing the selection:

1. Click **Save Selection**
2. Return to the booking tab
3. The selected extras and pricing will now be visible
4. Save the booking again to finalize the changes

<figure><img src="../../.gitbook/assets/activity in booking save.png" alt=""><figcaption></figcaption></figure>

***

## Price Calculation Example

### Example 1 – Individual Pricing + Hourly Pricing

#### Configuration

| Setting                        | Value   |
| ------------------------------ | ------- |
| Individual price by pax number | Enabled |
| Per Hour                       | Enabled |

#### Price Rules

| Passenger   | Price |
| ----------- | ----- |
| Passenger 1 | 40    |
| Passenger 2 | 30    |
| Passenger 3 | 20    |

#### Duration

* 3 hours

#### Calculation

$$
Price =[(40+30+20)*3]/3
$$

Result:

* Final calculated price per passenger = **90**

***

### Example 2 – Shared Group Pricing

#### Configuration

| Setting                        | Value    |
| ------------------------------ | -------- |
| Individual price by pax number | Disabled |
| Per Hour                       | Disabled |

In this scenario:

* The price configured for the total number of passengers is applied equally to each passenger.

<figure><img src="../../.gitbook/assets/activty calc.png" alt=""><figcaption></figcaption></figure>

***

## Extras Selection in Webbooking

The same extras functionality is available in **Customer Center**

Customers can:

* Select eligible extras
* Choose which passengers participate
* View the automatically calculated pricing

The behavior is similar to the Office booking flow.

***

## Best Practices

* Always verify that the extra belongs to a category with type `ActivityPricedPerPax`
* Ensure **Maximum pax** matches the highest configured pricing tier
* Use **Individual price by pax number** when pricing should differ per participant
* Use **Per Hour** only for services charged based on duration
* Test the setup with multiple passenger combinations before going live
