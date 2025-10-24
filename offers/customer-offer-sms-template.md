# Customer Offer SMS template

#### **Overview**

The **Customer Offer SMS Template** feature allows users to create predefined SMS templates used for customer communication.\
These templates ensure consistency and save time when sending messages from the **Select Offer** view.

<figure><img src="../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

#### **Configuration Details**

| **Field / Section**     | **Description**                                                                                                                                                                  |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Location**            | The SMS template setup is located under **Brand Settings → Select Offer**.                                                                                                       |
| **Purpose**             | Enables the creation of an SMS template that can be used directly from the **Select Offer** screen to contact customers.                                                         |
| **Variables**           | The SMS template supports predefined placeholders (variables) that dynamically insert specific content when the message is sent.                                                 |
| **\[Message] Variable** | This is the key variable in the template. When an SMS is sent from **Select Offer**, the text written in the message field replaces the `[Message]` placeholder in the template. |
| **Usage**               | Once configured, the SMS can be sent directly from the **Select Offer** view to customers, using the predefined structure and variables.                                         |

<figure><img src="../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Note: There are several variables that can be inserted into the template. The most important one is the \[Message]
{% endhint %}

#### **Example**

**Template Example:**

```
Dear [CustomerFirstName],  
[Message]  
Thank you for choosing [BrandName].
```

When sent, the `[Message]` variable is replaced with the text entered by the user in the **Select Offer** message field.

<figure><img src="../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>

#### **Customer Outcome**

* **Efficiency:** Users can quickly send standardized SMS messages without typing them from scratch.
* **Personalization:** Dynamic variables allow messages to be customized for each customer.
* **Consistency:** Ensures all communication aligns with the company’s tone and branding.
* **Automation Readiness:** Simplifies future enhancements for automated SMS triggers linked to offers or booking workflows.
