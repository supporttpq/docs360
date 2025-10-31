# Insurance Automated Reporting

#### Overview

The **Insurance Automated Reporting** system is designed to automatically collect information about the **Travel** and **Cancellation Insurance** options selected by passengers and send this data to the respective insurance providers.

The service supports multiple providers, with **Gouda** and **Europæiske** available as the primary options. Each agency can configure its preferred insurance provider within the **Brands** menu.

#### Purpose

The purpose of this service is to ensure that all booked travel and cancellation insurance data is consistently and accurately transmitted to external insurance providers without requiring manual input. This automation helps agencies maintain compliance, streamline reporting, and minimize operational errors.

#### Instructions

**1. Provider Configuration**

* The preferred **insurance provider** (Gouda or Europæiske) can be set up in the **Brands** menu.
* **Credentials** for authentication with the provider’s web services are also defined in the same menu.
* Refer to the **Insurance Reporting** page for detailed setup instructions.

**2. Adding Insurance Assets**

* Insurance assets are added through the **Travel Insurance** or **Cancellation Insurance** menus.
* When adding an asset:
  * Assign an **abbreviation** to the insurance product.
  * Define corresponding abbreviations that indicate the mapped policies from **Gouda** or **Europæiske**.
  * Configure additional options to help identify the corresponding provider product.

**3. Automated Processing**

* The automated service runs **once daily** and processes bookings according to the configured **communication type**.
* Insurance details are sent to the respective providers based on two key criteria:
  * **Departure Date:** The service adds or subtracts a specified number of days (configurable in the Brands menu) from the current date.
  * **Deposit Paid Date:** The service subtracts a configurable number of days from the current date to verify deposit status.

**4. Confirmation and Error Handling**

* When insurance data is successfully sent, a **confirmation number** is assigned to each passenger.
* On subsequent runs, passengers with an existing confirmation number are **excluded** from processing.
* If an error occurs, an **email notification** is automatically sent to a predefined address (also configurable in the Brands menu).
