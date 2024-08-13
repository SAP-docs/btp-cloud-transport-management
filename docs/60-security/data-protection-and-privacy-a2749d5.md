<!-- loioa2749d51bbe04bccb95370901e7d31b9 -->

# Data Protection and Privacy



For general information about data protection and privacy on SAP BTP, see the SAP BTP documentation under [Data Protection and Privacy](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7e513d31704a4a87831191e504ca850a.html).

Some basic requirements that support data protection are often referred to as technical and organizational measures \(TOM\). The following topics are related to data protection and require appropriate TOMs:

-   Access control: Authentication features as described in section [Security](security-51939a4.md).

-   Separation by purpose: Is subject to the organizational model implemented and must be applied as part of the authorization concept.




### Personal Data processed by SAP Cloud Transport Management Service

SAP Cloud Transport Management service records all tenant changing processes, like landscape transports and landscape configurations. They’re recorded together with the user who performs the action and the time when it was done. Doing so, the user is identified by its user ID, maintained in the configured identity provider, and used during login. Sensitive personal data isn’t processed by the service.

SAP Cloud Transport Management stores file names, and displays them in the logs. In addition, the service transfers files to the connected deployment services. Do not use any personal data in names of files that are uploaded to the service. This is also true for MTA extension descriptors.



### Personal Data Encapsulation

SAP Cloud Transport Management ensures that tenant-specific content is stored in a separate schema so that this data isn’t visible in other tenants.



### View Personal Data

User information is shown in the SAP Cloud Transport Management user interface and available using a REST API, when the corresponding landscape-related or transport-related entities are requested.



### Deletion of Personal Data

The tenant-specific and user-specific persistency as done by SAP Cloud Transport Management is related to the lifecycle of the tenant subscribed to the service. The records are required to fulfill auditability requirements. The deletion of all data is performed as part of the unsubscription process.

> ### Note:  
> In order to keep the data for the legally required retention period, the corresponding tenant-based subscription to the SAP Cloud Transport Management SaaS application must be in place.



<a name="loioa2749d51bbe04bccb95370901e7d31b9__section_uhn_qrf_z2b"/>

## Related Information

For more information about data protection in SAP BTP, see [Data Protection and Privacy](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7e513d31704a4a87831191e504ca850a.html) in the SAP BTP documentation.

