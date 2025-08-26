<!-- loiod088caa3a7a34be082a3fa64d4aa3708 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Managing Transport Requests

Get an overview of the transport requests in your tenant, process modifiable transport requests, and delete transport requests from all import queues in your tenant.



<a name="loiod088caa3a7a34be082a3fa64d4aa3708__context_bbp_ss2_ggc"/>

## Context

Transport requests serve as containers for transporting content. Transport requests can contain different content types \(files or references\). By default, they are created automatically whenever files are added to import queues of transport nodes. These transport requests contain one file and cannot be changed. You can create modifiable transport requests that let you add multiple files and test their deployment before releasing them to production environments.

To manage transport requests, choose <span class="SAP-icons-V5"></span> Transport Requests from the navigation pane in the SAP Cloud Transport Management user interface.

All transport requests in a tenant are displayed in a list. For each transport request, the list displays the ID, description, creation date, owner, the size of the files attached to the transport request, and a lifecycle status. By default, all transport requests in status *Released* and *Open* are displayed. For more information, see [Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md).

Managing transport requests includes performing different actions that are described in the following topics.

-   **[Displaying Details of Transport Requests](displaying-details-of-transport-requests-0415f2f.md "Display detailed information about individual transport requests and navigate to the
		related import queues.")**  
Display detailed information about individual transport requests and navigate to the related import queues.
-   **[Processing Modifiable Transport Requests](processing-modifiable-transport-requests-b541b09.md "Modifiable transport requests provide an efficient and flexible way for managing
		multiple files in one transport request.")**  
Modifiable transport requests provide an efficient and flexible way for managing multiple files in one transport request.
-   **[Delete Transport Requests](delete-transport-requests-2ef725c.md "You can delete transport requests from all import queues in your tenant. ")**  
You can delete transport requests from all import queues in your tenant.
-   **[Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md "A transport request can have an import status in an import queue and a lifecycle
		status in the transport requests overview.")**  
A transport request can have an import status in an import queue and a lifecycle status in the transport requests overview.

