<!-- loio0415f2fba54844b58e20c6edc878caad -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Display Details of Individual Transport Requests

You can display comprehensive information about individual transport requests.



<a name="loio0415f2fba54844b58e20c6edc878caad__prereq_s32_rpj_55b"/>

## Prerequisites

You are in one of the following places in SAP Cloud Transport Management:

-   In the import queue of a transport node. For more information, see [Prerequisites for Using the Import Queue](../30-using-import-queue/prerequisites-for-using-the-import-queue-dd661c7.md).
-   In the transport requests overview. For more information, see [Using the Transport Requests Overview](using-the-transport-requests-overview-d088caa.md).



## Procedure

1.  Click anywhere in the row of the transport request whose details you want to display.

    In the header section of the transport request viewer, general information about the transport request is displayed:

    -   Transport Request ID
    -   Transport Description
    -   Created by
    -   Created at

2.  Open the different tabs to display the following information:

    -   *Tracking* tab

        This tab is opened by default.

        On a canvas, the current state of the landscape related to the transport request is displayed. This includes all transport nodes that are related to the transport request, and the transport routes between the nodes. The statuses of the transport requests in the individual nodes are indicated by colors. Use the legend to find out about the statuses of the transport request in the displayed transport nodes.

        The individual transport nodes contain more information, such as the Node ID, and the forward mode. Clicking on a node opens the import queue of the selected node.

    -   *Action Logs* tab

        This tab displays a list of all actions related to the transport request in the different transport nodes in reverse chronological order. For each action in each node, it contains information about the node, action type, user, status, and date. This applies also to deleted nodes.

        > ### Note:  
        > This tab doesn't mention explicitly that a transport action has already been archived. However, if the user is displayed as **<anonymized\>**, this means that the action is archived.
        > 
        > Note that the *Archived* status of a *transport action* is different from the *Archived* status of a *transport request*. See: [Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md)

        Clicking anywhere in an action line opens the detailed log of the transport action \(*Log of Action: *<Transport Action\>**\). For more information, see [Transport Action Logs](../transport-action-logs-86319ed.md).

    -   *Content* tab

        This tab contains more information about the content of the transport request. For `.mtar` files, the individual modules of the files contained in the transport request are displayed. The information displayed corresponds to the information that you get when you choose :paperclip: in the import queue.

        The checksum is available for files. You can download or copy the checksum to verify that the file is genuine and error-free.

        If an application has added object metadata about the content of the transport request, this object metadata is displayed here. For example, transport requests created for references of SAP BTP ABAP environment contain metadata, such as the software component, commit ID, tag name, or branch name of the reference.



**Related Information**  


[Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md "Transport requests can have different statuses in the import queue that are in turn aggregated into lifecycle statuses displayed in the transport requests overview.")

[Using the Transport Requests Overview](using-the-transport-requests-overview-d088caa.md "You can use the transport requests overview to display all transport requests in a tenant, to delete transport requests from all related transport nodes, and to display details of individual transport requests.")

