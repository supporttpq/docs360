# System Setup – FTP Providers

### Overview

The **FTP Providers** section in **System Setup** is used to configure FTP (File Transfer Protocol) connections for various services. This setup enables the system to securely exchange files (such as booking data, manifests, or reports) with external providers through FTP servers. Each provider (e.g., Inflight Service FTP, Airshoppen FTP, Paxport FTP) can be configured separately.

### Purpose

The purpose of this configuration is to establish automated file transfers between the system and external providers. Correct FTP setup ensures seamless communication, file synchronization, and data integration without requiring manual uploads or downloads.

### Fields & Options

<figure><img src="../../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure>

#### 1. **Username**

* **Description:** The login username required to access the FTP server.
* **Purpose:** Authenticates the system with the provider’s FTP server.
* **Instruction:** Enter the FTP account username provided by the service provider.

#### 2. **Password**

* **Description:** The password paired with the username for FTP login.
* **Purpose:** Provides secure authentication for file transfer.
* **Instruction:** Enter the password exactly as provided. Use the eye icon to reveal if necessary.

#### 3. **Host Address**

* **Description:** The domain name or IP address of the FTP server.
* **Purpose:** Specifies the location of the external FTP server.
* **Instruction:** Enter the FTP host (e.g., `ftp.provider.com` or `192.168.1.1`).

#### 4. **File Prefix**

* **Description:** A text string that will be added at the beginning of files transferred.
* **Purpose:** Helps organize or distinguish files, preventing overwrites or confusion.
* **Instruction:** Define a unique prefix if required by the provider (e.g., `report_`).

#### 5. **Folder**

* **Description:** The target directory on the FTP server where files will be uploaded or downloaded.
* **Purpose:** Ensures files are transferred to the correct location.
* **Instruction:** Enter the path of the designated folder (e.g., `/incoming` or `/exports`).

#### 6. **Port**

* **Description:** The communication port used to connect to the FTP server.
* **Default Value:** `21` (standard FTP port).
* **Instruction:** Enter the port number if the provider specifies a custom one. Otherwise, leave as `21`.

#### 7. **Secure FTP**

* **Description:** Checkbox to enable **SFTP (Secure File Transfer Protocol)** or FTPS (FTP over SSL).
* **Purpose:** Ensures files are transferred over an encrypted connection for better security.
* **Instruction:** Tick this box if the provider requires secure FTP access.

#### 8. **Enabled**

* **Description:** Checkbox to activate or deactivate the FTP configuration.
* **Purpose:** Determines whether this FTP setup is active.
* **Instruction:** Tick this box to enable the connection. Leave unticked if the setup is not yet ready.

### Instructions for Configuration

1. Navigate to **System Setup > FTP Providers**.
2. Select the appropriate tab for the provider you need to configure (e.g., _Inflight Service FTP_).
3. Fill in the required fields:
   * **Username** and **Password** as provided by the FTP provider.
   * **Host Address** of the FTP server.
   * **Port** (leave as `21` unless otherwise specified).
   * Optional fields: **File Prefix** and **Folder** depending on provider requirements.
4. Tick **Secure FTP** if the provider uses encrypted connections.
5. Tick **Enabled** to activate the configuration.
6. Save the configuration.

✅ Once saved, the system will automatically use this setup for exchanging files with the configured provider.

### Troubleshooting Guide

#### 1. **Login Failed / Authentication Error**

* **Cause:** Incorrect username or password.
* **Solution:** Double-check credentials with the provider and re-enter them carefully.

#### 2. **Unable to Connect to FTP Server**

* **Cause:** Wrong host address or firewall blocking the connection.
* **Solution:** Verify the **Host Address** and **Port**. Check with IT if firewall rules are blocking access.

#### 3. **Port Connection Timeout**

* **Cause:** Wrong port number or provider requires Secure FTP.
* **Solution:** Confirm the correct port (default is `21` for FTP, `22` for SFTP). Enable **Secure FTP** if needed.

#### 4. **Files Not Appearing in Correct Location**

* **Cause:** Incorrect folder path.
* **Solution:** Verify the **Folder** field matches the provider’s designated directory.

#### 5. **Duplicate or Overwritten Files**

* **Cause:** No unique file naming convention.
* **Solution:** Use a **File Prefix** (e.g., `daily_` or `report_`) to avoid overwriting.

#### 6. **Connection Works but Files Transfer Insecurely**

* **Cause:** Secure FTP not enabled.
* **Solution:** Tick the **Secure FTP** checkbox if encryption is required.

***

✅ **Tips:**\
Always confirm the required FTP details (username, password, host, port, folder, security requirements) directly with the provider before making changes. If an error persists after checking all fields, escalate the issue to the IT/security team.
