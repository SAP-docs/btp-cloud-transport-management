<!-- loio85b6ac3c2925448c86bcd04f0da6678e -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# What's New for SAP Cloud Transport Management





**2025 - 2026**


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
<th valign="top">

Scope

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

Removal of the 100 MTA import limit for queues containing Cloud Foundry–dependent MTAs

</td>
<td valign="top">

The limit of 100 MTAs per import operation no longer applies when the queue includes a Cloud Foundry runtime-dependent MTA. You don't need to change any configuration.

The corresponding restriction was removed from the [Import Transport Requests](30-using-import-queue/import-transport-requests-d2005d5.md) topic.

</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

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

2026-04-20

</td>
<td valign="top">

2026-04-18

</td>
<td valign="top">

2603b

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

New API endpoints for Cloud Transport Management API

</td>
<td valign="top">

The Cloud Transport Management API version was updated from 2.2 to 2.3.1 and enhanced. Version 2.3.1 contains the following new endpoints:

-   [GET /nodes/\{nodeId\}/transportRequests/\{transportRequestId\}](https://api.sap.com/api/TMS_v2/path/NODE_TR_GET_V2)
-   [GET /transportRequests/\{transportRequestId\}/tracking](https://api.sap.com/api/TMS_v2/path/TR_TRACKING_GET_V2)

See also:

-   [Integration of SAP Cloud Transport Management Using APIs](70-integrations/extended-integration-scenarios-7e966f7.md#loiob608919f90c546d59876b8b765c01511)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

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

2026-04-18

</td>
<td valign="top">

2026-04-18

</td>
<td valign="top">

2603b

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

Closer integration of SAP Alert Notification Service and SAP Cloud Transport Management.

</td>
<td valign="top">

SAP Cloud Transport Management now uses SAP Alert Notification Service as a trusted internal service. This reduces the configuration efforts by eliminating the need to configure a destination.

You can continue to use any existing destination-based configuration. However, that integration is deprecated and will be removed from SAP Cloud Transport Management in Q4 2026.

**Existing users**: If you previously enabled the *Perform Notification* checkbox for specific transport nodes and haven't restricted notifications using `tags.nodeName` or `tags.nodeId` conditions in SAP Alert Notification service, you will receive more notifications than expected. For more information about how to restrict notifications, see [Migrating to SAP Alert Notification Service As a Trusted Internal Service](migrating-to-sap-alert-notification-service-as-a-trusted-internal-service-0914d2c.md).

See:

-   [Migrating to SAP Alert Notification Service As a Trusted Internal Service](migrating-to-sap-alert-notification-service-as-a-trusted-internal-service-0914d2c.md)
-   [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

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

2026-04-18

</td>
<td valign="top">

2026-04-18

</td>
<td valign="top">

2603b

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

New *Service Plans and Metering* topic

</td>
<td valign="top">

The topic contains information about the service plans needed to understand the relationship between the content of the Discovery Center and the content in SAP BTP Cockpit.

See:

-   [Service Plans and Metering](service-plans-and-metering-17c102d.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

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

2026-04-18

</td>
<td valign="top">

2026-04-18

</td>
<td valign="top">



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

Configure User Data Anonymization Settings

</td>
<td valign="top">

User data anonymization enables you to customize retention periods and anonymization schedules for user data displayed and logged in SAP Cloud Transport Management. This feature helps ensure compliance with data privacy regulations by automatically anonymizing user data according to your organization’s requirements.

See:

-   [Configure User Data Anonymization Settings](50-administration/configure-user-data-anonymization-settings-f3c0a3b.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

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

2026-03-06

</td>
<td valign="top">

2026-03-06

</td>
<td valign="top">

2602a

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

Documentation Enhancements

</td>
<td valign="top">

-   New topic: [Configuring File Retention Time](50-administration/configuring-file-retention-time-9969d8d.md)
-   New topic about using Mutual Transport Layer Security \(mTLS\) for authentication for destinations for deployment of application content transported in an application-specific format: [Destination for Deployment of Application Content Transported in an Application-Specific Format Using mTLS Authentication](20-configure-landscape/destination-for-deployment-of-application-content-transported-in-an-application-specific-72bfde3.md)
-   Restructured and renamed topic: [Storage in SAP Cloud Transport Management: What To Know](50-administration/storage-in-sap-cloud-transport-management-what-to-know-e8d5187.md) \(previously called: *Background Information: Storage Capacity*\)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

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

2026-03-06

</td>
<td valign="top">

2026-03-06

</td>
<td valign="top">



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

Deprecation of route used in Cloud Foundry destinations using SAP Cloud Deployment service 

</td>
<td valign="top">

The legacy route <code>https://deploy-service.cfapps.<i class="varname">&lt;domain&gt;</i></code> is deprecated and will be removed in Q4/2026.

<code><i class="varname">&lt;domain&gt;</i></code> is derived from the Cloud Foundry API endpoint, which can be found in the SAP BTP cockpit of your subaccount under *Overview*.

**Action**: If you have destinations pointing to the legacy route, update all Cloud Foundry destinations using SAP Cloud Deployment service to <code>https://deploy-service.cf.<i class="varname">&lt;domain&gt;</i></code> by replacing `cfapps` with `cf`.

A warning message on the SAP Cloud Transport Management UI informs you about the deprecation. You can display all affected destinations and navigate to the destinations editor to update them.

See:

-   [3695458](https://me.sap.com/notes/3695458) - *Removal of Legacy URL for SAP Cloud Deployment Service in Cloud Foundry*
-   [Creating Destinations Using SAP Cloud Deployment Service with OAuth2Password Authentication](20-configure-landscape/creating-destinations-using-sap-cloud-deployment-service-with-oauth2password-authenticati-a26a721.md)
-   [Creating Destinations Using SAP Cloud Deployment Service with Basic Authentication](20-configure-landscape/creating-destinations-using-sap-cloud-deployment-service-with-basic-authentication-6b7c9d8.md)



</td>
<td valign="top">

Required

</td>
<td valign="top">

Deprecated

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

2026-03-06

</td>
<td valign="top">

2026-03-06

</td>
<td valign="top">

 

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

Modifiable transport requests

</td>
<td valign="top">

UI enhancements to the modifiable transport requests function.

New blog post announcing modifiable transport requests.

See:

-   [Processing Modifiable Transport Requests](40-using-request-overview/processing-modifiable-transport-requests-b541b09.md)
-   Blog post: [Modifiable Transport Requests now also for your SAP cloud changes](https://community.sap.com/t5/technology-blog-posts-by-sap/modifiable-transport-requests-now-also-for-your-sap-cloud-changes/ba-p/14194823)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

Changed

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

2025-09-04

</td>
<td valign="top">

2025-09-04

</td>
<td valign="top">

2508b

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

Modifiable transport requests

</td>
<td valign="top">

You can create transport requests that are initially empty. You can use them to add multiple files and test the deployment of the files. After successful testing, you can release the transport requests. As a result, they become available for import.

See:

-   [Processing Modifiable Transport Requests](40-using-request-overview/processing-modifiable-transport-requests-b541b09.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

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

2025-08-26

</td>
<td valign="top">

2025-08-26

</td>
<td valign="top">

2508a

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

New *ImportSelectedOperator* role

</td>
<td valign="top">

Use this role if you want to enable users to import selected transport requests in an import queue, but not all requests.

See:

-   [Security](60-security/security-51939a4.md)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

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

2025-08-26

</td>
<td valign="top">

2025-08-26

</td>
<td valign="top">

2508a

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

Integration of SAP Asset Performance Management with SAP Cloud Transport Management 

</td>
<td valign="top">

You can now use SAP Cloud Transport Management to transport SAP Asset Performance management content.

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

New

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

2025-08-26

</td>
<td valign="top">

2025-08-26

</td>
<td valign="top">

 

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

SAP Cloud Transport Management service catalog \(`ctms-sapcp`\) available in Automation Pilot 

</td>
<td valign="top">

You can now use Automation Pilot to manage transport nodes, routes, and transport requests of SAP Cloud Transport Management.

See:

-   [Integrations Into Other Cloud Services, Development, and Change Management Processes](70-integrations/extended-integration-scenarios-7e966f7.md#loio1b3c6637adb54d4bbb1828f911bb9547)



</td>
<td valign="top">

Info only

</td>
<td valign="top">

General Availability

</td>
<td valign="top">

New

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

2025-08-26

</td>
<td valign="top">

2025-07-10

</td>
<td valign="top">

 

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

UI changes

</td>
<td valign="top">

Landscape Visualization:

-   Introduction of an overview graph for navigation in large transport landscapes, as well as options to adjust the orientation and placement of nodes.

-   Highlighting of transport nodes using icons and color to indicate the overall import status of a node and quick overview of important configuration settings.

-   Selecting a transport node or route now allows you to open a details popover.

-   Editing a node or route was moved from the icon bar to the popover.


See:

-   [Using the Landscape Visualization](using-the-landscape-visualization-9fea4f2.md)



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

2025-07-23

</td>
<td valign="top">

2025-07-23

</td>
<td valign="top">

2507a

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

Data protection and privacy information of the service can now be accessed directly from the UI of the service.

</td>
<td valign="top">

From the User Profile dropdown menu, you can now directly open the data protection and privacy information in the SAP Cloud Transport Management documentation on SAP Help Portal.

See:

-   [SAP Cloud Transport Management Home Screen](sap-cloud-transport-management-home-screen-9ac7880.md). In the topic, select the Title Bar, and then scroll down to the *User Profile* section.



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

2025-07-23

</td>
<td valign="top">

2025-07-23

</td>
<td valign="top">

2507a

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

Integration of Joule Studio with SAP Cloud Transport Management 

</td>
<td valign="top">

You can now use SAP Cloud Transport Management to transport Joule Studio projects.

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

2025-07-23

</td>
<td valign="top">

2025-07-02

</td>
<td valign="top">

 

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

New *build-runtime* application service plan available.

</td>
<td valign="top">

You can use the *build-runtime* service plan when you use SAP Cloud Transport Management as part of a service from the SAP Build ecosystem.

See:

-   [Subscribing to Cloud Transport Management](10-initial-setup/subscribing-to-cloud-transport-management-7fe10fc.md)
-   [Updating the Service Plan](50-administration/updating-the-service-plan-1717e87.md)



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

2025-07-02

</td>
<td valign="top">

2025-07-02

</td>
<td valign="top">

2506a

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

SAP Cloud Transport Management service available on new data centers.

</td>
<td valign="top">

SAP Cloud Transport Management service is now also available in the following regions:

-   Amazon Web Services in the US West \(Oregon\) region
-   Azure in the Canada Central \(Toronto\) region

See:

-   [SAP Cloud Transport Management in SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management/?region=all&tab=service_plan)
-   [Regions and API Endpoints Available for the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/f344a57233d34199b2123b9620d0bb41.html)



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

2025-06-06

</td>
<td valign="top">

2025-06-06

</td>
<td valign="top">

 

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

Smaller UI changes

</td>
<td valign="top">

**Title Bar**

-   Some functions that were previously found under the logon e-mail address are now available under the new :gear: button.

-   The logon e-mail address was replaced by a *User Profile* icon.


See:

-   [SAP Cloud Transport Management Home Screen](sap-cloud-transport-management-home-screen-9ac7880.md)

**Import Queue**

-   New *Node Details* tab displaying general information about a node as well as information about import scheduling.

-   The *Disable Import* and *Enable Automatic Import* buttons were moved to the top right of the UI.


See:

-   [Using the Import Queue](30-using-import-queue/using-the-import-queue-3c4b6f3.md)



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

2025-06-06

</td>
<td valign="top">

2025-06-06

</td>
<td valign="top">

2505a

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

New tutorial available about transporting Mobile Development Kit apps using SAP Content Agent UI and SAP Cloud Transport Management 

</td>
<td valign="top">

See:

-   Link to tutorial in [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md)
-   Tutorial: [Transport Mobile Development Kit \(MDK\) apps using SAP Content Agent UI](https://developers.sap.com/tutorials/btp-content-agent-transport-mobile-apps.html)



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

2025-06-06

</td>
<td valign="top">

2025-06-06

</td>
<td valign="top">

 

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

New feedback button is available in the title bar of SAP Cloud Transport Management 

</td>
<td valign="top">

Use the feedback button to share anonymous feedback about SAP Cloud Transport Management.

See:

-   [SAP Cloud Transport Management Home Screen](sap-cloud-transport-management-home-screen-9ac7880.md)



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

2025-05-16

</td>
<td valign="top">

2025-05-16

</td>
<td valign="top">

2504b

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

SAP Cloud Transport Management service available on new data centers.

</td>
<td valign="top">

SAP Cloud Transport Management service is now also available in the following regions:

-   Amazon Web Services in the US West \(Oregon\) region
-   Azure in the Canada Central \(Toronto\) region

See:

-   [SAP Cloud Transport Management in SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management/?region=all&tab=service_plan)
-   [Regions and API Endpoints Available for the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/f344a57233d34199b2123b9620d0bb41.html)



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

2025-05-16

</td>
<td valign="top">

2025-05-16

</td>
<td valign="top">

 

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

Enhancements to the *Create Node* dialog.

</td>
<td valign="top">

When you create or edit a transport node, the destination selection box now displays both the name and description of each destination. The description makes it easier to choose the appropriate destination.

See:

-   [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md)



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

2025-05-06

</td>
<td valign="top">

2025-05-06

</td>
<td valign="top">

2504a

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

Revamp of the Landscape Action Logs

</td>
<td valign="top">

The landscape action logs are now displayed in a more flexible table layout with extensive filter options, detail display, and links to the affected objects.

See:

-   [Landscape Action Logs](landscape-action-logs-7b630db.md)



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

2025-05-06

</td>
<td valign="top">

2025-05-06

</td>
<td valign="top">

2504a

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

New function in the import queue: Immediately start imports of transport requests as soon as they enter an import queue.

</td>
<td valign="top">

This function enhances automation, and simplifies the import process.

See:

-   [Enable Automatic Import](30-using-import-queue/enable-automatic-import-9171d39.md)



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

2025-05-06

</td>
<td valign="top">

2025-05-06

</td>
<td valign="top">

2504a

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

New tutorial available on SAP Learning: *Transport SAP Integration Suite Content using SAP Cloud Transport Management service and SAP Content Agent service* 

</td>
<td valign="top">

If you want to transport SAP Integration Suite content using SAP Cloud Transport Management and use SAP Content Agent both for the export of the content in a source subaccount and for the import of the content in a target subaccount, use this tutorial to learn about the required configuration steps.

See:

-   [Transport SAP Integration Suite Content using SAP Cloud Transport Management service and SAP Content Agent service](https://developers.sap.com/tutorials/btp-transport-management-cpi-01-use-case.html)



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

2025-04-17

</td>
<td valign="top">

2025-04-17

</td>
<td valign="top">

 

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

SAP Cloud Transport Management service available on new data centers.

</td>
<td valign="top">

SAP Cloud Transport Management service is now also available in the following regions:

-   Amazon Web Services in the Brazil \(São Paulo\) region
-   Google Cloud in the Japan \(Osaka\) region
-   Google Cloud in the Australia Southeast \(Sydney\) region
-   Google Cloud in the Europe \(Frankfurt\) region

See:

-   [SAP Cloud Transport Management in SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management/?region=all&tab=service_plan)
-   [Regions and API Endpoints Available for the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/f344a57233d34199b2123b9620d0bb41.html)



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

2025-04-03

</td>
<td valign="top">

2025-04-03

</td>
<td valign="top">

 

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

New troubleshooting topic containing information about issues that can arise when transporting Multitarget Applications \(MTAs\) in Cloud Foundry.

</td>
<td valign="top">

See:

-   [Troubleshooting Issues when Transporting Multitarget Applications \(MTAs\)](troubleshooting-issues-when-transporting-multitarget-applications-mtas-3f7a9bc.md)



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

2025-04-03

</td>
<td valign="top">

2025-04-03

</td>
<td valign="top">

 

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

SAP Cloud Transport Management service available on new data centers.

</td>
<td valign="top">

SAP Cloud Transport Management service is now also available in the following regions:

-   Google Cloud in the KSA \(Dammam\) region
-   Google Cloud in the Japan \(Tokyo\) region

See:

-   [SAP Cloud Transport Management in SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management/?region=all&tab=service_plan)
-   [Regions and API Endpoints Available for the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/f344a57233d34199b2123b9620d0bb41.html)



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

2025-04-03

</td>
<td valign="top">

2025-03-07

</td>
<td valign="top">

2502a

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

Option to download only the selected \(filtered\) transport action logs.

</td>
<td valign="top">

You can now download only selected \(filtered\) transport action logs as `.csv` or plain text \(`.txt`\) files. Previously, the downloaded `.zip` file contained all transport actions, regardless of the filters.

See:

-   [Transport Action Logs](transport-action-logs-86319ed.md)



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

2025-03-07

</td>
<td valign="top">

2025-03-07

</td>
<td valign="top">

2502a

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

Option to download transport action logs in a `.csv` file format.

</td>
<td valign="top">

You can now download transport action logs as `.csv` files, either individually or all at once. This structured format simplifies data analysis and enhances audit compliance.

See:

-   [Transport Action Logs](transport-action-logs-86319ed.md)



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

2025-01-23

</td>
<td valign="top">

2025-01-23

</td>
<td valign="top">

2413b

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

Introduction of tags in SAP Cloud Transport Management 

</td>
<td valign="top">

You can now tag transport nodes, allowing you to group them based on the assigned tags. You can use tags to add additional information, such as project details, or system characteristics. The tags appear as labels on the *Transport Nodes* screen, providing more information at a glance beyond just the description field.

See:

-   [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md)



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

2025-01-23

</td>
<td valign="top">

2025-01-23

</td>
<td valign="top">

2413b

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

Option to download MTA operation logs directly from the *Log of Transport Request* 

</td>
<td valign="top">

For MTA deployment on Cloud Foundry, the log of the transport request now contains additional information about how to download the corresponding MTA operation logs, and includes a link to download the logs of the deploy operation directly from the SAP Cloud Transport Management user interface. Like this, you can obtain the MTA logs without using the Cloud Foundry command- line interface \(`cf cli`\).

See:

-   [Options to Display Information about Transport Requests](30-using-import-queue/options-to-display-information-about-transport-requests-a90d808.md)



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

2025-01-23

</td>
<td valign="top">

2025-01-23

</td>
<td valign="top">

2413b

</td>
<td valign="top">

 

</td>
</tr>
</table>

-   **[2024 SAP Cloud Transport Management \(Archive\)](2024-sap-cloud-transport-management-archive-8af3915.md)**  


