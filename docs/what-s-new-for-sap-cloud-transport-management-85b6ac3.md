<!-- loio85b6ac3c2925448c86bcd04f0da6678e -->

# What's New for SAP Cloud Transport Management





**2026**


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
</table>

-   **[2025 SAP Cloud Transport Management \(Archive\)](2025-sap-cloud-transport-management-archive-5de81f9.md)**  


