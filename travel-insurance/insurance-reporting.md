# Insurance Reporting

## Insurance Reporting

### Overview

Travel and cancellation insurance reporting is managed in **Brand settings** under the **Insurance** tab.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="Insurance reporting settings in Brand settings"><figcaption></figcaption></figure></div>

### Reporting schedule

The **Communication type** controls the reporting schedule:

* **Days before/after departure**: Reports insurance to the company `x` days before or after departure.
  * A value of `0` reports insurance on the departure date.
  * A value of `-1` reports insurance one day before departure.
  * A value of `1` reports insurance one day after departure.
* **Days after deposit paid date**: Reports insurance to the company `x` days after deposit payment.

### Passenger details override

The booking **Passenger details** tab can also control insurance reporting.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (66).png" alt="Insurance reporting date in Passenger details"><figcaption></figcaption></figure></div>

### System behavior

When both settings define a reporting date, the system uses the earliest date.

### Examples

#### Example one

A booking departs on `09.06.2025`. Insurance reporting is set to one day before departure. The **Passenger details** date is `08.06.2025`. The system reports insurance on `08.06.2025`.

#### Example two

The same booking has reporting set to seven days before departure. The **Passenger details** date is `07.06.2025`. The system reports insurance on `02.06.2025`.
