# Automatic Seating

#### Overview

The **Automatic Seating** feature automatically assigns seats to passengers who do not already have a seat assigned. It ensures unassigned passengers are seated on the aircraft according to predefined rules, without requiring manual input.

#### Purpose

This feature streamlines the seat assignment process, reduces manual work, and ensures passengers are seated before departure. It also provides flexible notification options to keep stakeholders informed once the process is completed.

#### Activation

Automatic Seating is enabled in **SuperAdmin** under the **Upsale** category. It is divided into two options:

* **Automatic Seating** – for normal transports.
* **Automatic Real Transport Seating** – for real transports.

#### Transport Page Configuration

When the feature is activated, a new section becomes available on the **Transport** page, containing the following settings:

* **Use Automatic Seating** – If checked, the system will automatically assign seats for this transport.
* **Hours before departure** – Defines how many hours before departure the automatic seating process will run.
* **Email address(es)** – Enter one or more email addresses (separated by commas). After automatic seating is completed, a report is sent to the listed recipients, based on the chosen reporting type.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

#### Booking Page Indicators

On the booking page, passengers assigned through automatic seating are marked with:

* The passenger’s name displayed in **shadowed text**.
* **No seat supplement** – The seat supplement will not appear in the Customer Center or on the passenger’s ticket.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Manual Assignment – Keep Seat Price

When assigning seats manually, the **Keep seat price** option is available:

* If checked, the **SEAT supplement** will not be added to the passenger.

#### FAQ

**When does automatic seating run?**\
It runs the configured number of hours before departure, per transport, when **Use Automatic Seating** is enabled.

**Who gets seats assigned automatically?**\
Only passengers without a seat assignment are affected. Existing seat assignments are kept.

**What is the difference between “Automatic Seating” and “Automatic Real Transport Seating”?**\
Use **Automatic Seating** for normal transports. Use **Automatic Real Transport Seating** for real transports.

**Who receives the report email?**\
Recipients are taken from **Email address(es)** on the Transport page. Reporting follows the selected reporting type.

**Why don’t I see the seat supplement on the ticket/Customer Center?**\
Passengers assigned through automatic seating are marked with **No seat supplement**, so the supplement is not shown externally.
