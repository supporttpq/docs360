---
noIndex: true
---

# Relational Price list

Available for Admin users.

Contact Tourpaq Support for activation.

Relational pricelists allow the linking of 2 price lists (parent and daughter) based on a relation price list. Also, price lists can be linked on top of each other like a ladder, forming a network of price lists.

### Creating a relational price list[​](https://docs.tourpaq.com/docs/documentation/relation-pricelist#creating-a-relational-price-list) <a href="#creating-a-relational-price-list" id="creating-a-relational-price-list"></a>

A relational price list can be created from **Price list / Create price list**.

A room has to be chosen to act as the base room of the relation.

<figure><img src=".gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the example, we have used DD2+1B-DH-AGI150.

Click on the check box **Create new relation price list**.

Fill in the **Relation name**.

Choose the **Relation room**. This should be the same as the room selected. In our case, DD2+1B-DH-AGI150.

After this, click on the **Create relation price** button in the upper right corner.\


> ⚠️ **CAUTION:**

**A RELATIONAL PRICELIST CAN ONLY BE USED IN THE HOTEL IT WAS CREATED FOR.**

### Setting up relation price list[​](https://docs.tourpaq.com/docs/documentation/relation-pricelist#setting-up-relation-price-list) <a href="#setting-up-relation-price-list" id="setting-up-relation-price-list"></a>

For setting up relation price lists between rooms, first you have to display the rooms. You will notice 2 columns in the right part of the screen named **Base Room Price** and **Relation Price**. These columns allow the user to manage the price lists for the hotel.

<figure><img src=".gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Base Room Price** is the room that will provide the price for the price list of the room type.

**Relation Price** is the relation rule that will govern the price.

In our case, we have 6 rooms, DD2+1B-DH-AGI150, DJU21-H-PP-AGI150, EXJU21-PP-H-AGI150, FSU3/24-DH-AGI150, JU21-DH-AGI150, and SSU2/22-DH-AGI150, and one relation, AGI150-Relation.

DD2+1B-DH-AGI150 will provide the base price for DJU21-H-PP-AGI150 according to the rules set up in the relation AGI150-Relation.

DJU21-H-PP-AGI150 will provide the base price for EXJU21-PP-H-AGI150 according to the rules set up in the relation AGI150-Relation.

**Base room price cannot be the same as room type. Meaning you cannot use DD2+1B-DH-AGI150 as a base room for the DD2+1B-DH-AGI150 room type at the same hotel and agency.**

After setting up the base room and relation, click on the **Update new price list** button. It is located in the upper right corner.

<figure><img src=".gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Price list configuration[​](https://docs.tourpaq.com/docs/documentation/relation-pricelist#price-list-configuration) <a href="#price-list-configuration" id="price-list-configuration"></a>

When entering the price list, after selecting all desired filters (⚠️ **Warning:** Price list relation is available only if the hotel is also chosen!!!!) \*\*, after clicking on the **Display** button, you will see 2 new tabs called **Relation PL** and \*\*Related PL\*\*

<figure><img src=".gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Relation PL[​](https://docs.tourpaq.com/docs/documentation/relation-pricelist#relation-pl) <a href="#relation-pl" id="relation-pl"></a>

At this moment only **Relation PL** is of interest. To configure it, click on **View**

<figure><img src=".gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

For a relation price list to be in use, it has to be activated. That is done from the **ACTIVE** column check box.

**The type** column controls the operation that can be done: +, -, \*, /. The values used in the operation in our example are DD2+1B-DH-AGI150 price and 200 (value inserted in P1).

**Currency conversion allows** the conversion of the amount into another currency. Works only for interbrand relations. Conversions for the same brand are not recommended.

Also, when inserting a new currency exchange rate from **System Setup**, the prices will be automatically updated to the new currency in about 5 minutes after the exchange rate has been inserted.

> ⚠️ **Warning:**

If currency or round rule is set, prices are created automatically.

If the type is "+" or "-", there is no need to have values in P1-P4 and D1-D4; the prices will be created.

If the type is "\*" or "/", a value that is greater than "0" is required in P1-P4 and D1-D4; otherwise, the prices will not be created.

The settings are saved using the **Save Relation PL** in the upper right corner.

To see the prices, the base room will need prices first. The rest of the rooms will have their prices set in about 2 minutes from the moment the price list is saved.

<figure><img src=".gitbook/assets/image (8) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

This is the result of the relation price list.

You can see that the EXJU21-PP-H-AGI150 room has the same configuration as DJU21-H-PP-AGI150. This is the default. To set a different configuration for it, you will need to scroll down in the Relation PL and search for it. Since the Relation PL will not display the room for which the relation is applied, the room has to be searched by the creation order in the price list. DJU21-H-PP-AGI150 was created before EXJU21-PP-H-AGI150, and by the departure date, the first departure is 09-05-2025 and the last departure is 17-10-2025.

<figure><img src=".gitbook/assets/image (9) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (10) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

The same configuration is by default set for the created price list relation on the Maltaresor brand. To change it, select the brand Maltaresor, with the transport and hotel, go into the **Relation PL** and perform your changes there.

Since both rooms have been created using the same price relation rule, both rooms will have the same price.

### Related PL[​](https://docs.tourpaq.com/docs/documentation/relation-pricelist#related-pl) <a href="#related-pl" id="related-pl"></a>

This tab displays all price lists related to the current price list. By clicking on **View,** the user is sent to view the prices set for the selected price list.

<figure><img src=".gitbook/assets/image (11) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>
