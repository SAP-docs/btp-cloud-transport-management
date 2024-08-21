<!-- loio1fe30308fc554187a629469ec2ef01bc -->

# Administration

Learn about administration tasks that account administrators may need to perform on a regular basis or on demand to configure the service and ensure proper operation.

> ### Note:  
> The initial setup of the service is already done. For more information, see [Initial Setup](../10-initial-setup/initial-setup-66fd728.md).

> ### Tip:  
> SAP Cloud Transport Management service is an *additional* service that must be integrated into the existing development processes of the cloud services or applications whose content it transports. Moreover, the service can be integrated into the change management processes of other services or tools. We recommend that you always start reading the documentation of the application whose content you want to transport to learn about the required configuration tasks.

The following table contains an overview of regular or on demand administration and configuration tasks:

**Overview of Administration Tasks**


<table>
<tr>
<th valign="top" colspan="2">

Task

</th>
<th valign="top">

More Information

</th>
</tr>
<tr>
<td valign="top" colspan="2">

Configure your transport landscape. Configuration tasks include:

-   If your application supports transporting content archives directly in your application: Configuring the export processes in your development environment. You usually do this by creating a destination to the SAP Cloud Transport Management service. The configuration depends on the content you want to transport. If you want to transport SAP Cloud Integration content, for example, you need to configure an SAP Content Agent service instance and different destinations.

    For more information, see [Create Destinations to SAP Cloud Transport Management Service](../20-configure-landscape/create-destinations-to-sap-cloud-transport-management-service-795f733.md#loio795f7337e5d943df98c961303b02678b).

    Some integrations don't require that you create a destination pointing to SAP Cloud Transport Management service. Instead, you must upload the service key of the SAP Cloud Transport Management service instance directly into the application. For example, this is the case for the SAP Continuous Integration and Delivery service.

-   Creating transport nodes representing your landscape , and creating transport routes between the nodes.

    For more information, see [Create Transport Nodes](../20-configure-landscape/create-transport-nodes-f71a4d5.md) and [Create Transport Routes](../20-configure-landscape/create-transport-routes-dddb749.md).

-   Configuring the import processes. That is, creating transport destinations used to address the target end point of a deployment process.

    For more information, see [Create Transport Destinations](../20-configure-landscape/create-transport-destinations-c9905c1.md).


In addition, you can integrate SAP Cloud Transport Management service with change management tools, such as SAP Cloud ALM Feature Management to handle the deployment to the target environments. For more information, see [Integrating SAP Cloud Transport Management service with SAP Cloud ALM](../70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__calm).

</td>
<td valign="top">

[Configuring the Landscape](../20-configure-landscape/configuring-the-landscape-3e7b042.md)

</td>
</tr>
<tr>
<td valign="top" colspan="2">

Grant user roles available for SAP Cloud Transport Management according to the tasks users need to perform.

</td>
<td valign="top">

[Security](../60-security/security-51939a4.md)

</td>
</tr>
<tr>
<td valign="top" colspan="2">

Configure archiving settings for the transport actions that take place in your subaccount.

</td>
<td valign="top">

[Configure Archiving Settings of Transport Actions](../configure-archiving-settings-of-transport-actions-0507a06.md)

</td>
</tr>
<tr>
<td valign="top" colspan="2">

Configure SAP Cloud Transport Management service to send notifications using SAP Alert Notification Service for actions started in the service, such as the creation of a transport request and the start and completion of an import.

</td>
<td valign="top">

[Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](../receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md)

</td>
</tr>
<tr>
<td valign="top" colspan="2">

Determine, if the backup functions of SAP Cloud Transport Management are sufficient, or if your company policies require additional manual exports or downloads of specific data.

</td>
<td valign="top">

[Configuring Backup](configuring-backup-8d15541.md)

</td>
</tr>
<tr>
<td valign="top" colspan="2">

Manage the storage space available in your subaccount.

</td>
<td valign="top">

[Background Information: Storage Capacity](background-information-storage-capacity-e8d5187.md)

</td>
</tr>
<tr>
<td valign="top" colspan="2">

To access additional features of the SAP Cloud Transport Management user interface, update the service \(application\) plan.

</td>
<td valign="top">

[Updating the Service Plan](updating-the-service-plan-1717e87.md)

</td>
</tr>
</table>





### More Information

For general information about administration and operation tasks in SAP BTP, such as management and configuration of global accounts and subaccounts, refer to the following SAP BTP documentation: [Administration and Operations](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/e183664210cf460796de3d90ca6bb6c3.html) under *Administration and Operations in the Cloud Foundry Environment*.

-   **[Configuring Backup](configuring-backup-8d15541.md "Learn about your options to back up your data in SAP Cloud Transport Management. ")**  
Learn about your options to back up your data in SAP Cloud Transport Management.
-   **[Background Information: Storage Capacity](background-information-storage-capacity-e8d5187.md "The storage capacity for files uploaded to SAP Cloud Transport Management service is limited for each
		subscription.")**  
The storage capacity for files uploaded to SAP Cloud Transport Management service is limited for each subscription.
-   **[Updating the Service Plan](updating-the-service-plan-1717e87.md "To access additional features of the SAP Cloud Transport Management user interface, update the
		service (application) plan.")**  
To access additional features of the SAP Cloud Transport Management user interface, update the service \(application\) plan.

