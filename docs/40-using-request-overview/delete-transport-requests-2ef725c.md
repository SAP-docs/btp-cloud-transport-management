<!-- loio2ef725c1bc784490bc13f4f5d551a7d1 -->

# Delete Transport Requests

You can delete transport requests from all import queues in your tenant.



<a name="loio2ef725c1bc784490bc13f4f5d551a7d1__prereq_vxq_2st_xxb"/>

## Prerequisites

-   You have at least the authorization of the *TransportOperator* role for all the nodes that exist in your tenant. For more information, see [Security](../60-security/security-51939a4.md).
-   You are in the transport requests overview. For more information, see [Prerequisites for Using the Transport Requests Overview](prerequisites-for-using-the-transport-requests-overview-55f162d.md).
-   There are transport requests that you want to delete centrally from all import queues in your tenant.



## Context

This mass deletion function allows you to reduce your storage consumption for files that were uploaded to SAP Cloud Transport Management and that you no longer need. The physical deletion of files from your tenant is delayed and can take up to 24 hours. Marking transport requests for deletion will therefore not immediately reduce your tenant's storage quota consumption. For more information about the automatic cleanup mechanism of SAP Cloud Transport Management, see [Background Information: Storage Capacity](../50-administration/background-information-storage-capacity-e8d5187.md).

> ### Caution:  
> You cannot restore deleted transport requests.



## Procedure

1.  In the transport requests overview, select the transport requests that you want to delete.

2.  On the subsequent dialog box, confirm your selection.




<a name="loio2ef725c1bc784490bc13f4f5d551a7d1__result_hgl_kzt_xxb"/>

## Results

The selected transport requests are deleted in all import queues in your subaccount or tenant. The physical file of the transport request will be deleleted wih the next run of the autmatic cleanup mechanism.

