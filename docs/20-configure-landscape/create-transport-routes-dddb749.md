<!-- loiodddb74937a014aea8d3d76d740180597 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Create Transport Routes

In SAP Cloud Transport Management, transport routes are used to connect transport nodes.



<a name="loiodddb74937a014aea8d3d76d740180597__prereq_bw3_tcd_gcb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *LandscapeOperator* assigned to your user. For more information, see [Security](../60-security/security-51939a4.md).

-   You have configured transport nodes. For more information, see [Create Transport Nodes](create-transport-nodes-f71a4d5.md).

-   You are on one of the following screens in the SAP Cloud Transport Management UI:
    -   On the *Landscape Visualization* screen, you have chosen <span class="SAP-icons-V5"></span> \(Create a Route\), or you have chosen <span class="SAP-icons-V5"></span> \(Create Route\) from the side menu of a selected transport node.
    -   On the *Transport Landscape Wizard* screen, you create a transport route as part of the process.
    -   On the *Transport Nodes* screen, you have chosen :heavy_plus_sign:.




<a name="loiodddb74937a014aea8d3d76d740180597__context_ywt_z4n_vcb"/>

## Context

You can use the same transport node as a source node for multiple transport routes. However, you can use the same transport node only once as a target node for a transport route.



## Procedure

1.  Enter a name for the transport route.

2.  **Optional:** Enter a description.

3.  Choose the source and the target nodes from the existing transport nodes.




<a name="loiodddb74937a014aea8d3d76d740180597__result_bjv_lww_fcb"/>

## Results

The transport route was created. You can edit transport nodes at a later point in time:

-   On the *Transport Routes* screen, select the checkbox in front of the transport route name, and choose :pencil2:.
-   On the *Landscape Visualization* screen, select a transport route and click on the :pencil2: icon in the icon bar.

You can check the details of all actions performed on transport routes in the [Landscape Action Logs](../landscape-action-logs-7b630db.md).

