# Insurance Payload Log (Gouda & Europæiske)

### Introduction

The **Insurance Payload Log** provides visibility into the data sent from Tourpaq to external insurance providers, specifically **Gouda** and **Europæiske**.

This functionality is directly related to:

* **Brands → General → Insurance** (where insurance providers are configured)
* **Booking flow** (where insurance is added to passengers)
* **API integrations** (where data is transmitted to external systems)

The log enables traceability of insurance communication and is primarily used for troubleshooting and audit purposes.

***

### Overview

The Insurance Payload Log stores structured records of all payloads sent to:

* Gouda&#x20;
* Europæiske&#x20;

The log captures key booking and travel data along with the result of the API transmission.

***

### Purpose

* Provide transparency into data sent to insurance providers
* Support debugging of API issues
* Enable verification of successful insurance reporting
* Maintain a historical record of insurance transactions

***

### Requirements

*   Insurance provider configured under **Brands → General → Insurance**&#x20;

    <figure><img src="../../.gitbook/assets/image (757).png" alt=""><figcaption></figcaption></figure>
* Active bookings with Travel or Cancellation insurance
* API communication enabled between Tourpaq and provider

***

### Navigation

This log is **available in Setup -> Internal Logs -> Insurance Hystory (Type)**

Access is provided via:

* **Elastic (logging platform)**
* Available to **Tourpaq Support**&#x20;

***

### Interface Overview

<figure><img src="../../.gitbook/assets/image (772).png" alt=""><figcaption></figcaption></figure>

The interface consists of two main sections:

**1. Filters Bar**

Located at the top of the page:

* **Date period** – defines the time interval for logs
* **Select user** – filters logs by user
* **Select type** – filters by entity type (e.g. _InsuranceHistory_)
* **Filter type ID** - filters by Key ID
* **Display** – loads results
* **Clear** – resets filters
* **Export** – downloads the result set

**2. Results Table**

Displays log entries grouped by execution instance (timestamp + user + type).

Each entry represents one payload sent to an insurance provider.

***

#### Field Description

Each row in the table represents a logged operation on a specific entity property.

| Field              | Description                                           |
| ------------------ | ----------------------------------------------------- |
| **KeyId**          | Booking number                                        |
| **Action**         | Type of operation performed (e.g. _Insert)_.          |
| **Entity Name**    | Log type (in this case, _InsuranceHistory_).          |
| **Property Name**  | The specific field that was modified or recorded.     |
| **Original Value** | The previous value before the change (if applicable). |
| **New Value**      | The new value after the operation.                    |
| **Agency**         | The brand or agency context where the change applies. |
| **Description**    | Additional system-generated details about the action. |

### Property Names Description

Each log entry contains the following fields:

#### - Insurance Booking date: Date when the insurance product was added to the booking.

* Reflects when insurance became active in the booking
* May differ from the booking creation date

#### -  Type of insurance: Defines the insurance category (Travel Insurance)

* Determines which API endpoint and logic are used

#### - Reporting date to Gouda/Europæsike: Date when the payload was sent to the insurance provider.

* Used to track delays or failures in reporting
* Important for compliance with provider requirements

#### - Arrival gateway: The arrival destination associated with the booking.

* Typically corresponds to IATA or configured arrival location
* Used by insurance provider to determine travel region

#### - Departure date: Start date of the travel.

* Used in insurance policy calculation
* Must align with booking travel dates

#### - Status (OK / FAILED): Indicates the result of the API transmission.

Values:

* **OK** → Payload successfully processed by provider
* **FAILED** → Error occurred during transmission
* Critical for monitoring integration health
* Used as primary filter during troubleshooting

***

### Configuration Steps

No direct configuration is required for the log itself.

To ensure logging works correctly:

1.  Configure insurance provider under:\
    **Brands → General → Insurance**&#x20;

    <figure><img src="../../.gitbook/assets/image (758).png" alt=""><figcaption></figcaption></figure>
2. Ensure valid credentials are entered:
   * Insurance Agent Username
   * Insurance Agent Password
   * Insurance Agent Code
   * Insurance Agency Code
3. Create a booking with insurance
4. Trigger insurance reporting (automatic or manual process)

The system will automatically generate log entries.

***

### System Behavior

* A log entry is created each time a payload is sent to Gouda or Europæiske
* Applies to both Travel and Cancellation insurance
* Logs are stored in Elastic
* Data retention is a minimum of **12 weeks**
* Logs are read-only and cannot be modified

If transmission fails:

* Status is marked as **FAILED**
* Entry remains available for investigation

***

### Examples

#### Example 1 – Successful Transmission

* Booking number: 123456
* Type of insurance: Travel
* Reporting date: 01.02.2026
* Status: OK

Interpretation:\
Insurance data was successfully sent and accepted.

***

#### Example 2 – Failed Transmission

* Booking number: 123789
* Type of insurance: Cancellation
* Reporting date: 02.02.2026
* Status: FAILED

Interpretation:\
Payload was not processed successfully. Investigation required.

***
