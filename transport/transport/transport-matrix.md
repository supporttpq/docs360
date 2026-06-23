# Transport Matrix

### Overview

The **Transport Price Control** module uses a calculation matrix to determine **load factors**.

The matrix shows expected transport occupancy based on:

* the **departure week**
* the **number of weeks remaining** until departure

### Purpose

Use the matrix to forecast occupancy trends and adjust pricing and planning earlier.

It helps you spot weak and strong sales periods across departures.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1)  (24).png" alt=""><figcaption></figcaption></figure>

### Fields

* **Dept weeks** – The calendar weeks in which departures occur.
* **Weeks to dept** – The number of weeks remaining until departure.
* **Matrix values** – The expected occupancy percentage (load factor) for the matching week combination.

### How to read it

Pick a **departure week** and a **weeks-to-departure** value.

The intersecting cell is the expected load factor for that situation.

{% hint style="info" %}
Treat the matrix as a planning signal. It is not a guarantee.
{% endhint %}

### Related pages

* [Transport Price Control](../../transport-price-control.md)
* [Transport Definition](transport-definition.md)
