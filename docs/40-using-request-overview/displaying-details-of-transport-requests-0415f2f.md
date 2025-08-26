<!-- loio0415f2fba54844b58e20c6edc878caad -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Displaying Details of Transport Requests

Display detailed information about individual transport requests and navigate to the related import queues.



## Procedure

1.  In the import queue of a transport node, or in the transport requests overview, select a transport request.

    The header section displays general information about the transport request, such as the lifecycle status, the transport request ID, the date, and user who created the transport request, its content type, and the size of the files that are attached to the transport request.

    For modifiable transport request, a testing status is displayed. This status is related to the test function available for modifiable transport requests. If imports in test nodes failed, select the *Imports Failed* link to display the affected transport nodes. For more information, see [Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md).

2.  On the individual tabs, you can display additional information.

    -   *Tracking* tab

        This tab is opened by default.

        The canvas displays the current state of the landscape related to the transport request. This includes all relevant transport nodes and the transport routes between them. Colors indicate the import status of the transport request in each node. Refer to the legend to understand the meaning of the colors and the corresponding statuses.

        Each transport node contains additional information, such as the node ID and the forward mode. When you select a node, a context menu opens that lets you open the import queue of the selected node.

        For modifiable transport requests, a *Test Nodes* frame surrounds the transport nodes where testing takes place. Using the context menu of the individual transport nodes, you can go to the import queues, or modify the test nodes scope. For more information, see [Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md).

    -   *Action Logs* tab

        This tab displays a list of all actions related to the transport request in the relevant transport nodes in reverse chronological order. For each action in each node, the list contains information about the node name, action type, user, status, and last changed date. This applies also to deleted nodes.

        This tab doesn't mention explicitly that a transport action was already archived. However, if the user is displayed as **<anonymized\>**, this means that the action is archived.

        > ### Note:  
        > Note that the *Archived* status of a *transport action* is different from the *Archived* status of a *transport request*. For more information, see [Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md).

        Clicking anywhere in an action row opens the detailed log of the transport action \(*Log of Action: *<Transport Action\>**\). For more information, see [Transport Action Logs](../transport-action-logs-86319ed.md).

    -   *Content* tab

        This tab displays details about the content of the transport request. For each file, it shows the URI, name, version, and file name.

        On this tab, you can add content to a modifiable transport request, remove existing content, and rearrange the content, if multiple files are attached to the transport request. For more information, see [Create Modifiable Transport Requests](create-modifiable-transport-requests-b74238c.md).

        Clicking anywhere in the row of a file opens the detail view that displays the MD5 hash of the file. For `.mtar` files, the detail view lists the individual modules of the file. This information corresponds to the details that you get when you choose :paperclip: in the import queue. If an application has added object metadata about the content of the transport request, this object metadata is displayed. For example, transport requests created for references of SAP BTP ABAP environment contain metadata, such as the software component, commit ID, tag name, or branch name of the reference.



**Related Information**  


[Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md "A transport request can have an import status in an import queue and a lifecycle status in the transport requests overview.")

[Managing Transport Requests](managing-transport-requests-d088caa.md "Get an overview of the transport requests in your tenant, process modifiable transport requests, and delete transport requests from all import queues in your tenant.")

