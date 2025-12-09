# Select Offer Setup

The **Select Offer** tab defines the visual and textual content used when generating offers for a specific Brand. This configuration controls the images, texts, email templates, reminder settings, and optional sections that appear to customers when receiving an offer or related communication.\
All settings in this area apply exclusively to the active Brand and allow agencies to tailor the customer experience to match their identity and product style.

***

### **Template Images**

The first section contains a set of configurable images that are displayed in the customer-facing offer material. Brands can upload custom visuals to match their marketing profile. Typical images include:

* **Logo** – The brand logo displayed at the top of the offer.
* **Trip Safety Image** – A visual used in the safety or travel information section.
* **More Experiences Image** – An image promoting additional activities or upgrade options.
* **Inkluderet Image** – A visual used in the “Included” section of the offer.

Each image can be uploaded directly or replaced by dragging files into the designated upload areas. A preview (“View full”) allows users to verify the visual before saving.

<figure><img src="../.gitbook/assets/image (499).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
These images are not available in the default template! Please be aware that images will be resized if they are too large for the template. Check the tooltips for each image type to see the recomanded sizes.
{% endhint %}

***

### **Close Reasons & Surcharge Descriptions**

Brands can maintain custom **Close Reasons** used when closing an offer, as well as **Surcharge Descriptions** related to extra fees.\
If no entries exist, this area will show an empty list. Editors can add or edit available reasons and descriptions via the linked configuration screens.

***

### **Email Placeholders**

A link to the list of supported placeholders ensures that editors know which dynamic fields (e.g., customer name, offer number, salesperson) can be inserted into the email templates defined in this section.

<figure><img src="../.gitbook/assets/image (498).png" alt=""><figcaption></figcaption></figure>

***

### **SMS & Email Configuration**

The brand can define communication templates for both email and SMS:

#### **SMS Configuration**

A predefined SMS template can be selected, typically used when sending automated or manual offer notifications. Placeholders such as CustomerFirstName and OfferNo can be inserted to personalize outgoing messages.

#### **Mail Subject & General Text**

The brand can configure:

* **Mail Subject** – The default subject line used when sending offers by email.
* **General Available Product Text** – Generic text included in the offer describing available products or general service information.

These fields support rich text formatting, allowing editors to structure content using headings, bold text, bullet lists, etc.

***

### **Mail Header & Mail Footer**

The offer email can include a fully customizable header and footer.\
The **Mail Header** usually contains a greeting, introduction text, and dynamic placeholders. The **Mail Footer** can include contact information, disclaimers, or brand signatures.

Both fields support full rich-text formatting.

***

### **Unavailable Custom Message**

If a product or offer becomes unavailable, this text is shown to the customer.\
The message can be tailored to reflect the brand’s tone and provide guidance for alternative options.

***

### **Insurance Texts**

Brands can choose whether to display insurance information in the offer. If enabled, the following can be configured:

* **Insurance Link** – A URL directing customers to the insurance provider.
* **Travel Insurance Text** – Description of the travel insurance included or available for purchase.
* **Cancellation Insurance Text** – Information about cancellation coverage.

This area lets brands clarify insurance options and ensure compliance with local requirements.

***

### **More Experiences & Trip Safety Text**

If the brand chooses to display these sections in the offer:

* **More Experiences Text** describes optional activities or upgrades.
* **Trip Safety Text** provides safety instructions or destination-specific information.

Both texts appear alongside the corresponding uploaded images.

***

### **Email Reminder Settings**

The offer system supports automatic reminders based on brand configuration. The following can be defined:

* **Email Reminder Schedule Days** – The number of days to resend the offer, splitted by comma: 7,14,21.
* **Enable Auto Schedule** – Activates automatic reminders for this brand.
* **Enable Auto Schedule Close** – Enableing the checkbox will close the offers after the last email is sent by the scheduler.
* **Display Extra Description** – Enable the checkbox allow to sets custom description visible for included price extras. Must be available in the template.

#### **Mail Reminder Templates**

* **Mail Reminder Subject** – Subject line used for reminder emails.
* **Mail Reminder Body** – Rich-text body for reminder emails.
* **SMS Reminder Body** – Text template used for reminder SMS messages (if enabled).

***

### **Purpose of the Select Offer Tab**

This section centralizes all branding, communication, and informational content related to offers. By configuring the Select Offer settings, the agency ensures that customers receive consistent, professional, and brand-aligned communication throughout the offer lifecycle—from the initial send-out to reminders and follow-up messages.
