<!-- loioe4e92ed3a2e646e4b632a753bb8a030e -->

# Remove Transport Requests

You can remove selected transport requests from an import queue.



<a name="loioe4e92ed3a2e646e4b632a753bb8a030e__prereq_vjx_xpb_wxb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *TransportOperator* assigned to your role. For more information, see [Security](../60-security/security-51939a4.md).

-   You are in the import queue of the transport node where you want to remove transport requests. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Procedure

1.  In the import queue, select the transport requests that you want to remove, and choose *Remove*.

2.  On the subsequent dialog box, confirm your selection.




<a name="loioe4e92ed3a2e646e4b632a753bb8a030e__result_swt_kqb_wxb"/>

## Results

The transport requests are removed from the import queue. They get the final status *Deleted*. The content files attached to the transport requests are still part of the requests. The files continue to use storage in your SAP Cloud Transport Management subscription.

As long as the transport requests are still in progress in any import queue in the transport landscape, they remain in the import queue with the status *Deleted*. Once they are processed in all import queues and have reached a final status, the configured retention period applies. By default, this period is 30 days. After that period, an automatic cleanup job removes the files attached to the transport requests and sets their lifecycle status to *Archived*. Archived transport requests do not appear in import queues. You can find information about these requests in the transport request logs or the transport action logs.

When the transport request is removed from **all** import queues in the transport landscape, the automatic cleanup job deletes the attached files and sets the transport request to *Archived* **immediately** with the next cleanup run, regardless of the retention time.

For more information about automatic cleanup and retention time, see [Storage in SAP Cloud Transport Management: What To Know](../50-administration/storage-in-sap-cloud-transport-management-what-to-know-e8d5187.md).

> ### Note:  
> To remove a transport request from all related import queues, you can use the *Delete* function in the transport requests overview. For more information, see [Delete Transport Requests](../40-using-request-overview/delete-transport-requests-2ef725c.md).

