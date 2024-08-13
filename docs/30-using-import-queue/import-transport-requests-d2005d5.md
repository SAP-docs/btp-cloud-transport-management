<!-- loiod2005d5d2fc346b98eff7146107243fc -->

# Import Transport Requests

You can either import all transport requests in an import queue, or selected transport requests only.



<a name="loiod2005d5d2fc346b98eff7146107243fc__prereq_bcl_gtk_bhb"/>

## Prerequisites

-   To execute an import of all transport requests in the import queue, you need the *ImportOperator* authorization. To execute an import of selected transport requests in the import queue, you need the *TransportOperator* authorization. For more information, see [Security](../60-security/security-51939a4.md).

-   You're in the import queue of the transport node where you want to execute imports. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Context

In the import queue, you have the following options:

-   Import all transport requests in the import queue
-   Import one or more selected transport requests of the import queue
-   Import all transport requests up to a selected transport request.

> ### Note:  
> It is possible that an option is not available in an import queue. Possible reasons are that an option is not supported by the content type to be imported or because of missing authorizations of the user.

All entries with the *Initial*, *Fatal*, and *Repeatable* statuses can be imported.



## Procedure

1.  Make sure that the filters in the import queue are set correctly so that all relevant transport requests are displayed.

2.  To start the import, choose one of the following options:

    -   *Import All*

        To import all transport requests in the import queue, choose *Import All*.

        All transport requests are imported in the sequence in which they’re placed in the import queue.

        > ### Caution:  
        > The import also includes any importable transport requests that may currently not be visible because of your filter settings.

    -   *Import Selected* \(not available for content type *BTP ABAP*\)

        To import individual transport requests, select one or multiple transport requests, and choose *Import Selected*.

        The selected transport requests are imported in the sequence in which they’re placed in the import queue.

        Note that the import of individual transport requests can lead to inconsistencies in the target runtime if dependent transport requests aren’t imported. SAP Cloud Transport Management doesn’t perform any dependency checks on the selected transport requests.

    -   *Import Upto* \(available for content type *BTP ABAP*\)

        To import all requests in the import queue up to a specific transport request, select a transport request, and choose *Import Upto*.

        The selected transport request and all previous requests are imported in the sequence in which they are in the import queue.

        > ### Note:  
        > If relevant transport requests are hidden because of your filter settings, SAP Cloud Transport Management displays an error message. Adjust your filter settings to display the relevant transport requests, and restart the import.


    By default, the import is executed immediately.

3.  **Optional:** Schedule imports of all transport requests to be executed at regular intervals.

    For more information, see [Schedule Imports](schedule-imports-110a7a4.md).




<a name="loiod2005d5d2fc346b98eff7146107243fc__result_g3r_ksk_bhb"/>

## Results

If the transport node has a content type and a valid destination assigned, the transport requests are imported into the runtime of the transport node and get a *Succeeded* status.

If transport requests are imported in virtual nodes, they are forwarded to the import queues of the target nodes. In the virtual node itself, they get a *Skipped* status.

If multiple transport requests of content type *BTP ABAP* are imported using *Import Upto*, and all requests contain references of the same software component, only the content of the selected request is imported. All previous requests get a *Skipped* status.

For more information, see [Statuses of Transport Requests](../40-using-request-overview/statuses-of-transport-requests-3a8259e.md).

> ### Note:  
> If a transport request with a Multitarget Application archive \(`.mta`\) was imported in a subaccount of the Neo environment, the archive is afterward visible in the *Standard Solutions* category in the *Solutions* page in the SAP BTP cockpit of the subaccount. For more information on solutions, see [Operating Solutions](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/2abf7d47063542208d0d99f7bc05f4f4.html?locale=en-US) in the SAP BTP documentation.

Check the status and the logs to make sure that the import was successful.



### Transport Request Forwarding

Depending on the *Forward Mode* defined for the transport node, transport requests are automatically forwarded to the target nodes or not. For more information, see [Create Transport Nodes](../20-configure-landscape/create-transport-nodes-f71a4d5.md).

If automatic forwarding takes place, the transport requests are forwarded into all target transport nodes according to the transport routes defined for the node where the import was started.

Forwarded transport requests are added to the end of the import queues of the target nodes. If any forwarded transport requests are already part of the import queue of a target node, they’re moved to the end of this import queue. The status of a moved transport request changes as follows:

-   *Initial* remains *Initial*.
-   *Deleted*, *Error*, *Fatal*, *Skipped*, *Succeeded*, and *Warning* change to *Repeatable*.
-   *Repeatable* remains *Repeatable*.

If the *Forward Mode* is *Manual*, manually forward the transport requests as required. For more information, see [Forward Transport Requests](forward-transport-requests-630fae7.md).

