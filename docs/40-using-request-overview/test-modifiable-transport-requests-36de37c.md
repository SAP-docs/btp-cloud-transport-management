<!-- loio36de37c73a4046b980b0d3d6ebccebb7 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Test Modifiable Transport Requests

Test modifiable transport requests to ensure successful deployment.



<a name="loio36de37c73a4046b980b0d3d6ebccebb7__prereq_axj_wvx_dgc"/>

## Prerequisites

-   You're in the detail view of a modifiable transport request that you want to test. For more information, see [Displaying Details of Transport Requests](displaying-details-of-transport-requests-0415f2f.md).
-   You have at least the authorization of the *ImportOperator* role for all the nodes where you want to test the transport request. For more information, see [Security](../60-security/security-51939a4.md).



## Procedure

1.  To get an overview of the nodes where the import is tested, go to the *Tracking* tab.

    A *Test Nodes* frame surrounds the transport nodes where the testing takes place.

    If the *Upload in Source Node* checkbox was selected when creating the transport request, the test node scope includes the source node and the first-level follow-on nodes. If the checkbox wasn't selected, the scope only consists of the first-level follow-on nodes. You can modify this scope.

2.  **Optional:** Modify the scope of test nodes.

    You have the following options:

    -   Add another node to the test nodes scope.

        Select a node outside of the *Test Nodes* frame that you want to add. From the context menu choose :heavy_plus_sign:. When you select a node that isn't directly connected to a node within the frame, the in-between nodes are also added as test nodes. You can't select the last node of connected nodes because it's considered a production node and doesn't allow testing.

    -   Remove a node from the test nodes scope.

        Select a node within the *Test Nodes* frame that you want to remove from the test nodes scope. From the context menu, choose :x:.


3.  Choose *Test*.

    A dialog box opens that displays all test nodes.

4.  **Optional:** To start the import immediately when the transport request enters an import queue, select the *Auto Trigger Import* checkbox.

    This setting applies to all nodes of the test scope and is realized according to the forward mode of the nodes. If you don't select this checkbox, the transport request is added to the import queue, but the import isn't started. You must manually start the import.

5.  Choose *Test*.

    To see the results, you may have to refresh the screen.




<a name="loio36de37c73a4046b980b0d3d6ebccebb7__result_ok5_2sg_jgc"/>

## Results

The transport request is added to the import queues of the first-level nodes. It's in an *Initial* status and *Test* mode. If you've selected the *Auto Trigger Import* checkbox, SAP Cloud Transport Management immediately imports the request. If not, you can manually start the import. Forwarding the request to subsequent nodes occurs according to the specified forward mode for the node.

If the test finishes with an error in a node, the header section displays an *Imports Failed* status. Select this link to view the nodes where errors occurred.

> ### Example:  
> Examples of forward mode settings and the impact on testing modifiable transport requests:
> 
> -   The forward mode of the first transport node is *On Success*. If the import into that node fails, the transport request isn't forwarded to the follow-on node.
> -   The forward mode of the first transport node is *Pre-Import* \(*AUTO*\). If the import into that node fails, the transport request is still forwarded to the follow-on node. If the *Auto Trigger Import* checkbox is selected, the transport request is also imported in the follow-on node.

Based on the test results, you can change the transport request at any time during testing as needed.



<a name="loio36de37c73a4046b980b0d3d6ebccebb7__postreq_gdj_fsg_jgc"/>

## Next Steps

[Release Modifiable Transport Requests](release-modifiable-transport-requests-b96d433.md)

