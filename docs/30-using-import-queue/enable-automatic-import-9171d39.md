<!-- loio9171d39a8a0e4208ab4c8f8ae96a0d4f -->

# Enable Automatic Import

To enable immediate imports of transport requests as soon as they enter a new queue, you can enable the automatic import for a transport node.



<a name="loio9171d39a8a0e4208ab4c8f8ae96a0d4f__prereq_xgl_yn5_z2c"/>

## Prerequisites

-   You have one of the roles *Administrator* or *TransportOperator* assigned to your user. For more information, see [Security](../60-security/security-51939a4.md).

-   You are in the transport node where you want to enable the automatic import. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).

-   The import isn't disabled in the transport node. You can enable the automatic import even if the import is disabled, but as long as the import is disabled, no automatic import takes place in the transport node.




## Context

By default, system administration manually imports transport requests into transport nodes. You can configure the transport node to automatically import transport requests as soon as they enter an import queue. Automatic imports simplify the process, ensure timely and consistent processing of transport requests, and eliminate the need for manual intervention.

> ### Caution:  
> When you enable automatic import, all *importable* transport requests in the import queue are immediately imported. These are transports in one of the following statuses: *Initial*, *Fatal*, or *Repeatable*.



## Procedure

1.  In the transport node, choose *Import Settings* \> *Enable Automatic Import*.

2.  Confirm that you want to enable the import.




<a name="loio9171d39a8a0e4208ab4c8f8ae96a0d4f__result_i4j_v45_z2c"/>

## Results

An enabled automatic import has the following effects:

-   If importable transport requests are already in the import queue, they're imported immediately.

-   The next time a new transport request is added to the import queue, it's automatically imported in the background as an *Import All* action. This means that any transport requests that previously failed to import are retried when a new request enters the import queue. To see the status update, refresh the screen.

-   You can no longer manually import transport requests into this queue.

-   The *Enable Automatic Import* option turns into a *Disable Automatic Import* option.

    To disable the automatic import, choose *Import Settings* \> *Disable Automatic Import*.

-   If an import schedule existed for the import queue, it's deactivated.

    To run scheduled imports alongside automatic imports, reactivate the deactivated scheduled imports, or activate new ones.

-   The action is logged in the landscape action logs as an *Action Type* = *Edit* for the affected transport node. In the details, the *Import Automatically* attribute gets the new value *true*.

-   In the *Landscape Visualization*, when you display the details of the transport node, the *Import Automatically* property is displayed with the value *Yes*.


