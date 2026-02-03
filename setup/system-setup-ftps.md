# System Setup FTPs

### Overview

The **FTPs** page in **System Setup** lets admins configure FTP connections used for imports, exports, and automated file exchange.

It typically covers FTP and secure variants like **FTPS** and **SFTP**.

### Purpose

Use this page to:

* Define new FTP/FTPS connections.
* Store credentials and connection details.
* Enable or disable a configuration.

***

### Page Overview

#### Fields and Configuration Options

| Field            | Description                                                              |
| ---------------- | ------------------------------------------------------------------------ |
| **Name**         | Unique identifier for the FTP configuration.                             |
| **Username**     | FTP server login username.                                               |
| **Password**     | Encrypted password for the FTP account.                                  |
| **Host Address** | IP address or domain of the FTP server (e.g., `ftp.example.com`).        |
| **Path**         | Remote folder path used for uploads/downloads (for example `/incoming`). |
| **Private Key**  | Private key used for key-based authentication (typically SFTP).          |
| **Passphrase**   | Passphrase used to decrypt the private key (if the key is encrypted).    |
| **Secure FTP**   | Enables encrypted file transfer (FTPS or SFTP, depending on the server). |
| **Enabled**      | Activates this FTP configuration.                                        |

***

### Typical Use Cases

* Export PNL reports nightly to a transport operator via FTPS.

***

### How to Add a New FTP Configuration

1. Go to **Setup → System Setup → FTPs**.
2. Click **Create**.
3. Fill in **Name**, **Host Address**, and **Path**.
4. Add credentials:
   * Use **Username/Password** for password login.
   * Use **Private Key** (and **Passphrase**) for key login.
5. Enable **Secure FTP** if your server requires encryption.
6. Tick **Enabled**, then click **Save**.

{% hint style="warning" %}
FTP credentials are sensitive.

Limit access to admins and rotate passwords if exposed.
{% endhint %}

### Troubleshooting

#### Login failed

* Re-check **Username** and **Password**.
* If you use keys, verify **Private Key** and **Passphrase**.

#### Can’t connect to the server

* Verify **Host Address** is correct.
* Check that outbound FTP/SFTP/FTPS is allowed by firewall.

#### Files land in the wrong folder

* Verify the **Path** matches the provider’s folder.
* Confirm whether a leading `/` is required.

### FAQ

<details>

<summary><strong>What’s the difference between FTP, FTPS, and SFTP?</strong></summary>

**FTP** is unencrypted.

**FTPS** is FTP over SSL/TLS.

**SFTP** runs over SSH and uses different authentication options.

</details>

<details>

<summary><strong>When do I need a private key?</strong></summary>

Use **Private Key** when the server requires key-based login.

This is most common with SFTP.

</details>

<details>

<summary><strong>What should I enter in “Path”?</strong></summary>

Use the remote folder where files should be read or written.

Example: `/incoming` or `/exports`.

</details>

<details>

<summary><strong>How do I verify the setup works?</strong></summary>

Enable the configuration, then run the related import/export job.

Confirm the file appears on the remote server.

</details>
