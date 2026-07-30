# System Setup – Inflight Service

### Overview

**Inflight Service** generates transport reporting files for inflight passenger services.

Tourpaq transfers the files to airlines or transport providers through FTP.

The feature works with [Communication](../../transport/transport/communication.md) and transport reporting.

### Purpose

Use **Inflight Service** to automate passenger-service file generation and delivery.

The configuration stores the provider's FTP connection and file-naming requirements.

### Requirements

Before configuring **Inflight Service**, complete these requirements:

* Obtain the provider's FTP host, port, credentials, and target folder.
* Confirm the required file prefix and folder-separator format.
* Ensure **Communication Service** is enabled for the required reporting type.
* Ensure administrator access to **System Setup**.

{% hint style="warning" %}
FTP credentials are sensitive.

Restrict access and rotate the password after suspected exposure.
{% endhint %}

### Navigation

In Tourpaq Office, open **Setup → System Setup → Inflight Service**.

### Interface overview

**Inflight Service** contains connection, file-naming, and activation settings.

The configuration determines where Tourpaq sends generated reporting files.

### Configuration fields

| Field                   | Requirement | Description                                                |
| ----------------------- | ----------- | ---------------------------------------------------------- |
| **Username / Password** | Required    | Stores FTP credentials supplied by the transport provider. |
| **Host Address**        | Required    | Sets the FTP server address for file delivery.             |
| **File Prefix**         | Optional    | Sets the generated-file prefix. Default: `PassengerData_`. |
| **Folder**              | Required    | Sets the target FTP folder. Use `//` as separators.        |
| **Port**                | Optional    | Sets the FTP port. Tourpaq uses `21` when blank.           |
| **Enabled**             | Optional    | Activates file generation and FTP delivery.                |

**Username / Password**, **Host Address**, **Folder**, and **Port** control the provider connection.

**File Prefix** controls the generated filename.

**Enabled** controls whether Tourpaq creates and sends inflight service files.

### Configuration steps

Configure **Inflight Service** as follows:

1. In **System Setup**, open **Inflight Service**.
2. Enter **Username / Password**.
3. Enter **Host Address**.
4. Enter **Folder**.
5. Enter **Port**, when the provider does not use port `21`.
6. Set **File Prefix** to the provider's required naming prefix.
7. Select **Enabled**.
8. Save the configuration.

{% hint style="info" %}
Use the provider's exact folder format.

For example: `//inflight//exports`
{% endhint %}

### System behavior

When **Enabled** is selected, Tourpaq generates inflight service reporting files.

Tourpaq sends the files to the configured FTP server.

Files use **File Prefix** and a date-based suffix.

When **Enabled** is cleared, Tourpaq does not generate or send files.

The **Communication Service** checks reporting schedulers every nine minutes.

### Examples

#### Default FTP port

Leave **Port** blank when the provider uses FTP port `21`.

Tourpaq uses port `21` for the connection.

#### Provider-specific folder

Set **Folder** to `//inflight//exports` when the provider requires that location.

Tourpaq transfers generated files to the configured folder.

### Operational guidance

#### Usage notes

* Only administrators can configure **Inflight Service**.
* Ensure the target folder exists on the FTP server.
* Confirm file delivery after enabling a new provider configuration.

#### Troubleshooting

* **No file is created:** Confirm **Enabled** is selected and reporting is triggered.
* **File is not delivered:** Verify **Host Address**, **Port**, **Username / Password**, and **Folder**.
* **FTP connection fails:** Confirm the server is reachable and **Port** is open.
* **Files use the wrong folder:** Check **Folder** and the required `//` separators.

### Related pages

* [Communication](../../transport/transport/communication.md) explains transport reporting and service activation.
* [System Setup](./) lists company-wide configuration areas.
