<!-- loio9e3ee9459f2a4d62a0d9ec7e17b821bb -->

# Auditing and Logging Information

Here you can find a list of the security events that are logged by SAP Cloud Transport Management service.



SAP Cloud Transport Management writes security-relevant events to the audit log. The service writes audit log messages of category *audit.security-events* in the following situations:

**Security events written in audit logs**


<table>
<tr>
<th valign="top">

Event grouping

</th>
<th valign="top">

What events are logged

</th>
<th valign="top">

How to identify related log events

</th>
<th valign="top">

Additional information

</th>
</tr>
<tr>
<td valign="top" rowspan="3">

General

</td>
<td valign="top">

SAP Cloud Transport Management runs a cleanup service at regular intervals to delete files in transport requests after a specific period of time. Cleanup service events are logged.

</td>
<td valign="top">

-   *Cleanup service runs*



</td>
<td valign="top">

For more information about the cleanup mechanism, see [Background Information: Storage Capacity](../50-administration/background-information-storage-capacity-e8d5187.md).

</td>
</tr>
<tr>
<td valign="top">

When an SAP Cloud Transport Management API is used, it is possible that a service endpoint is called without sufficient authorization. If the call fails, this event is logged.

</td>
<td valign="top">

-   *Authorization check for the scope *<scope-id\>* failed*



</td>
<td valign="top">

For more information about using the APIs of the service, see [Integration of SAP Cloud Transport Management Using APIs](../70-integrations/extended-integration-scenarios-7e966f7.md#loiob608919f90c546d59876b8b765c01511).

</td>
</tr>
<tr>
<td valign="top">

When the subscription of SAP Cloud Transport Management is updated to a new plan, this event is logged.

</td>
<td valign="top">

-   *Subscription plan was updated to "*<plan name\>*" for tenant *<tenant-id\>**
-   *Update of subscription plan to "*<plan name\>*" failed for tenant *<tenant-id\>**



</td>
<td valign="top">

For more information about the plans available for the service, see [SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management?service_plan=standard&region=all&tab=service_plan).

</td>
</tr>
</table>

**Related Information**  


[Audit Logging in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f92c86ab11f6474ea5579d839051c334.html)

[Audit Logging in the Neo Environment](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/02c39712c1064c96b37c1ea5bc9420dc.html)

