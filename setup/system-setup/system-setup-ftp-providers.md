---
description: >-
  Configure FTP/SFTP connections for automated file exchange with external
  providers.
---

# System Setup – FTP Providers

### Overview

**FTP Providers** configures file-transfer connections for external provider services. Tourpaq uses these connections to exchange booking data, manifests, and reports.

Each provider tab stores a separate connection. The configuration can support services such as [Inflight Service](system-setup-inflight-service.md).

{% hint style="warning" %}
FTP usernames and passwords are sensitive.

Restrict access and rotate credentials after suspected exposure.
{% endhint %}

### Purpose

Use **FTP Providers** to establish automated file exchange with each provider. The configuration controls the connection destination, authentication, folder, and transfer security.

### Requirements

Before configuring a provider, collect these details:

* Administrator access to **System Setup**.
* The provider tab that requires the connection.
* The provider's **Username**, **Password**, **Host Address**, and **Port**.
* The required **Folder**, **File Prefix**, and security protocol.
* Approval to activate the connection after validation.

### Navigation

In Tourpaq Office, open **Setup → System Setup → FTP Providers**.

### Interface overview

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (358).png" alt="FTP Providers settings showing Username, Password, Host Address, File Prefix, Folder, Port, Secure FTP, and Enabled."><figcaption><p>FTP Providers configuration fields.</p></figcaption></figure></div>

Select a provider tab before entering the connection details.

### Field descriptions

| Field            | Description                                                                                                            |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Username**     | Required. Identifies the FTP account used to authenticate with the provider server.                                    |
| **Password**     | Required. Authenticates the account defined in **Username**. Enter the provider-supplied value exactly.                |
| **Host Address** | Required. Defines the provider FTP server domain name or IP address.                                                   |
| **File Prefix**  | Optional unless the provider requires a naming convention. Tourpaq adds this value before transferred file names.      |
| **Folder**       | Optional unless the provider requires a target directory. Defines the remote folder for file uploads or downloads.     |
| **Port**         | Required when the provider specifies a custom port. The default FTP port is `21`.                                      |
| **Secure FTP**   | Optional. Enables encrypted FTP transfer when required by the provider. This setting relates to the provider protocol. |
| **Enabled**      | Required to activate the provider connection. Clear this option while the configuration remains unverified.            |

### Configuration steps

To configure a provider connection:

1. In **FTP Providers**, select the required provider tab.
2. In **Username**, enter the provider-supplied account name.
3. In **Password**, enter the provider-supplied password.
4. In **Host Address**, enter the provider server address.
5. In **Port**, enter the provider port or retain `21`.
6. When required, enter the file-name prefix in **File Prefix**.
7. When required, enter the provider directory in **Folder**.
8. Select **Secure FTP** when the provider requires encrypted transfer.
9. Select **Enabled** after validating the connection details.
10. Click **Save**.

### System behavior

Tourpaq uses an enabled provider configuration for the related file-exchange workflow. The selected provider tab determines which service uses the connection.

**File Prefix** helps distinguish transferred files. **Folder** determines the provider directory used for the transfer.

When **Secure FTP** is selected, Tourpaq uses encrypted transfer for that connection. When **Enabled** is cleared, Tourpaq does not use the provider configuration.

### Examples

#### Standard FTP connection

For a provider requiring ordinary FTP:

1. Enter the provider FTP server in **Host Address**.
2. Enter `21` in **Port**.
3. Leave **Secure FTP** cleared.

#### Provider-specific file naming

For a provider requiring the `report_` prefix:

1. Enter `report_` in **File Prefix**.
2. Enter the provider directory in **Folder**.
3. Select **Enabled** after validation.

### Troubleshooting

| Issue                              | Cause                                                        | Resolution                                                         |
| ---------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| Login fails                        | **Username** or **Password** is incorrect.                   | Confirm the credentials with the provider, then re-enter them.     |
| Connection fails                   | **Host Address**, **Port**, or firewall access is incorrect. | Verify the connection details and confirm firewall access with IT. |
| Connection times out               | The provider requires another port or encrypted transfer.    | Confirm the port and select **Secure FTP** when required.          |
| Files appear in the wrong location | **Folder** does not match the provider directory.            | Confirm the required folder path with the provider.                |
| Files overwrite each other         | **File Prefix** does not create unique names.                | Enter the provider-required prefix.                                |

{% hint style="info" %}
Confirm the FTP details with the provider before making changes.

Escalate unresolved connection errors to the IT or security team.
{% endhint %}

### Related pages

Use these related guides:

* [System Setup](./) describes company-wide configuration.
* [Inflight Service](system-setup-inflight-service.md) uses FTP delivery for inflight reporting files.
