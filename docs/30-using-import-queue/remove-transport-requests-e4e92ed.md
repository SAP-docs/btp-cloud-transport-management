<!-- loioe4e92ed3a2e646e4b632a753bb8a030e -->

# Remove Transport Requests

You can remove selected transport requests from an import queue.



<a name="loioe4e92ed3a2e646e4b632a753bb8a030e__prereq_vjx_xpb_wxb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *TransportOperator* assigned to your role. For more information, see [Security](../60-security/security-51939a4.md).

-   You are in the import queue of the transport node where you want to remove transport requests. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Procedure

1.  In the import queue, select the transport requests that you want to remove.

2.  Choose *Remove*.




<a name="loioe4e92ed3a2e646e4b632a753bb8a030e__result_swt_kqb_wxb"/>

## Results

The transport request is removed from the import queue. It gets the status *Deleted*.

When the transport request is removed from all related import queues, the automatic cleanup mechanism of SAP Cloud Transport Management deletes the physical file attached to the transport request. For more information, see [Background Information: Storage Capacity](../50-administration/background-information-storage-capacity-e8d5187.md).

> ### Note:  
> To remove a transport request from all related import queues, you can use the *Delete* function in the transport requests overview. For more information, see [Delete Transport Requests](../40-using-request-overview/delete-transport-requests-2ef725c.md).

