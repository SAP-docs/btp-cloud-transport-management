<!-- loio630fae7f8308464ea4cb38b10d7d59a4 -->

# Forward Transport Requests

If the *Forward Mode* of a transport node is set to the value *Manual*, you can manually forward transport requests in this node to target transport nodes.



<a name="loio630fae7f8308464ea4cb38b10d7d59a4__prereq_tx4_wn1_fxb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *TransportOperator* assigned to your role. For more information, see [Security](../60-security/security-51939a4.md).

-   You are in the import queue of the transport node where you want to forward transport requests. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).
-   The *Forward Mode* of the transport node is set to the value *Manual*. For more information, see [Create Transport Nodes](../20-configure-landscape/create-transport-nodes-f71a4d5.md).
-   The archive that is attached to the transport request isn’t deleted.

    Forwarding transport requests is only possible as long as the archive exists. The default retention period of archives depends on the service plan that you use for SAP Cloud Transport Management. For more information, see [Background Information: Storage Capacity](../50-administration/background-information-storage-capacity-e8d5187.md).

-   The transport requests that you want to forward are in one of the statuses *Error*, *Skipped*, *Succeeded*, or *Warning*.



## Context

If the forward mode of a transport node is *Manual*, no automatic forwarding takes place. Forwarding takes place into all target transport nodes according to the transport routes defined for the node where the import is started. You can manually select individual transport requests in the current import queue that you want to forward.

For transport nodes of content type *BTP ABAP*: You can forward transport requests only according to the *Import upto* logic. This means the selected transport request is forwared along with all previous requests.



## Procedure

1.  In the import queue, select one or multiple transport requests that you want to forward.

    The transport requests are forwarded in the same order in which you selected them. This allows you to influence the order in which the transport requests are placed in the target import queue.

    > ### Note:  
    > For content type *BTP ABAP*: Forwarding individual transport requests isn't supported. When you select a request, its previous requests are also selected and forwarded.

2.  Choose *Forward*.




<a name="loio630fae7f8308464ea4cb38b10d7d59a4__result_ybb_w41_fxb"/>

## Results

The forwarded transport requests are added to the end of the import queues of the target transport nodes. If the forwarded transport requests are already part of the import queue of the target node, they’re moved to the end of this import queue. The status of a moved transport request changes as follows:

-   *Initial* remains *Initial*.
-   *Deleted*, *Error*, *Fatal*, *Skipped*, *Succeeded*, and *Warning* change to *Repeatable*.
-   *Repeatable* remains *Repeatable*.

