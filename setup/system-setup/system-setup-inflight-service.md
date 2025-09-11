# System Setup – Inflight Service

### **Overview**

The **Inflight Service** module allows Tourpaq to generate and send transport reporting files for inflight services. These files are typically exported to airline or transport providers via FTP and are used for passenger service management.

### **Purpose**

* Automate the generation of inflight service reports.
* Ensure accurate passenger information is sent to transport providers.
* Centralize configuration of file generation and delivery.

### **Configuration Fields**

| **Field**               | **Description**                                                                   |
| ----------------------- | --------------------------------------------------------------------------------- |
| **Username / Password** | Credentials for accessing the inflight service system.                            |
| **Host Address**        | FTP server address for file delivery.                                             |
| **File Prefix**         | Prefix for generated files (default: `PassengerData_`).                           |
| **Folder**              | FTP folder path where files are stored. Use `//` as directory separators.         |
| **Port**                | FTP port (default: 21 if left blank).                                             |
| **Enabled**             | Check to enable inflight service; uncheck to disable file generation and sending. |

### **Usage Notes**

* Only administrators can configure inflight service settings.
* Ensure that the folder structure exists on the FTP server to prevent errors.
* Files are named automatically with the prefix and current date.
* Disabled services will not generate or send files.
