# Migrate Pricelist

The migrate price list function allows you to make a bulk copy of all pricelists from one agency to another. This can be done only between agencies of the same company.&#x20;

To migrate pricelists, choose Migrate price list from the Price List menu.&#x20;

<figure><img src="../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

* You need to select the source agency you want to migrate from using the “From brand” dropdown. All pricelists from this agency will be copied into the agency selected by the “To brand” dropdown, which will be the destination agency.&#x20;
* The Set Tag option allows defining what tag will be set on all destination price pricelists. To do this, check the checkbox and select a tag from the dropdown. The selected tag will be set on all pricelists on the destination agency. How to define and use price list tags is presented in a separate video.&#x20;
* The increase/decrease amount field allows you to specify a value that will be added to all price fields on destination pricelists. To increase prices, enter a positive number, and to decrease prices, enter a negative number. Note only already set prices on the destination will be affected by this.&#x20;
* Increase/decrease percentage allows you to specify a percentage by which all price fields on destination pricelists will be changed. To add with a percentage, enter a positive number, and to decrease with that percentage, enter a negative number. Note only already set prices on the destination will be affected by this.&#x20;

It is important to say that the increase/decrease amount and percentage fields can be used separately or together; in the latter case, the percentage will be applied and then the amount will be added.&#x20;

* If you want to copy the max rooms fields from source pricelists into destination price lists, check the “copy max room” checkbox.&#x20;
* By default, the migration also makes the necessary brand assignments on transports, hotels, resorts, extras, and discounts. That means the source brand will be assigned to all entities on which the source brand is assigned. If you do not want to change brand assignments on the destination mark, check the “copy only pricelists” checkbox.&#x20;

An additional option that can be used in the “source agency” field that can be set on transport, resort, and destination in their general settings tab. By using the source agency, you specify that a transport, for example, is defined and controlled by that. This is useful when you want to migrate prices in both ways, from and to the same agency. By using the source agency field, you can migrate pricelists that are defined by that agency and avoid being overwritten when you migrate pricelists to that agency. Here you have the option to check if you want to migrate only from transports, resorts or destinations where the source agency is the one you selected in “From brand.”&#x20;

* When ready, click the “Migrate Prices” button.&#x20;

Migrations made in the past are logged so you can keep track of these actions. You also have the option to search through migrations by clicking the “Search Migrations” button.

<figure><img src="../.gitbook/assets/image (51) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;Here you can filter by brands, users who performed the migration, and date of migration.&#x20;

The “Show hidden” button allows you to see migrations older than the number of days specified by “Hide filters” in System Setup.
