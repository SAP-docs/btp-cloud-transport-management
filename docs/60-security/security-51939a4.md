<!-- loio51939a49db9749578b7e237139bfd08d -->

# Security

This section describes the security aspects that are relevant for SAP Cloud Transport Management service.



<a name="loio51939a49db9749578b7e237139bfd08d__section_zbw_m5d_r3b"/>

## SAP Cloud Transport Management Role Templates

SAP Cloud Transport Management service delivers the following role templates that you can use to create user roles to enable access to specific tasks.


<table>
<tr>
<th valign="top">

Role Template

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*Administrator* 

</td>
<td valign="top">

Contains the overall administration authorization for all SAP Cloud Transport Management tasks. The *Administrator* has all authorizations of the other roles, as well as additional authorizations. In the import queue, the *Administrator* can add files to the import queue, remove files from the import queue, and reset the status of transport requests. If the *Forward Mode* of a transport node is set to the value *Manual*, the *Administrator* can forward all or selected transport requests to the target import queue.

</td>
</tr>
<tr>
<td valign="top">

*LandscapeOperator* 

</td>
<td valign="top">

Grants authorizations for transport landscape configuration tasks. This includes the following actions:

-   Creating transport nodes and transport routes.
-   Editing, and deleting transport nodes and transport routes.
-   Displaying the landscape action logs.



</td>
</tr>
<tr>
<td valign="top">

*TransportOperator* 

</td>
<td valign="top">

Grants authorizations for tasks in import queues. This includes the following actions:

-   Removing files from the import queue.
-   Forwarding transport requests.
-   Resetting the status of transport requests.
-   Uploading and deleting MTA extension descriptors.
-   Scheduling imports.
-   Disabling/re-enabling the import.
-   Releasing and deleting modifiable transport requests.

This role also includes authorizations for import tasks \(*ImportOperator*\), plus starting the import of selected transport requests \(*ImportSelectedOperator*\). However, it doesn't include authorizations for export tasks, such as adding files to import queues.

</td>
</tr>
<tr>
<td valign="top">

*ImportSelectedOperator* 

</td>
<td valign="top">

Grants authorizations to start the import of selected requests in the import queue.

Use this role to restrict import authorization so that users can import individual requests only, not all requests.

</td>
</tr>
<tr>
<td valign="top">

*ImportOperator* 

</td>
<td valign="top">

Grants authorizations for import tasks. This includes the following actions:

-   Starting the import of all transport requests in the import queue.
-   Testing modifiable transport requests.

This role doesn’t include authorizations for importing selected transport requests, adding files to the import queue, removing files from the import queue, resetting the status of queue entries, and forwarding queue entries.

</td>
</tr>
<tr>
<td valign="top">

*ExportOperator* 

</td>
<td valign="top">

Grants authorizations for export tasks. This includes the following actions:

-   Adding files to import queues, and, if files are transported directly in the application, adding them to a transport request in the application.
-   Creating modifiable transport requests, and adding files to modifiable transport requests.



</td>
</tr>
<tr>
<td valign="top">

*Viewer* 

</td>
<td valign="top">

Grants display authorization in SAP Cloud Transport Management. This role doesn’t include authorizations to perform any landscape configuration or import tasks.

</td>
</tr>
</table>

For more information about how to use SAP BTP Cockpit to create roles and role collections to which you can assign these role templates, see [Building Roles and Role Collections for Applications](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/eaa6a26291914b348e875a00b6beb729.html).



<a name="loio51939a49db9749578b7e237139bfd08d__section_ffn_mqw_ztb"/>

## SAP Cloud Transport Management Role Collections

SAP Cloud Transport Management delivers the following role collections that you can assign to users.


<table>
<tr>
<th valign="top">

Role Collection

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*TMS\_LandscapeOperator\_RC*

</td>
<td valign="top">

Role collection based on the *LandscapeOperator* role.

</td>
</tr>
<tr>
<td valign="top">

*TMS\_Viewer\_RC*

</td>
<td valign="top">

Role collection based on the *Viewer* role.

</td>
</tr>
</table>



<a name="loio51939a49db9749578b7e237139bfd08d__node_specific_attributes"/>

## Transport Node-Specific Attributes

For the role templates *TransportOperator*, *ExportOperator*, *ImportOperator*, and *ImportSelectedOperator* attributes exist that allow you to restrict the corresponding authorizations to specific transport nodes only.

The following attributes exist for SAP Cloud Transport Management:


<table>
<tr>
<th valign="top">

Role Template

</th>
<th valign="top">

Attribute Name

</th>
</tr>
<tr>
<td valign="top">

*TransportOperator*

</td>
<td valign="top">

`TmsNodesTransportOperator`

</td>
</tr>
<tr>
<td valign="top">

*ImportOperator*

</td>
<td valign="top">

`TmsNodesImport`

</td>
</tr>
<tr>
<td valign="top">

*ExportOperator*

</td>
<td valign="top">

`TmsNodesExport`

</td>
</tr>
<tr>
<td valign="top">

*ImportSelectedOperator*

</td>
<td valign="top">

`TmsNodesImportSelected`

</td>
</tr>
</table>

To do this, you create node-specific roles based on the role templates, and add the corresponding attributes to the roles. You enter the transport node names as values of the attributes. For each attribute, you can enter one or multiple transport node names. For these restricted roles with attributes, the corresponding tasks can be performed only in the transport nodes that were entered as attribute values.

