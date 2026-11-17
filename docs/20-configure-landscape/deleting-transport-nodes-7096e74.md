<!-- loio7096e746df2b44b28a985d2290b33597 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Deleting Transport Nodes

Delete a transport node that is no longer needed in your transport landscape.



## Prerequisites

-   You have one of the roles *Administrator* or *Landscape Operator* assigned to your user. For more information, see [Security](../60-security/security-51939a4.md).

-   You've removed all transport routes connected to the node.




## Procedure

1.  Navigate to the transport node that you want to delete using one of the following options:

    -   On the *Transport Nodes* screen, select the radio button in front of the transport node name, and choose *Delete*.
    -   On the *Landscape Visualization* screen, select a transport node and choose :wastebasket: from the side menu.

2.  Confirm the deletion.




<a name="loio7096e746df2b44b28a985d2290b33597__result"/>

## Results

The transport node is deleted:

-   The node is removed from the *Transport Nodes* screen and from the *Landscape Visualization*.

-   Transport requests that were exclusively used in this import queue are deleted and immediately get the *Archived* status.

-   Tags that were exclusively assigned to this node are also deleted.


You can check the details of the action in the [Landscape Action Logs](../landscape-action-logs-7b630db.md).

