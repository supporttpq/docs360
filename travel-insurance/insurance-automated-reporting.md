# Insurance Automated Reporting

## Insurance Automated Reporting

### Overview

The **Insurance Automated Reporting** system is designed to automatically collect information about the **Travel** and **Cancellation Insurance** options selected by passengers and send this data to the respective insurance providers.

The service supports multiple providers. **Gouda** and **Europæiske** are primary options. Each agency configures its insurance provider in **Brands**.

### Purpose

The purpose of this service is to ensure that all booked travel and cancellation insurance data is consistently and accurately transmitted to external insurance providers without requiring manual input. This automation helps agencies maintain compliance, streamline reporting, and minimize operational errors.

### Configuration

#### Provider configuration

* The preferred **insurance provider** is set up in **Brands**.
* **Credentials** authenticate with the provider’s web services.
* See [Insurance Reporting](insurance-reporting.md) for reporting settings.

#### Adding insurance assets

* Insurance assets are added through **Travel Insurance** or **Cancellation Insurance**.
* When adding an asset:
  * Assign an **abbreviation** to the insurance product.
  * Define corresponding abbreviations that indicate the mapped policies from **Gouda** or **Europæiske**.
  * Configure additional options to help identify the corresponding provider product.

### System behavior

#### Automated processing

* The automated service runs once daily and processes bookings according to the configured **communication type**.
* Insurance details are sent to the respective providers based on two key criteria:
  * **Departure Date:** The service adds or subtracts a specified number of days (configurable in the Brands menu) from the current date.
  * **Deposit Paid Date:** The service subtracts a configurable number of days from the current date to verify deposit status.

#### Confirmation and error handling

* When the service sends insurance data, it assigns a **confirmation number** to each passenger.
* On later runs, the service excludes passengers with a confirmation number.
* If an error occurs, the service sends an **email notification** to a predefined address in **Brands**.
