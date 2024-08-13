<!-- loio7cd4a780fbec497d84b7336101669d4e -->

# About Transport Nodes

In SAP Cloud Transport Management service, transport nodes represent source or target end points of a deployment process - for example, a Cloud Foundry subaccount. Transports take place between transport nodes.

You create transport nodes as part of the configuration of your transport landscape.

For specific purposes, you can configure transport nodes as *virtual nodes* that don't refer to a physical source or target end point. Virtual nodes can serve specific purposes, for example they can be used as placeholders to support uneven landscapes in hybrid change management scenarios, or to collect transport requests and forward them to a set of connected nodes. Transport requests that are imported into virtual nodes result in a *Skipped* status.

A typical configuration of a source node includes allowing file uploads.

A typical configuration of a target node includes details about the deployment, such as the type of content to be transported, the name of the transport destination that addresses the *target* end point, or the deployment strategy. It can also include specifying that transports are controlled by SAP Solution Manager.

You can find the configuration details of a transport node in the following places:

-   On the *Transport Nodes* screen: When you select a transport node, the details are displayed in the header area.
-   On the *Landscape Visualization* screen: When you select a transport node, the details are displayed in a panel on the right side of the screen.

**Related Information**  


[Create Transport Nodes](create-transport-nodes-f71a4d5.md "Create transport nodes as representations of the source and target end points of deployment processes in your landscape. Add configuration details as required.")

[Using the Landscape Visualization](../using-the-landscape-visualization-9fea4f2.md "Use the Transport Landscape Visualization to configure the transport nodes and transport routes of your transport landscape, as well as display and edit the existing landscape.")

[Using the Import Queue](../30-using-import-queue/using-the-import-queue-3c4b6f3.md "In the import queue of a transport node, you can start the upload of a file or import processes.")

