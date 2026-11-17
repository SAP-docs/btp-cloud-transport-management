<!-- loio39b082dba7604908b5dede0390b3bbf2 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Transport Routes

In SAP Cloud Transport Management, transport routes connect transport nodes and define the paths along which transport requests move through your transport landscape.



You create transport routes as part of the configuration of your transport landscape, after configuring transport nodes. Each transport route connects exactly one source node to one target node.

Multiple transport routes can originate from the same source node, allowing transport requests to be forwarded to several target nodes at the same time.

The *Forwarding Mode* configured on a transport node determines how transport requests are forwarded along the outgoing routes of that node. Depending on the forwarding mode, requests are forwarded automatically after import, or must be forwarded manually. For more information, see [Create Transport Nodes](create-transport-nodes-f71a4d5.md).



You can find details about transport routes in the following places:

-   *Transport Routes* screen: Displays all transport routes in your landscape together with source and target nodes. To navigate to a source or target node, select the corresponding link.
-   *Transport Nodes* screen: Select a transport node to open its import queue. Choose the *Transport Routes* tab to display the transport routes associated with that node.
-   *Landscape Visualization* screen: Transport routes are displayed as directed connections between transport nodes. Select a transport route to display source and target nodes.

    **Node Details** popover:

    To display the details popover, choose the <span class="SAP-icons-V5"></span> \(Route Details\) icon from the side menu. To edit the route configuration, choose *Edit*.


**Related Information**  


[Create Transport Routes](create-transport-routes-dddb749.md "In SAP Cloud Transport Management, transport routes are used to connect transport nodes.")

[Using the Landscape Visualization](../using-the-landscape-visualization-9fea4f2.md "Use the Transport Landscape Visualization to configure the transport nodes and transport routes of your transport landscape, as well as display and edit the existing landscape.")

[Forward Transport Requests](../30-using-import-queue/forward-transport-requests-630fae7.md "If the Forwarding Mode of a transport node is set to the value Manual, you can manually forward transport requests in this node to target transport nodes.")

