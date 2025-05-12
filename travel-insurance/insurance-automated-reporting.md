# Insurance Automated Reporting

The purpose of the Travel and Cancellation Insurance automated reporting system is to select the insurance options chosen by passengers for their trips and send the corresponding data to the selected insurance providers.

The service supports multiple insurance providers. Initially, two primary providers are available: Gouda and Europæiske. Each agency can select their preferred insurance provider, which can be configured in the Brands menu.

Insurance assets are added to the system via the Travel Insurance or Cancellation Insurance menu, where mappings to the policies provided by Gouda and Europæiske will be defined.

For example, when a travel or cancellation insurance asset is added, an abbreviation is assigned to the insurance, along with abbreviations that indicate which policy/policies from Gouda or Europæiske it corresponds to. Additional options can also be configured for the insurance to help identify the corresponding product from these providers.

Credentials required for authenticating with the insurance provider’s web services can be set up in the Brands menu. For more details, refer to the Insurance Reporting page.

The service runs once daily and processes bookings based on the configured communication type to send the insurance details to the respective providers. The date used for processing will be calculated as follows:

* Departure Date: A specified number of days, configurable in the Brands menu, will be added or subtracted from the current date.
* Deposit Paid Date: A specified number of days, configurable in the Brands menu, will be subtracted from the current date to check for deposit status.

Once the travel or cancellation insurance has been successfully sent to the insurance provider, a confirmation number will be assigned to the corresponding passenger. On subsequent runs, passengers with a confirmation number will be excluded from the selection.

In case of an error during the process, an email will be sent to a predefined email address, which can also be configured in the Brands menu.
