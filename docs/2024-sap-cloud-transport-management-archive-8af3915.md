<!-- loio8af391505a4e4489bd5ee1ff284c8c71 -->

# 2024 SAP Cloud Transport Management \(Archive\)





**2024**


<table>
<tr>
<th valign="top">

Technical Component

</th>
<th valign="top">

Environment

</th>
<th valign="top">

Title

</th>
<th valign="top">

Description

</th>
<th valign="top">

Action

</th>
<th valign="top">

Lifecycle

</th>
<th valign="top">

Type

</th>
<th valign="top">

Line of Business

</th>
<th valign="top">

Modular Business Process

</th>
<th valign="top">

Product

</th>
<th valign="top">

Latest Revision

</th>
<th valign="top">

Available as of

</th>
<th valign="top">

Version

</th>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

On-the-fly machine translation is now available for SAP Cloud Transport Management.

</td>
<td valign="top">

On-the-fly machine translation is now available in multiple languages for SAP Cloud Transport Management documentation on SAP Help Portal. This means that you can generate translation of content instantly by selecting the respective language from the dropdown list.

We’d appreciate your feedback through the link provided on the top of each translation page.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-12-20

</td>
<td valign="top">

2024-12-20

</td>
<td valign="top">

2412a

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Immediately delete files attached to transport requests when the corresponding request is manually deleted from all import queues.

</td>
<td valign="top">

Previously, when a transport request was manually deleted from all import queues, the attached files were not erased until the next cleanup run, which caused a delay in freeing up storage space.

See:

-   [Delete Transport Requests](40-using-request-overview/delete-transport-requests-2ef725c.md)

