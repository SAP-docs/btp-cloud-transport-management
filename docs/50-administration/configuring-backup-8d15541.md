<!-- loio8d15541fcc7146d29281f1401187bc36 -->

# Configuring Backup

Learn about your options to back up your data in SAP Cloud Transport Management.

SAP Cloud Transport Management stores all your data, such as the landscape configuration, transport requests, uploaded files, and log files, in the PostgreSQL and Object Store databases.

Most of the data is stored in PostgreSQL. SAP keeps backups of the PostgreSQL database instances for a retention period of 14 days. This data can be restored in case of emergency – with the restriction that restoring this data occurs at the datacenter level for all customers in a datacenter, not for individual customers.

Uploaded files, such as MTAs, and archived transport action logs, are stored in Object Store. Object Store doesn’t provide backup and restore functions.

In general, it is not necessary to access uploaded files after they’ve been transported through your landscape. In addition, it’s usually possible to recreate an MTA based on a specific commit.

However, if the automated backup options provided by the service are not sufficient for your company’s policies, you can use the following download and export functions of the SAP Cloud Transport Management service to back up your data and securely store the data locally.

-   Download transport-related logs.
-   Download MTA extension descriptors.
-   Export landscape configuration data.

For more information, see [Customer Data Export](../60-security/customer-data-export-11365bf.md).

