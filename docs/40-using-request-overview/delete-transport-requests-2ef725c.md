<!-- loio2ef725c1bc784490bc13f4f5d551a7d1 -->

# Delete Transport Requests

You can delete transport requests from all import queues in your SAP Cloud Transport Management subscription.



<a name="loio2ef725c1bc784490bc13f4f5d551a7d1__prereq_vxq_2st_xxb"/>

## Prerequisites

-   You have at least the authorization of the *TransportOperator* role for all the nodes that exist in your subscription. For more information, see [Security](../60-security/security-51939a4.md).
-   You are in the transport requests overview. For more information, see [Managing Transport Requests](managing-transport-requests-d088caa.md).
-   There are transport requests that you want to delete centrally from all import queues in your transport landscape.



## Context

This mass deletion function allows you to reduce your storage consumption for files that were uploaded to SAP Cloud Transport Management and that you no longer need. When you delete transport requests, the files attached to the requests are immediately deleted from the internal storage and the requests are set to *Archived*. This reduces your tenant's storage quota consumption.

> ### Caution:  
> You can't restore deleted transport requests.



## Procedure

1.  In the transport requests overview, select the transport requests that you want to delete, and choose *Delete*.

2.  On the subsequent dialog box, confirm your selection.




<a name="loio2ef725c1bc784490bc13f4f5d551a7d1__result_hgl_kzt_xxb"/>

## Results

The selected transport requests are deleted in all import queues in your subaccount or tenant. The files attached to the transport requests are also deleted. The transport requests are set to the status *Archived*. The metadata of these transport requests is kept.

**Related Information**  


[Storage in SAP Cloud Transport Management: What To Know](../50-administration/storage-in-sap-cloud-transport-management-what-to-know-e8d5187.md "Storage management in SAP Cloud Transport Management involves fixed quotas, file size limits, and automatic cleanup based on configurable retention times to avoid running out of space.")

