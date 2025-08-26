<!-- loio2ef725c1bc784490bc13f4f5d551a7d1 -->

# Delete Transport Requests

You can delete transport requests from all import queues in your tenant.



<a name="loio2ef725c1bc784490bc13f4f5d551a7d1__prereq_vxq_2st_xxb"/>

## Prerequisites

-   You have at least the authorization of the *TransportOperator* role for all the nodes that exist in your tenant. For more information, see [Security](../60-security/security-51939a4.md).
-   You are in the transport requests overview. For more information, see [Managing Transport Requests](managing-transport-requests-d088caa.md).
-   There are transport requests that you want to delete centrally from all import queues in your tenant.



## Context

This mass deletion function allows you to reduce your storage consumption for files that were uploaded to SAP Cloud Transport Management and that you no longer need. When you delete a transport request, the corresponding file attached to the request is also immediately deleted from the internal storage. This reduces your tenant's storage quota consumption.

> ### Caution:  
> You cannot restore deleted transport requests.



## Procedure

1.  In the transport requests overview, select the transport requests that you want to delete.

2.  On the subsequent dialog box, confirm your selection.




<a name="loio2ef725c1bc784490bc13f4f5d551a7d1__result_hgl_kzt_xxb"/>

## Results

The selected transport requests are deleted in all import queues in your subaccount or tenant. The files attached to the transport requests are also deleleted.

**Related Information**  


[Background Information: Storage Capacity](../50-administration/background-information-storage-capacity-e8d5187.md "The storage capacity for files uploaded to SAP Cloud Transport Management service is limited for each subscription.")

