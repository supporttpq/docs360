# Transport Matrix

#### Overview

The Transport Price Control module includes a calculation matrix used to determine various load factors. This matrix provides an overview of expected transport occupancy, based on the relationship between departure weeks and the number of weeks remaining until departure.

#### Purpose

The purpose of this functionality is to help users analyze and predict occupancy trends, enabling more accurate transport planning and pricing decisions. By comparing departure weeks with the time remaining before departure, the system supports proactive adjustments to optimize load factors.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

#### Field Explanations

* **Dept weeks** – Indicates the calendar weeks in which departures occur.
* **Weeks to dept** – Indicates the number of weeks remaining until the departure.
* **Matrix values** – Represent the expected occupancy percentage of the transport. These values are calculated based on the correlation between the departure week and the number of weeks before departure.