> ### Note:  
> The *TmsNodesTransportOperator* attribute restricts the authorizations for the *TransportOperator* tasks only, but not for the *ImportOperator* and *ImportSelectedOperator* tasks that also belong to this role.
> 
> To restrict authorizations for *ImportOperator* and *ImportSelectedOperator* tasks as well, create separate custom roles based on the respective templates. For *ImportOperator* tasks, set the `TmsNodesImport` attribute to limit access to specific transport nodes. For *ImportSelectedOperator* tasks, set the `TmsNodesImportSelected` attribute.
> 
> This allows you to have a user that is allowed to perform imports in all transport nodes, but perform *TransportOperator* tasks only in specific transport nodes.

> ### Note:  
> When adding attributes to roles, it isn't checked that the transport node names exist in your transport landscape. Equally, when you delete a transport node, you must manually update the corresponding role, if necessary.
> 
> If you don´t add any attributes to a role, this allows unrestricted access to all nodes. If you assign both restricted and unrestricted roles to users, the restricted role takes effect.

For more information about how to use SAP BTP Cockpit to create roles with attributes, see [Attributes](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/713f52ac36a041ef8fdc72560d6cfbcd.html).



<a name="loio51939a49db9749578b7e237139bfd08d__serviceplans"/>

## Service Plans with Specific Authorizations

SAP Cloud Transport Management offers different service plans with specific authorizations when calling the Cloud Transport Management API. The service plans are available for a service instance of Cloud Transport Management and can be used for the *Transport of Content Archives directly in another Application* scenario.


<table>
<tr>
<th valign="top">

Instance Plan

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*standard*

</td>
<td valign="top">

Default plan to access SAP Cloud Transport Management using programmatic access.

This plan provides full access to the Cloud Transport Management API.

Use this service plan for all standard integrations with SAP Cloud Transport Management. This includes integrations from SAP Cloud ALM and Change Request Management/Quality Gate Management of SAP Solution Manager.

</td>
</tr>
<tr>
<td valign="top">

*export*

</td>
<td valign="top">

Plan to access SAP Cloud Transport Management using programmatic access with reduced authorizations for export actions only. This plan allows file upload and node upload/export actions.

Use this service plan to restrict access to SAP Cloud Transport Management, if enhanced security requirements are required. Use it, for example for the integration with SAP Solution Lifecycle Management service or CI/CD pipelines.

</td>
</tr>
<tr>
<td valign="top">

*transport\_operator*

</td>
<td valign="top">

Plan to access SAP Cloud Transport Management using programmatic access with reduced authorizations for transport operator actions only. This plan allows import, reset, forward, and delete actions.

Use this service plan to restrict access to SAP Cloud Transport Management, if enhanced security requirements are required.

</td>
</tr>
</table>



<a name="loio51939a49db9749578b7e237139bfd08d__sp"/>

## Malware

SAP Cloud Transport Management treats archives that it uploads, attaches, or transports as ‘black box’ content. This means, SAP Cloud Transport Management doesn’t process or extract any archives. They’re only temporarily persisted as BLOB \(Binary Large Objects\) in the database. Therefore, SAP Cloud Transport Management doesn’t perform any malware scans, since it's the obligation of the target applications, services, or content runtimes which process the uploaded or referenced archive to perform malware scans. The only exception is the transport of an MTA archive. Here, SAP Cloud Transport Management reads the metadata of the MTA, and ensures that the MTA archive contains a malware-free MTA deployment descriptor file. However, the modules of the MTA itself aren’t covered by the check since it´s again the obligation of the corresponding applications, services, or content runtimes that are called with the module content to perform the malware scans.



<a name="loio51939a49db9749578b7e237139bfd08d__section_r4d_gqv_qmb"/>

## Encryption

The uploaded archives and MTA extension descriptors aren't encrypted by the persistency layer used by SAP Cloud Transport Management even if the content upload was done via SSL/TLS. Keep this in mind, if the content that you want to transport contains sensitive data. The uploaded archives are only temporarily persisted. They are deleted after a fixed period of time after they were transported in the configured landscape.

-   **[Auditing and Logging Information](auditing-and-logging-information-9e3ee94.md "Here you can find a list of the security events that are logged by SAP Cloud Transport Management
        service.")**  
Here you can find a list of the security events that are logged by SAP Cloud Transport Management service.
-   **[Data Protection and Privacy](data-protection-and-privacy-a2749d5.md "")**  

-   **[Customer Data Export](customer-data-export-11365bf.md "Exporting transport-related action logs, MTA extension descriptors, and the current landscape configuration is possible at any time as
		part of the user interface of SAP Cloud Transport Management service. Additionally, it is possible to request a
		final customer data export as part of a decommissioning process.")**  
Exporting transport-related action logs, MTA extension descriptors, and the current landscape configuration is possible at any time as part of the user interface of SAP Cloud Transport Management service. Additionally, it is possible to request a final customer data export as part of a decommissioning process.

**Related Information**  


[SAP BTP Security Recommendations](https://help.sap.com/docs/BTP/c8a9bb59fe624f0981efa0eff2497d7d/531f33def8074ccdb6f1f784a34dafcb.html?seclist-service=Cloud%20Transport%20Management)

