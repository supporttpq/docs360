---
description: Configure FTP, FTPS, and SFTP connections for file exchange.
---

# System Setup FTPs

### Overview

**FTPs** configures FTP connections for imports, exports, and automated file exchange. It is part of the company-wide settings in [System Setup](system-setup/).

The connection can use FTP or secure variants such as FTPS and SFTP.

### Purpose

Use **FTPs** to:

* Define FTP connections.
* Store credentials and connection details.
* Enable or disable a configuration.

### Requirements

Before creating a connection, collect these details:

* **Administrator** rights for **System Setup**.
* The server **Host Address** and **Path**.
* A unique **Name**.
* The server authentication method and credentials.
* The server security requirement.

### Interface overview

Each entry stores the server location, authentication method, security setting, and activation status.

### Field descriptions

| Field            | Description                                                              |
| ---------------- | ------------------------------------------------------------------------ |
| **Name**         | Identifies the FTP configuration. Use a unique name.                     |
| **Username**     | Stores the FTP server login name for password authentication.            |
| **Password**     | Stores the encrypted password for the account in **Username**.           |
| **Host Address** | Defines the FTP server domain name or IP address.                        |
| **Path**         | Defines the remote folder for uploads and downloads.                     |
| **Private Key**  | Stores the key for key-based authentication, typically with SFTP.        |
| **Passphrase**   | Unlocks an encrypted **Private Key**.                                    |
| **Secure FTP**   | Enables encrypted transfer when the target server requires FTPS or SFTP. |
| **Enabled**      | Activates the FTP configuration for related file-exchange workflows.     |

The screen does not indicate required fields. Complete the values required by the target server before enabling the configuration.

### Configuration steps

1. In Tourpaq Office, open **Setup → System Setup → FTPs**.
2. In **FTPs**, click **Create**.
3. In **Name**, enter a unique configuration name.
4. In **Host Address**, enter the FTP server address.
5. In **Path**, enter the remote folder path.
6. For password authentication, enter **Username**.
7. Enter **Password**.
8. For key authentication, add **Private Key**.
9. When required, enter **Passphrase**.
10. Select **Secure FTP** when the server requires encrypted transfer.
11. Select **Enabled** after validating the connection.
12. Click **Save**.

### System behavior

Tourpaq uses an enabled FTP configuration for related imports, exports, and file-exchange workflows.

When **Secure FTP** is selected, Tourpaq uses encrypted transfer for that connection. When **Enabled** is cleared, Tourpaq does not use the configuration.

### Examples

#### Password-authenticated export

An export process uses a password-protected FTP server:

1. Enter the server account in **Username**.
2. Enter its password in **Password**.
3. Set the required **Path**.
4. Select **Enabled**.

#### Key-authenticated transfer

An SFTP server requires key authentication:

1. Add the server key in **Private Key**.
2. Enter **Passphrase** when the key is encrypted.
3. Select **Secure FTP** and save the configuration.

{% hint style="warning" %}
FTP credentials are sensitive.

Restrict access to administrators. Rotate passwords after suspected exposure.
{% endhint %}

### Troubleshooting

#### Login failed

* Verify **Username** and **Password**.
* For key authentication, verify **Private Key** and **Passphrase**.

#### Can’t connect to the server

* Verify **Host Address** is correct.
* Confirm that the firewall allows outbound FTP, FTPS, or SFTP.

#### Files land in the wrong folder

* Verify the **Path** matches the provider’s folder.
* Confirm whether a leading `/` is required.

### Related pages

* [System Setup](system-setup/) describes company-wide configuration.
* [FTP Providers](system-setup/system-setup-ftp-providers.md) configures provider-specific file transfer connections.
