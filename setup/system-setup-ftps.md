# System Setup FTPs

The **FTPs Page** within the **System Setup** section allows administrators to configure and manage FTP (File Transfer Protocol) and FTPS (FTP Secure) connections used for file imports, exports, or automated data exchanges with external systems.

### Purpose

This page is used to:

* Define new FTP/FTPS connections.
* Set up credentials and access details.
* Enable FTP

***

### Page Overview

#### Fields and Configuration Options

| Field            | Description                                                                                                                                                                                                                                                          |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**         | Unique identifier for the FTP configuration.                                                                                                                                                                                                                         |
| **Username**     | FTP server login username.                                                                                                                                                                                                                                           |
| **Password**     | Encrypted password for the FTP account.                                                                                                                                                                                                                              |
| **Host Address** | IP address or domain of the FTP server (e.g., `ftp.example.com`).                                                                                                                                                                                                    |
| **Path**         | Folder path on the remote server where files are uploaded/downloaded.                                                                                                                                                                                                |
| **Private Key**  | SSL Cerificate - uses as SFTP credentialsCertificate                                                                                                                                                                                                                 |
| Passphrase       | A **passphrase** is like a password, but it’s specifically used to **protect a private key file**. When you generate a key pair (public and private keys) for secure authentication, the private key can be encrypted with a passphrase to prevent unauthorized use. |
| **Secure FTP**   | Checkbox: use secure FTP protocol                                                                                                                                                                                                                                    |
| **Enable**       | Checkbox: when is checked it will make enable the System FTP                                                                                                                                                                                                         |

***

### Typical Use Cases

* Export PNL reports nightly to a transport operator via FTPS.

***

### How to Add a New FTP Configuration

1. Navigate to **System Setup → FTPs**.
2. Click on **“Create”**.
3. Fill in all required fields.
4. Click **“Save”** to store the configuration.
