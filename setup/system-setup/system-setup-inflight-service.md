# System Setup – Inflight Service

### Overview

The **Inflight Service** module allows Tourpaq to generate and send transport reporting files for inflight services. These files are typically exported to airline or transport providers via FTP and are used for passenger service management.

Go to **Setup → System Setup → Inflight Service**.

{% hint style="warning" %}
FTP credentials are sensitive.

Limit access and rotate the password if you suspect exposure.
{% endhint %}

### Purpose

* Automate the generation of inflight service reports.
* Ensure accurate passenger information is sent to transport providers.
* Centralize configuration of file generation and delivery.

### Configuration fields

| **Field**               | **Description**                                                                   |
| ----------------------- | --------------------------------------------------------------------------------- |
| **Username / Password** | Credentials for accessing the inflight service system.                            |
| **Host Address**        | FTP server address for file delivery.                                             |
| **File Prefix**         | Prefix for generated files (default: `PassengerData_`).                           |
| **Folder**              | FTP folder path where files are stored. Use `//` as directory separators.         |
| **Port**                | FTP port (default: 21 if left blank).                                             |
| **Enabled**             | Check to enable inflight service; uncheck to disable file generation and sending. |

### How to set it up

1. Get the FTP details from your airline/transport provider:
   * Host
   * Port
   * Username/password
   * Target folder
2. Enter the values in **Inflight Service**.
3. Keep the default file prefix unless your provider requires another naming rule.
4. Enable the service and save.
5. Run the export flow and verify the file appears on the FTP server.

{% hint style="info" %}
If your provider requires a specific folder format, mirror it exactly.

Example: `//inflight//exports`
{% endhint %}

### Usage notes

* Only administrators can configure inflight service settings.
* Ensure that the folder structure exists on the FTP server to prevent errors.
* Files are named automatically with the prefix and current date.
* Disabled services will not generate or send files.

### Troubleshooting

* **No file is created:** Confirm **Enabled** is on and the export flow is triggered.
* **File is created but not delivered:** Verify host, port, credentials, and folder path.
* **FTP connection fails:** Confirm the server is reachable from your Tourpaq environment and the port is open.
* **Files land in the wrong folder:** Re-check the **Folder** value and required separators (`//`).

### FAQ

<details>

<summary><strong>What does Inflight Service generate?</strong></summary>

It generates transport reporting files containing passenger/service data.

Those files are delivered to a provider via FTP.

</details>

<details>

<summary><strong>Does disabling the service stop file sending?</strong></summary>

Yes. When **Enabled** is off, Tourpaq does not generate or send files.

</details>

<details>

<summary><strong>What port should I use?</strong></summary>

Use the port provided by your provider.

If empty, Tourpaq defaults to `21`.

</details>

<details>

<summary><strong>How are files named?</strong></summary>

Tourpaq uses the configured **File Prefix** plus a date-based suffix.

If your provider requires a specific naming format, align the prefix with that requirement.

</details>