-   [Background Information: Storage Capacity](50-administration/background-information-storage-capacity-e8d5187.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-11-29

</td>
<td valign="top">

2024-11-29

</td>
<td valign="top">

2411b

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Notification-based forward flow for *TmsImportFinished* and *TmsTransportRequestAdded* events.

</td>
<td valign="top">

When you have configured SAP Alert Notification Service to send notifications for actions started in Cloud Transport Management service, the notifications sent for the *TmsImportFinished* and *TmsTransportRequestAdded* events now contain links to the relevant import queues. This allows you to directly start follow-on actions, such as forward or import transport requests, depending on the event for which the notification was sent.

See:

-   [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md)




</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-11-29

</td>
<td valign="top">

2024-11-29

</td>
<td valign="top">

2411b

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Configure File Retention Time

</td>
<td valign="top">

The time that files uploaded to the service are retained in the internal storage of the service depends on the subscribed service plan. After the configured retention time, files that are in a *final* status in all relevant import queues are deleted by an automatic cleanup mechanism. You can now change the default retention time to a supported value \(depending on the service plan\).

See:

-   [SAP Cloud Transport Management Home Screen](sap-cloud-transport-management-home-screen-9ac7880.md)
-   [Background Information: Storage Capacity](50-administration/background-information-storage-capacity-e8d5187.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-10-18

</td>
<td valign="top">

2024-10-18

</td>
<td valign="top">

2410a

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

New Tutorial available on SAP Tutorial Navigator: *Get Started with SAP Cloud Transport Management Service* 

</td>
<td valign="top">

The tutorial illustrates the steps required for the *Initial Setup* of the service.

See: [Get Started with SAP Cloud Transport Management Service](https://developers.sap.com/tutorials/btp-transport-management-getting-started.html)

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-10-18

</td>
<td valign="top">

2024-10-17

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Integration of SAP Build Apps with SAP Cloud Transport Management 

</td>
<td valign="top">

You can now use SAP Cloud Transport Management to transport SAP Build Apps projects.

See:

-   [Supported Content Types](supported-content-types-8961dcb.md#loio8961dcb3edc84a76b84b29565833067b)
-   [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-10-18

</td>
<td valign="top">

2024-08-19

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Documentation enhancements

</td>
<td valign="top">

-   A link was added to a new blog post in SAP Community about changes to the integration of the service with SAP BTP ABAP environment.

    See: [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md)

-   The sample configuration for the SAP Cloud ALM use case was removed from the [Example: Destination to SAP Cloud Transport Management](20-configure-landscape/create-destinations-to-sap-cloud-transport-management-service-795f733.md#loio75fe5d4b4fa3492c87ef6be32ea0b819) topic, since integrating the service with SAP Cloud ALM has become easier.

    See the links in the *SAP Cloud ALM* section of: [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md)




</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-09-21

</td>
<td valign="top">

2024-09-21

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Documentation enhancements

</td>
<td valign="top">

The following topic was enhanced:

-   [Administration](50-administration/administration-1fe3030.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-08-21

</td>
<td valign="top">

2024-08-21

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

New auto-forward modes available for transport nodes. In addition, the previous default value *Auto* was renamed to *Pre-Import*.

</td>
<td valign="top">

The following forward modes are new:

-   *Post-Import*: Transport requests are automatically forwarded, after they've been imported in the current node, regardless of the import results and the request statuses after the import.
-   *On Success*: Transport requests are automatically forwarded, after they've been successfully imported in the current node. An import is successful, if the status of the request after the import is either *Skipped*, *Succeeded*, or *Warning*.

See: [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md) 

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

2407b

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

The English version of the SAP Cloud Transport Management documentation is now open for contributions and feedback using GitHub.

</td>
<td valign="top">

For more information about the process, see [What Is SAP Cloud Transport Management](what-is-sap-cloud-transport-management-5fef9d6.md).

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

2024-08-13

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Documentation enhancements

</td>
<td valign="top">

The following topics in the documentation were enhanced or are new:

-   [Updating the Service Plan](50-administration/updating-the-service-plan-1717e87.md) \(new\)
-   [Monitoring and Troubleshooting](monitoring-and-troubleshooting-c39411d.md) \(changed\)
-   [Monitoring](monitoring-30e60df.md) \(new\)
-   [General Troubleshooting Information](general-troubleshooting-information-1f090ea.md) \(new\)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

New link to Release Navigator for SAP Cloud Transport Management added to the documentation of the service.

</td>
<td valign="top">

The Release Navigator for SAP BTP contains release resources as well as general resources for SAP BTP products and services.

See:

-   [Release Navigator for SAP Cloud Transport Management](https://readiness-at-scale.enable-now.cloud.sap/pub/20230621_ras/index.html?show=book!BO_EC8330B09B97CDBE#SL_389720104C687893)

-   [What Is SAP Cloud Transport Management](what-is-sap-cloud-transport-management-5fef9d6.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

2024-08-12

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP Cloud Transport Management service available on new data center.

</td>
<td valign="top">

SAP Cloud Transport Management service is now also available on Google Cloud platform in the Israel - Tel Aviv \(IL30\) region.

See: [SAP Cloud Transport Management in SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management/?region=all&tab=service_plan) 

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-07-16

</td>
<td valign="top">

2024-07-16

</td>
<td valign="top">

2406b

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

New blog posts available on SAP Cloud Transport Management topics.

</td>
<td valign="top">

See:

-   [How to migrate an SAP Cloud Transport Management instance](https://community.sap.com/t5/technology-blogs-by-sap/how-to-migrate-an-sap-cloud-transport-management-instance/ba-p/13730165)
-   [SAP Datasphere Content Network Package Transport via BTP Transport Management service.](https://community.sap.com/t5/technology-blogs-by-sap/sap-datasphere-content-networkpackage-transport-via-btp-transport/ba-p/13759735)
-   [Transport configuration in SAP Batch Release Hub for Life Sciences](https://community.sap.com/t5/supply-chain-management-blogs-by-sap/transport-configuration-in-sap-batch-release-hub-for-life-sciences/ba-p/13756020)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-07-16

</td>
<td valign="top">

2024-07-16

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Enhancements to archiving of transport action logs

</td>
<td valign="top">

The following enhancements were made to the archiving of transport logs:

-   The default data retention time for transport action logs was extended from 6 to 7 years for all existing and new subscriptions.
-   Additional configuration option in archiving settings: You can now decide whether you want to anonymize user data, such as user names and email addresses, during an archiving run. User data is no longer anonymized by default.

See:

-   [Transport Action Logs](transport-action-logs-86319ed.md)
-   [Configure Archiving Settings of Transport Actions](configure-archiving-settings-of-transport-actions-0507a06.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-07-16

</td>
<td valign="top">

2024-07-16

</td>
<td valign="top">

2406b

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Integration of SAP Datasphere and SAP Intelligent Clinical Supply Management with SAP Cloud Transport Management

</td>
<td valign="top">

You can now use SAP Cloud Transport Management to transport SAP Datasphere content and configuration settings of SAP Intelligent Clinical Supply Management.

See:

-   [Supported Content Types](supported-content-types-8961dcb.md#loio8961dcb3edc84a76b84b29565833067b)
-   [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-07-03

</td>
<td valign="top">

2024-07-03

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

If you are using SAP Cloud Transport Management as part of SAP Build Code: New *build-code* subscription plan available for SAP Cloud Transport Management.

</td>
<td valign="top">

To subscribe or to update to the *build-code* subscription plan from your current SAP Cloud Transport Management subscription, use the SAP Build Code booster.

See:

-   SAP Build Code documentation: [Initial Setup](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/07698d7c31284e4db370acdf017cfd14.html?version=SHIP)
-   [Subscribing to Cloud Transport Management](10-initial-setup/subscribing-to-cloud-transport-management-7fe10fc.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-06-06

</td>
<td valign="top">

2024-06-06

</td>
<td valign="top">

2406a

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Archiving of transport action logs

</td>
<td valign="top">

SAP Cloud Transport Management now periodically runs archiving jobs on transport action logs. It takes the transport action logs of a defined time interval, moves them to an archive file in a secondary storage, and then removes them from the database. You can configure the archiving settings according to your requirements.

See:

-   [Transport Action Logs](transport-action-logs-86319ed.md)
-   [Configure Archiving Settings of Transport Actions](configure-archiving-settings-of-transport-actions-0507a06.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-06-06

</td>
<td valign="top">

2024-06-06

</td>
<td valign="top">

2406a

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Direct connection between SAP Cloud Transport Management and SAP Cloud ALM.

</td>
<td valign="top">

You can now directly connect an SAP Cloud Transport Management service instance subscribed in your SAP BTP Global Account to SAP Cloud ALM.

If you've subscribed to several SAP Cloud Transport Management service instances, it's possible to connect all of them to the same SAP Cloud ALM.

To use the direct connection, you need to reconfigure the destination to SAP Cloud Transport Management used for SAP Cloud ALM.

See:

-   SAP Cloud ALM documentation on SAP Help Portal: [Enabling Transport Management → SAP Cloud Transport Management Service](https://help.sap.com/docs/CloudALM/08879d094f3b4de3ac67832f4a56a6de/8b4af2f9c2df4a1797dd812b814f36a5.html?locale=en-US)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-05-22

</td>
<td valign="top">

2024-05-22

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP Cloud Transport Management now supports the import of all and selected transport requests in an import queue for imports of references of type *BTP ABAP*. For the import of a selected transport request, a special logic has been introduced \(*Import Upto*\), which always imports a selected transport request together with the previous transport requests in the import queue.

</td>
<td valign="top">

To enable the import of all transport requests of type *BTP ABAP*, SAP Cloud Transport Management now supports the `MANAGE_SOFTWARE_COMPONENTS` API of SAP BTP ABAP environment with the communication scenario `SAP_COM_0948`. Previously, the `MANAGE_GIT_REPOSITORIES` API and `SAP_COM_0510` was used. With the new communication scenario, the `SAP_COM_0510` scenario was deprecated.

To leverage the functions of the new API, reconfigure the destination in SAP BTP ABAP environment pointing to SAP Cloud Transport Management using the new URL, user, and password taken from the new communication scenario.

Already configured destinations continue to work with the current limitations \(import of individual requests\) for the duration of the deprecation phase. However, we recommend that you already plan to transition to the new communication scenario.

See:

-   [Creating Destinations for Deployment of References of SAP BTP, ABAP Environment](20-configure-landscape/creating-destinations-for-deployment-of-references-of-sap-btp-abap-environment-3014453.md)
-   [Import Transport Requests](30-using-import-queue/import-transport-requests-d2005d5.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-05-22

</td>
<td valign="top">

2024-05-22

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

New events:

-   *TmsStorageQuotaUsage*
-   *TmsNodeImportJobDeactivated*



</td>
<td valign="top">

You can configure SAP Alert Notification Service to send notifications for actions started in SAP Cloud Transport Management. The following new events are available for configuration:

-   *TmsStorageQuotaUsage*:

    Receive a notification when the storage quota in your subscription has increased over the warning threshold of 85%.

-   *TmsNodeImportJobDeactivated*

    Receive a notification when an import scheduler is deactivated because too many imports have failed.


See:

-   Documentation: [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md)
-   Blog post: [Receive a notification when your storage quota of SAP Cloud Transport Management passes 85%](https://community.sap.com/t5/technology-blogs-by-sap/receive-a-notification-when-your-storage-quota-of-sap-cloud-transport/ba-p/13674963)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-04-12

</td>
<td valign="top">

2024-04-12

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

New transport node classification: Virtual node

</td>
<td valign="top">

You can now create virtual transport nodes that don't refer to a physical source or target. They can serve specific purposes, for example they can be used as placeholders to support uneven landscapes in hybrid change management scenarios, or to collect transport requests and forward them to a set of connected nodes. Transport requests that are imported into virtual nodes result in a *Skipped* status.

See: [About Transport Nodes](20-configure-landscape/about-transport-nodes-7cd4a78.md)

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-03-14

</td>
<td valign="top">

2024-03-14

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Cloud Transport Management 

</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

The existing documentation was enhanced.

</td>
<td valign="top">

A sample configuration of a destination to SAP Cloud Transport Management was added.

See: [Example: Destination to SAP Cloud Transport Management](20-configure-landscape/create-destinations-to-sap-cloud-transport-management-service-795f733.md#loio75fe5d4b4fa3492c87ef6be32ea0b819)

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Announcement

</td>
<td valign="top">

Application Development and Integration

</td>
<td valign="top">

Not applicable

</td>
<td valign="top">

SAP Cloud Transport Management

</td>
<td valign="top">

2024-03-14

</td>
<td valign="top">

2024-03-14

</td>
<td valign="top">

 

</td>
</tr>
</table>

