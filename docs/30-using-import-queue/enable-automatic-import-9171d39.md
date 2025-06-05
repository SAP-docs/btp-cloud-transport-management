<!-- loio9171d39a8a0e4208ab4c8f8ae96a0d4f -->

# Enable Automatic Import

To enable immediate imports of transport requests as soon as they enter a new queue, you can enable the automatic import in the import queue of a transport node.



<a name="loio9171d39a8a0e4208ab4c8f8ae96a0d4f__prereq_xgl_yn5_z2c"/>

## Prerequisites

-   You have one of the roles *Administrator* or *TransportOperator* assigned to your user. For more information, see [Security](../60-security/security-51939a4.md).

-   You are in the import queue of the transport node where you want to enable the automatic import. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).

-   The import isn't disabled in the transport node. You can enable the automatic import even if the import is disabled, but as long as the import is disabled, no automatic import takes place in the transport node.




## Context

By default, system administration manually imports transport requests into transport nodes. You can configure the transport node to automatically import transport requests as soon as they enter an import queue. Automatic imports simplify the process, ensure timely and consistent processing of transport requests, and eliminate the need for manual intervention.

> ### Caution:  
> When you enable automatic import, all *importable* transport requests in the import queue are immediately imported. These are transports in one of the following statuses: *Initial*, *Fatal*, or *Repeatable*.



## Procedure

1.  In the import queue of a transport node, choose *Enable Automatic Import*.

2.  Confirm that you want to enable the import.




<a name="loio9171d39a8a0e4208ab4c8f8ae96a0d4f__result_i4j_v45_z2c"/>

## Results

An enabled automatic import has the following effects:

-   An *AUTOMATIC IMPORT ENABLED* label in the transport node's header area indicates that automatic import is enabled in this node.

    > ### Note:  
    > If the import is disabled in the transport node, the label isn't shown.
    > 
    > For more information, see [Disable the Import](disable-the-import-f810a35.md).

-   If *importable* transport requests are already in the import queue, they're imported immediately.

-   The next time a new transport request is added to the import queue, it's automatically imported in the background as an *Import All* action. This means that any transport requests that previously failed to import are retried when a new request enters the import queue. To see the status update, refresh the screen.

-   You can no longer manually import transport requests into this queue.

-   The *Enable Automatic Import* button turns into an *Disable Automatic Import* button.

    To disable the automatic import, choose *Disable Automatic Import*.

-   If an import schedule existed for the import queue, it's deactivated.

    To run scheduled imports alongside automatic imports, reactivate the deactivated scheduled imports, or activate new ones.

-   The action is logged in the landscape action logs as *Automatic Import Enabled* with the value *true*. In the *Log of Action*, the user of the action is `CTMS_APPLICATION`.

-   In the *Landscape Visualization*, when you click on the corresponding transport node, the *Import Automatically* property is displayed with the value *Yes*.

