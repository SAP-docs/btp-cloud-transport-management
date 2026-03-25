<!-- loioe8d5187d1352430aacbe04d4f3b0eb62 -->

# Storage in SAP Cloud Transport Management: What To Know

Storage management in SAP Cloud Transport Management involves fixed quotas, file size limits, and automatic cleanup based on configurable retention times to avoid running out of space.



## Overview

Each subscription to SAP Cloud Transport Management has a fixed storage quota for files that are uploaded to the service as part of transport requests. The size of a single uploaded file is limited by your service plan. To ensure that the storage quota isn't easily reached, files are automatically deleted by an automatic cleanup job after a configurable retention time, when they’re no longer in progress in any import queue in your transport landscape.



## Service Plan Limits

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

30 days \(default\)

You can set 1 - 30 days.

</td>
</tr>
<tr>
<td valign="top">

Free

</td>
<td valign="top">

500 MB

</td>
<td valign="top">

500 MB

</td>
<td valign="top">

7 days \(default\)

You can set 1 - 7 days.

</td>
</tr>
</table>

> ### Note:  
> If SAP Cloud Transport Management runs on SAP BTP, partner-managed edition in the China \(Shanghai\) or Government Cloud \(US\) regions, the storage capacity is as follows:
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
> 400 MB
> 
> </td>
> <td valign="top">
> 
> 30 days \(default\)
> 
> You can set 1 - 30 days.
> 
> </td>
> </tr>
> <tr>
> <td valign="top">
> 
> Free
> 
> </td>
> <td valign="top">
> 
> 500 MB
> 
> </td>
> <td valign="top">
> 
> 400 MB
> 
> </td>
> <td valign="top">
> 
> 7 days \(default\)
> 
> You can set 1 - 7 days.
> 
> </td>
> </tr>
> </table>

For more information about the service plans for SAP Cloud Transport Management, see [SAP Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-transport-management?tab=service_plan&region=all).



## How the Automatic Cleanup Works

The automatic cleanup removes physical files from transport requests that meet certain criteria based on import status and file retention settings. It keeps the transport request metadata and logs, and sets the transport requests to the lifecycle status *Archived*. The automatic cleanup runs daily.

Automatic deletion takes place, if a transport request meets the following criteria:

-   The transport request is no longer in progress in any import queue in the transport landscape. This means the import status is one of the following *final* states: *Deleted*, *Error*, *Skipped*, *Succeeded*, or *Warning*.

    > ### Note:  
    > Files in transport requests that are still in progress \(in an import status *Fatal*, *Initial*, *Repeatable*, or *Running*\) aren't deleted by the cleanup.

-   The last action on the transport request containing the file happened at least as many days ago as your retention setting \(for example, 30 days for *Standard* by default, 7 days for *Free* by default\).

    > ### Note:  
    > **Exception**: If the transport request has the status *Deleted* in all import queues \(set using the *Remove* button\), the attached files are deleted and the request is archived immediately at the next cleanup run, regardless of the retention time.




## Capacity Warnings and Blocking

-   When your space reaches 85% of its quota, a warning appears when you manually upload a file.

-   When your quota is reached, new uploads are blocked.




## How to Check Storage Usage and Configure File Retention Time

-   To check storage usage, use one of the following options:

    -   Click the dropdown next to your login e-mail and choose *My File Quota*.

    -   Open the *Storage Usage* section on the SAP Cloud Transport Management home screen.


-   To configure file retention time, follow these steps:

    1.  Click the dropdown next to your login e-mail and choose *File Retention Time*.
    2.  Set a value by clicking the bar or entering a number. The allowed range depends on your plan.




## Recommended Actions To Maintain Storage Space

-   **Set Up Alerts**

    Use SAP Alert Notification Service to notify you when your space reaches 85% of its quota.

    For more information, see [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](../receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md).

-   **Monitor and Reduce Usage**

    -   Regularly check storage usage in your account and keep plan limits in mind before uploading new files.

    -   To reduce the total file size, clean up your import queues using the following options:

        -   Import transport requests across all import queues of your transport landscape so they reach a final import status everywhere.

        -   Review all import queues to identify transport requests that are in a non-final status and that you no longer need.

            You can remove outdated or obsolete requests directly from the individual import queues. Once removed, a request gets the import status *Deleted*. As soon as a transport request is in a final status in all import queues, it becomes part of the automatic cleanup process. During the cleanup, all files associated with the transport requests are deleted, and the requests are set to *Archived*, while all metadata remains accessible.

            The same cleanup takes place when you use *Delete* in the transport request overview. This action sets the corresponding transport requests in the relevant import queues to *Deleted*. For more information, see [Delete Transport Requests](../40-using-request-overview/delete-transport-requests-2ef725c.md).


        > ### Note:  
        > Pay special attention to requests in status *Fatal*. The cleanup won't delete their files.


-   **Tune File Retention Time**

    To effectively balance the available storage with your operational requirements, set the file retention time based on your transport volume and data retention requirements. Consider the following points:

    -   High transport volume favors a shorter retention time to conserve space.

    -   Logs and transport requests that are still in progress are kept regardless of the retention settings. Decide whether you truly need older transport requests files or if log information is sufficient.



**Related Information**  


[SAP Cloud Transport Management Home Screen](../sap-cloud-transport-management-home-screen-9ac7880.md "On the home screen, you have an overview of the most commonly used functions of SAP Cloud Transport Management service with direct access. Using the navigation pane on the left side, you have access to all functions.")

