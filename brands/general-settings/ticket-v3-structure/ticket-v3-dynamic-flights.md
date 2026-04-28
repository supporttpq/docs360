# Ticket V3 - Dynamic flights

### Overview

This feature extends the e-ticket structure for bookings using **System Transport (dynamic flights)** by adding a dedicated page with detailed flight and passenger information.

The goal is to provide travelers with essential flight-related data such as PNR, e-ticket number, and baggage details.

***

### When It Applies

The additional page is included in the e-ticket when:

* The transport type is **System Transport**
* The booking includes **dynamic flights (GDS-based)**

***

### Page Placement

* The new page is inserted **before the Hotel Description page**
* It follows the same layout conventions as existing pages:
  * Header with **logo and booking number**
  * Footer with **page numbering**

***

### Page Structure

The page contains **two tables** and an optional informational text.

<figure><img src="../../../.gitbook/assets/image (782).png" alt=""><figcaption></figcaption></figure>

***

### Table 1: Passenger Flight Details

<figure><img src="../../../.gitbook/assets/image (785).png" alt=""><figcaption></figcaption></figure>

#### Header

```
DETAJLER OM DIN REJSE MED RUTEFLY
```

#### Structure

| Column | Field       | Description                                     |
| ------ | ----------- | ----------------------------------------------- |
| 1      | (No header) | Passenger number                                |
| 2      | Fornavn     | Passenger first name                            |
| 3      | Efternavn   | Passenger last name                             |
| 4      | Bagage      | Baggage information                             |
| 5      | PNR         | Amadeus reservation code from Booking → GDS tab |
| 6      | E-ticket    | Ticket number from Booking → GDS tab            |

#### Behavior Rules

* **PNR** is always retrieved from the GDS tab
* **E-ticket**:
  * Displayed only if the ticket has been issued
  * If not issued → field remains empty

***

### Table 2: Flight Information

* Contains **7 columns**
* Structure is identical to the **"FLYINFORMATION"** table shown on the first page of the e-ticket

This ensures consistency in how flight segments are displayed across the document.

***

### Additional Content

Below the second table:

*   Display the content configured in:

    ```
    User → Brands → GDS tab
    ```

<figure><img src="../../../.gitbook/assets/image (784).png" alt=""><figcaption></figcaption></figure>

This allows brand-specific messaging related to dynamic flights (e.g., check-in instructions, airline policies, or disclaimers).

***

### Summary of Behavior

* A new page is dynamically generated for **System Transport bookings**
* It consolidates:
  * Passenger-level flight data (PNR, e-ticket, baggage)
  * Flight segment details
  * Brand-specific GDS messaging
* Ensures that travelers receive complete and structured flight information in the e-ticket
