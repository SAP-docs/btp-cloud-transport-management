<!-- loio7cd4a780fbec497d84b7336101669d4e -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# About Transport Nodes

In SAP Cloud Transport Management service, transport nodes represent source or target end points of a deployment process - for example, a Cloud Foundry subaccount. Transports take place between transport nodes.

You create transport nodes as part of the configuration of your transport landscape.

For specific purposes, you can configure transport nodes as *virtual nodes* that don't refer to a physical source or target end point. Virtual nodes can serve specific purposes, for example they can be used as placeholders to support uneven landscapes in hybrid change management scenarios, or to collect transport requests and forward them to a set of connected nodes. Transport requests that are imported into virtual nodes get the import status *Skipped* in this node.

A typical configuration of a source node includes allowing file uploads.

A typical configuration of a target node includes details about the deployment, such as the type of content to be transported, the name of the transport destination that addresses the *target* end point, or the deployment strategy. It can also include specifying that transports are managed by SAP Solution Manager.

You can find details of a transport node in the following places:

-   On the *Transport Nodes* screen: Select a transport node to display transport node details on individual tabs:
    -   *Import Queue* tab:

        Displays the import queue of the transport node. For more information, see [Using the Import Queue](../30-using-import-queue/using-the-import-queue-3c4b6f3.md).

    -   *Node Details* tab:

        Displays the configuration details of the transport node and details about the import settings.

    -   *Transport Routes* tab:

        Displays the transport routes associated with the transport node. When you select a transport node link, the transport routes of the selected node are displayed.

    -   *MTA Extension Descriptors* tab \(available in Cloud Foundry transport nodes with the content type *Multi-Target Application*\):

        Displays MTA extension descriptors associated with the transport node.

        *Deployment Configuration* tab \(available in transport nodes with the content type *Application Content*\):

        Displays the deployment configuration for application content associated with the transport node.


-   On the *Landscape Visualization* screen: The transport node representation displays information about imports in this node. Select a transport node to display:
    -   *Import Queue* tab on the *Transport Nodes* screen:

        Choose the <span class="SAP-icons-V5"></span> \(Go to Node´s Import Queue\) icon from the side menu. For more information, see [Using the Import Queue](../30-using-import-queue/using-the-import-queue-3c4b6f3.md).

    -   **Node Details** popover:

        Choose the <span class="SAP-icons-V5"></span> \(Node Details\) icon from the side menu. The popover contains details of the node configuration and import settings. You can use it to change the import schedule, disable and enable the import, and edit the node configuration.



**Related Information**  


[Create Transport Nodes](create-transport-nodes-f71a4d5.md "Create transport nodes as representations of the source and target end points of deployment processes in your landscape. Add configuration details as required.")

[Using the Landscape Visualization](../using-the-landscape-visualization-9fea4f2.md "Use the Transport Landscape Visualization to configure the transport nodes and transport routes of your transport landscape, as well as display and edit the existing landscape.")

[Using the Import Queue](../30-using-import-queue/using-the-import-queue-3c4b6f3.md "In the import queue of a transport node, you can start the upload of a file or import processes.")

<a name="UAI_workspace_update"/>

<!-- UAI\_workspace\_update -->

## updated content from UAi Workspace in Markdown



```
# About Transport Nodes

In SAP Cloud Transport Management service, transport nodes represent source or target end points of a deployment process - for example, a Cloud Foundry subaccount. Transports take place between transport nodes.

You create transport nodes as part of the configuration of your transport landscape.

For specific purposes, you can configure transport nodes as virtual nodes that don't refer to a physical source or target end point. Virtual nodes can serve specific purposes, for example they can be used as placeholders to support uneven landscapes in hybrid change management scenarios, or to collect transport requests and forward them to a set of connected nodes. Transport requests that are imported into virtual nodes get the import status **Skipped** in this node.

A typical configuration of a source node includes allowing file uploads.

A typical configuration of a target node includes details about the deployment, such as the type of content to be transported, the name of the transport destination that addresses the **target** end point, or the deployment strategy. It can also include specifying that transports are managed by SAP Solution Manager.

You can find details of a transport node in the following places:

- On the **Transport Nodes** screen: Select a transport node to display the transport node object page with individual tabs:

  - **Import Queue** tab:

    Displays the import queue of the transport node. For more information, see [Using the Import Queue](3c4b6f38866b4a70b20e79501db5f7e5.html "In the import queue of a transport node, you can start the upload of a file or import processes.").
  - **Node Details** tab:

    Displays the configuration details of the transport node and details about the import settings.
  - **Transport Routes** tab:

    Displays the transport routes associated with the transport node. When you select a transport node link, the transport routes of the selected node are displayed.
  - **MTA Extension Descriptors** tab:

    Displays MTA extension descriptors associated with the transport node.
  - **Deployment Configuration** tab:

    Displays the deployment configuration for application content associated with the transport node.
- On the **Landscape Visualization** screen: The transport node representation displays information about imports in this node and import settings. Select a transport node to open the transport node object page, where you can view the import queue, node details, transport routes, MTA extension descriptors, and deployment configuration. To change import settings, use **Import Settings** in the transport node header.

## Related Information

[Create Transport Nodes](f71a4d5550cd453ea824d5b5c677969d.html "Create transport nodes as representations of the source and target end points of deployment processes in your landscape. Add configuration details as required.")

[Using the Landscape Visualization](9fea4f2d75f9440c8d3679e81fc65c49.html "Use the Transport Landscape Visualization to configure the transport nodes and transport routes of your transport landscape, as well as display and edit the existing landscape.")

[Using the Import Queue](3c4b6f38866b4a70b20e79501db5f7e5.html "In the import queue of a transport node, you can start the upload of a file or import processes.")

```

