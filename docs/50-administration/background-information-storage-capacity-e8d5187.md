<!-- loioe8d5187d1352430aacbe04d4f3b0eb62 -->

# Background Information: Storage Capacity

The storage capacity for files uploaded to SAP Cloud Transport Management service is limited for each subscription.

The total capacity as well as the retention time of files that were uploaded to the service depends on the service plan you have for the service. Each individual file that is uploaded to SAP Cloud Transport Management can have a maximum size of 1 GB.

**Details of Service Plans**


<table>
<tr>
<th valign="top">

Service Plan

</th>
<th valign="top">

Total Capacity

</th>
<th valign="top">

Size Limit of Individual Files

</th>
<th valign="top">

Retention Time

</th>
</tr>
<tr>
<td valign="top">

Standard

</td>
<td valign="top">

50 GB

</td>
<td valign="top">

1 GB

</td>
<td valign="top">

30 days

</td>
</tr>
<tr>
<td valign="top">

Free

</td>
<td valign="top">

2 GB

</td>
<td valign="top">

1 GB

</td>
<td valign="top">

7 days

</td>
</tr>
</table>

> ### Note:  
> If SAP Cloud Transport Management is running on SAP BTP, partner-managed edition in the China \(Shanghai\) or Government Cloud \(US\) regions, the storage capacity is as follows.
> 
> 
> <table>
> <tr>
> <th valign="top">
> 
> Service Plan
> 
> </th>
> <th valign="top">
> 
> Total Capacity
> 
> </th>
> <th valign="top">
> 
> Size Limit of Individual Files
> 
> </th>
> <th valign="top">
> 
> Retention Time
> 
> </th>
> </tr>
> <tr>
> <td valign="top">
> 
> Standard
> 
> </td>
> <td valign="top">
> 
> 10 GB
> 
> </td>
> <td valign="top">
> 
> 0.4 GB
> 
> </td>
> <td valign="top">
> 
> 30 days
> 
> </td>
> </tr>
> </table>

For more information about the service plans for SAP Cloud Transport Management, see [SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management?tab=service_plan&region=all).

You can check how much of the storage capacity is already in use by selecting the dropdown arrow next to your user's email address, and choosing *My File Quota*, or in the *Storage Usage* section on the SAP Cloud Transport Management home screen.

To ensure that the maximum capacity isn't easily reached, the service has an automatic cleanup mechanism in place. The cleanup mechanism runs on a daily basis. All uploaded files in transport requests are automatically deleted after a specific retention time, depending on the service plan you have. Automatic deletion takes place, if the following criteria are met:

-   In all import queues in the transport landscape, the transport requests are in one of the following statuses:

    -   *Deleted*
    -   *Error*
    -   *Skipped*
    -   *Succeeded*
    -   *Warning*

    > ### Note:  
    > If a file is still part of a transport request in one of the statuses *Fatal*, *Initial*, *Repeatable*, or *Running*, the physical files aren't deleted.

-   The last action for this file was executed 30 days \(*Standard* plan\) / 7 days \(*Free* plan\) before the cleanup run.

    > ### Note:  
    > This criterion doesn't apply to files in transport requests that have the status *Deleted* in all import queues. A transport request gets this status using the *Remove* button. This status allows an automatic deletion of files in such transport requests immediately when the cleanup mechanism detects them.


The metadata of the transport request isn't deleted, only the file. The file is also automatically deleted, if the corresponding transport request is deleted.

When you've reached at least 85% of the storage capacity in your space, and you're trying to upload a new file to SAP Cloud Transport Management, a warning message is displayed.

When you've reached the maximum storage capacity, no files can be uploaded to the service, and no quick solution is possible for the issue, because you can't manually delete files.

> ### Recommendation:  
> To avoid running out of space, we recommend that you implement the following measures:
> 
> -   Configure SAP Alert Notification Service to send notifications when you've reached at least 85% of the storage capacity in your space. For more information, see [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](../receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md).
> 
> -   Regularly track the storage usage in your account. In addition, keep in mind the total storage capacity of your subscription whenever you upload files. To reduce the total file size, regularly clean up the import queues in your transport landscape. You can do this either by importing the transport requests containing the same file in all import queues of your transport landscape, or by removing outdated and obsolete transport requests from all import queues. Especially pay attention to transport requests in status *Fatal*, because the cleanup mechanism doesn't automatically delete them.

