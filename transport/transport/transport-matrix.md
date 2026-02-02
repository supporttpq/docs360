# Transport Matrix

### Overview

The **Transport Price Control** module uses a calculation matrix to determine **load factors**.

The matrix shows expected transport occupancy based on:

* the **departure week**
* the **number of weeks remaining** until departure

### Purpose

Use the matrix to forecast occupancy trends and adjust pricing and planning earlier.

It helps you spot weak and strong sales periods across departures.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

### FAQ

<details>

<summary>What is the difference between <strong>Dept weeks</strong> and <strong>Weeks to dept</strong>?</summary>

* **Dept weeks** is _when the transport departs_ (calendar week number).
* **Weeks to dept** is _how far away the departure is_ (lead time).

</details>

<details>

<summary>What do the matrix values represent?</summary>

They represent the expected occupancy percentage for the given combination of departure week and lead time.

</details>

<details>

<summary>Why do some cells show <strong>0</strong> (or very low values)?</summary>

Typical reasons:

* The departure week is not expected to sell (seasonality).
* The lead time is too short for meaningful sales.
* The matrix has not been tuned for that scenario yet.

</details>

<details>

<summary>Can I change the matrix values?</summary>

Yes, if you have access to the Transport Price Control configuration. Update values carefully, since they impact planning decisions downstream.

</details>

<details>

<summary>How is this matrix used in the system?</summary>

It is used as an input for load-factor calculations inside Transport Price Control. Those load factors support decisions like pricing adjustments and capacity planning.

</details>

### Related pages

* [Transport Price Control](../../transport-price-control.md)
* [Transport Definition](transport-definition.md)
