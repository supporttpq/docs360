# Automatic ticket issue

### Overview

The **Automatic Ticket Issue** feature enables automated issuing of e-tickets for GDS bookings handled through Amadeus.

Instead of issuing tickets immediately after booking, the system monitors reservations and issues tickets at the most favorable time, based on ticketing deadlines.

This applies to:

* Bookings created in Tourpaq
* Reservations created directly in Amadeus

### Purpose

The purpose of this feature is to:

* Optimize ticket issuing timing
* Reduce manual workload
* Avoid missed ticketing deadlines
* Improve operational efficiency
* Ensure paid bookings are ticketed before deadline

By issuing tickets closer to the ticketing time limit, financial flexibility is improved while maintaining compliance with airline rules.

### Setup Configuration

#### Navigation

Setup → System Setup → Transport Providers → Amadeus tab → Automatic ticket issuing

<figure><img src="../../.gitbook/assets/image (667).png" alt=""><figcaption></figcaption></figure>

#### Behavior

When enabled:

* The daily automatic ticket issuing service is activated.
* Eligible reservations will be ticketed automatically based on deadline logic.
* Service runs once per day.

When disabled:

* Ticket issuing must be handled manually.
* No automatic deadline monitoring is performed.

### Operational Flow

1.  Reservation exists in Amadeus.

    <figure><img src="../../.gitbook/assets/image (663).png" alt=""><figcaption></figcaption></figure>
2.  The deposit must be paid.

    <figure><img src="../../.gitbook/assets/image (665).png" alt=""><figcaption></figcaption></figure>
3.  The ticketing deadline is registered.

    <figure><img src="../../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure>
4. The system runs a daily ticket-issuing service.
5. If the deadline threshold is met and the booking is eligible:
   *   The ticket is issued.

       <figure><img src="../../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>
6. For same-day deadlines after the daily run:
   * The system still issues tickets automatically if the booking is paid.

### FAQ

<details>

<summary><strong>Which bookings are eligible for automatic ticket issuing?</strong></summary>

Bookings must be handled through **Amadeus** and have a registered ticketing deadline.

The booking must also meet your company’s eligibility rules (for example, deposit paid).

</details>

<details>

<summary><strong>How often does the service run?</strong></summary>

It runs **once per day**.

Ticket issuing is triggered when the deadline threshold is met.

</details>

<details>

<summary><strong>What happens if the deposit is not paid?</strong></summary>

The booking will not be ticketed automatically.

Once the deposit is paid, it becomes eligible for the next run (or same-day handling).

</details>

<details>

<summary><strong>What does “same-day deadlines after the daily run” mean?</strong></summary>

It means a ticketing deadline can occur later the same day, after the scheduled run.

In that case, the system can still issue the ticket automatically when the booking is paid.

</details>

<details>

<summary><strong>Can we still issue tickets manually?</strong></summary>

Yes. Disabling automatic ticket issuing means ticketing must be handled manually.

</details>
