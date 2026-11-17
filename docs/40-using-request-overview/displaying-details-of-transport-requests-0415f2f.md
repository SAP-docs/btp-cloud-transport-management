<!-- loio0415f2fba54844b58e20c6edc878caad -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Displaying Details of Transport Requests

Display details about individual transport requests and open the related import queues.



## Procedure

1.  In the import queue of a transport node or in the transport requests overview, select a transport request.

    The header shows general information about the transport request, such as its lifecycle status, transport request ID, date, creator, content type, and the size of the files that are attached to the transport request.

    For modifiable transport request, the header shows a testing status. This status belongs to the test function for modifiable transport requests. If imports in test nodes fail, select the *Imports Failed* link to display the affected transport nodes. For more information, see [Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md).

2.  Use the tabs to display more details.

    -   The *Tracking* tab shows the transport request in the landscape.

        The *Tracking* tab opens by default.

        The canvas shows the current state of the landscape linked to the transport request. It includes all relevant transport nodes and the transport routes between them. Colors indicate the import status of the transport request in each node. Use the legend to learn the meaning of the colors and the matching statuses.

        Each transport node shows more details, such as the node ID and the forward mode. When you select a node, a context menu opens. Use the menu to open the import queue of the selected node.

        For modifiable transport requests, a *Test Nodes* frame surrounds the transport nodes where testing takes place. Use the context menu of a transport node to go to its import queue or change the test node scope. For more information, see [Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md).

    -   The *Action Logs* tab shows actions for the transport request.

        This tab lists all actions related to the transport request in the relevant transport nodes, with the newest entries first. For each action in each node, the list includes the node name, action type, user, status, and last changed date. This also applies to deleted nodes.

        This tab doesn't explicitly show that a transport action was already archived. If **<anonymized\>** appears as the user, the action is archived.

        > ### Note:  
        > The *Archived* status of a *transport action* differs from the *Archived* status of a *transport request*. For more information, see [Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md).

        Select an action row to open the detailed log of the transport action \(*Log of Action: *<Transport Action\>**\). For more information, see [Transport Action Logs](../transport-action-logs-86319ed.md).

    -   The *Content* tab shows transport request content.

        This tab shows details about the content of the transport request. For each file, it shows the URI, name, version, and file name. If the content provider doesn't supply a name or version, these fields remain empty.

        On this tab, you can add content to a modifiable transport request, remove existing content, and rearrange content when the transport request contains multiple files. For more information, see [Create Modifiable Transport Requests](create-modifiable-transport-requests-b74238c.md).

        Select a file row to open the file detail view. For `.mtar` files, the detail view lists the file modules. This information matches the details that appear when you select :paperclip: in the import queue. If an application provides object metadata about the content of the transport request, the metadata appears. If metadata comes from both the content provider and the MTA descriptor, the detail view shows the metadata in separate *Transport Request* and *MTA Descriptor* sections. The *Transport Request* section contains object metadata that the content provider supplies during export, for example, through SAP Content Agent service. The *MTA Descriptor* section contains technical information from the MTA deployment descriptor, such as the MTA ID, version, modules, module types, or MD5 hash. The metadata is displayed in a hierarchical table. Depending on the section, the table shows information such as name or ID, type, and version.

        For example, transport requests for references of SAP Business AI Platform, ABAP environment contain metadata, such as the software component, commit ID, tag name, or branch name of the reference.



**Related Information**  


[Statuses of Transport Requests](statuses-of-transport-requests-3a8259e.md "A transport request can have an import status in an import queue and a lifecycle status in the transport requests overview.")

[Managing Transport Requests](managing-transport-requests-d088caa.md "Get an overview of the transport requests in your tenant, process modifiable transport requests, and delete transport requests from all import queues in your tenant.")

