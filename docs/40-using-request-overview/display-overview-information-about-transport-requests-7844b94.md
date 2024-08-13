<!-- loio7844b94b21d14f81a7b2f6b8c8b5f6f6 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Display Overview Information about Transport Requests

For each transport request, the transport requests overview displays some basic overview information.

A transport request contains transportable content. It is created when a file is added to a transport node. It can contain different content types \(files or references\). On the transport requests overview, the following information is displayed for each transport request:

-   *ID*: ID of the transport request
-   *Description*: Description that was entered when the transport request was created.
-   *Owner*: User that created the transport request.
-   *Created At*: Date and time when the transport request was created.
-   *Occupied Storage*: Size of the file related to the transport request in megabytes \(MB\).
-   *Nodes*: Transport nodes related to the transport request.

    > ### Note:  
    > This column is inactive by default. You can display it in the :gear:.
    > 
    > If the *Nodes* column is displayed, the <span class="SAP-icons-V5"></span> \(Show related transport nodes\) icon allows you to display a list of all transport nodes related to the transport request. To go to the import queue of a transport node, select the node name.

-   *Status*: Aggregated statuses of the transport request in all transport nodes of the transport landscape.

    By default, all transport requests in status *Active* are displayed.

    For more information, see [Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md).


Clicking anywhere in a transport request row opens the transport request viewer. For more information, see [Display Details of Individual Transport Requests](display-details-of-individual-transport-requests-0415f2f.md).

