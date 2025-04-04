# Migrate Pricelist

Migrate pricelist function allows to make a bulk copy of all pricelists from one agency to another. This can be done only between agencies of the same company.&#x20;

To migrate pricelists, choose Migrate pricelist from the Pricelist menu.&#x20;

<figure><img src="../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

* You need to select the source agency you want to migrate from using the “From brand” dropdown. All pricelists from this agency will be copied into the agency selected by the “To brand” dropdown, which will be the destination agency.&#x20;
* Set Tag option allows defining what tag will be set on all destination pricelists. To do this check the checkbox and select a tag from dropdown. The selected tag will be set on all pricelists on the destination agency. How to define and use pricelist tags is presented in a separate video.&#x20;
* Increase/decrease amount field allows to specify a value that will be added to all price fields on destination pricelists. To increase prices enter a positive number and to decrease prices enter a negative number. Note only already set prices on destination will be affected by this.&#x20;
* Increase/decrease percentage allows to specify a percentage by which all price fields on destination pricelists will by change with. To add with a percentage, enter a positive number and to decrease with that percentage enter a negative number. Note only already set prices on destination will be affected by this.&#x20;

Important to say that the increase/decrease amount and percentage fields can be used separately or together; in the latter case, the percentage will be applied and then amount will be added.&#x20;

* If you want to copy the max rooms fields from source pricelists into destination pricelists check “copy max room” checkbox.&#x20;
* By default, the migration also makes the necessary brand assignments on transports, hotels, resorts, extras and discounts. That means the source brand will be assigned on all entities on which the source brand is assigned. If you do not want to change brand assignments on destination mark “copy only pricelists” checkbox.&#x20;

An additional option that can be used in the “source agency” field that can be set on transport, resort and destination in their general settings tab. By using the source agency, you specify that a transport for example, is defined and controlled by that. This is useful when you want to migrate prices in both ways, from and to the same agency. By using source agency field, you can migrate pricelists that are defined by that agency and avoid being overwritten when you migrate pricelists to that agency. Here you have the option to check if you want to migrate only from transports, resorts or destinations where the source agency is the one you selected in “From brand”&#x20;

* When ready click “Migrate Prices” button.&#x20;

Migrations made in the past are logged so you can keep track of these actions. You also have option to search through migrations by clicking “Search Migrations” button.

<figure><img src="../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;Here you can filter by brands, user who performed the migration and date of migration.&#x20;

The “Show hidden” button allows to see migration older than the number of days specified by “Hide filters” in System Setup.
