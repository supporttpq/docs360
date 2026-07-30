---
description: Review insurance payload activity sent to Gouda and Europæiske.
---

# Insurance Payload Log (Gouda & Europæiske)

## Insurance Payload Log (Gouda & Europæiske)

The **Insurance Payload Log** records insurance data sent to **Gouda** and **Europæiske**. Use it to investigate reporting activity for [Travel Insurance](../../travel-insurance/) and [Cancellation Insurance](../../cancellation-insurance/).

### Overview

The log stores one entry for each payload sent to an insurance provider. Each entry includes booking data, travel data, and the transmission result.

### Purpose

Use the log to:

* Verify insurance reporting.
* Investigate provider transmission failures.
* Maintain an audit record of insurance transactions.

### Requirements

The log requires:

* An insurance provider configured under **Brands → General → Insurance**.
* An active booking with Travel or Cancellation insurance.
* API communication between Tourpaq and the provider.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (757).png" alt="Insurance provider settings under Brands, General, and Insurance"><figcaption></figcaption></figure></div>

### Navigation

The log is available in **Setup → Internal Logs → Insurance Hystory (Type)**.

The following roles can access the log:

* **Elastic**
* **Tourpaq Support**

### Interface overview

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (772).png" alt="Insurance Payload Log filters and results table"><figcaption></figcaption></figure></div>

The interface contains filters and a results table.

#### Filters

| Field              | Description                                                |
| ------------------ | ---------------------------------------------------------- |
| **Date period**    | Defines the period used to retrieve log entries.           |
| **Select user**    | Limits results to activity from the selected user.         |
| **Select type**    | Limits results by entity type, such as `InsuranceHistory`. |
| **Filter type ID** | Limits results by **KeyId**.                               |
| **Display**        | Loads entries matching the selected filters.               |
| **Clear**          | Removes the selected filter values.                        |
| **Export**         | Downloads the displayed result set.                        |

#### Results table

The table groups entries by execution instance, user, and type. Each row records one operation for a specific insurance property.

| Field              | Description                                                                  |
| ------------------ | ---------------------------------------------------------------------------- |
| **KeyId**          | Identifies the booking number. Use this value with **Filter type ID**.       |
| **Action**         | Identifies the recorded operation, such as `Insert`.                         |
| **Entity Name**    | Identifies the log entity. Insurance payload entries use `InsuranceHistory`. |
| **Property Name**  | Identifies the insurance property recorded in the row.                       |
| **Original Value** | Shows the previous value when an earlier value exists.                       |
| **New Value**      | Shows the value recorded by the operation.                                   |
| **Agency**         | Identifies the brand or agency context for the entry.                        |
| **Description**    | Shows system-generated information about the operation.                      |

### Property names

The following **Property Name** values identify insurance payload data:

#### Insurance Booking date

Shows the date when insurance was added to the booking. It can differ from the booking creation date.

#### Type of insurance

Shows the insurance category, such as Travel Insurance. The category determines the provider endpoint and reporting logic.

#### Reporting date to Gouda/Europæsike

Shows the date when Tourpaq sent the payload to the provider. Use this value to investigate reporting delays or failures.

#### Arrival gateway

Shows the booking's arrival destination. The value can use an IATA code or a configured arrival location.

#### Departure date

Shows the travel start date from the booking. It supports insurance policy calculations.

#### Status (OK / FAILED)

Shows the provider transmission result:

* **OK** indicates that the provider processed the payload.
* **FAILED** indicates that the transmission encountered an error.

### Configuration steps

The log has no direct configuration. Configure the provider before Tourpaq can record payload activity:

{% stepper %}
{% step %}
#### Open the provider settings

In **Brands**, open **General**.
{% endstep %}

{% step %}
#### Select Insurance

Select **Insurance**.
{% endstep %}

{% step %}
#### Enter Insurance Agent Username

Enter the provider username in **Insurance Agent Username**.
{% endstep %}

{% step %}
#### Enter Insurance Agent Password

Enter the provider password in **Insurance Agent Password**.
{% endstep %}

{% step %}
#### Enter Insurance Agent Code

Enter the provider code in **Insurance Agent Code**.
{% endstep %}

{% step %}
#### Enter Insurance Agency Code

Enter the agency code in **Insurance Agency Code**.
{% endstep %}
{% endstepper %}

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (757).png" alt="Insurance provider credential fields in Brands settings"><figcaption></figcaption></figure></div>

### System behavior

Tourpaq creates a log entry when it sends a payload to Gouda or Europæiske. The log covers Travel Insurance and Cancellation Insurance.

Tourpaq stores logs in Elastic for at least 12 weeks. The entries are read-only.

When a transmission fails, Tourpaq records **FAILED**. The entry remains available for investigation.

### Examples

#### Successful transmission

An entry has the following values:

* **KeyId**: `123456`
* **Type of insurance**: Travel
* **Reporting date to Gouda/Europæsike**: `01.02.2026`
* **Status (OK / FAILED)**: **OK**

The provider processed the insurance payload.

#### Failed transmission

An entry has the following values:

* **KeyId**: `123789`
* **Type of insurance**: Cancellation
* **Reporting date to Gouda/Europæsike**: `02.02.2026`
* **Status (OK / FAILED)**: **FAILED**

Investigate the entry details and provider configuration.

### Related pages

* [Travel Insurance](../../travel-insurance/) configures travel insurance products and provider types.
* [Cancellation Insurance](../../cancellation-insurance/) configures cancellation insurance and external provider mapping.
