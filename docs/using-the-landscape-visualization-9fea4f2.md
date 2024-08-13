<!-- loio9fea4f2d75f9440c8d3679e81fc65c49 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Using the Landscape Visualization

Use the Transport Landscape Visualization to configure the transport nodes and transport routes of your transport landscape, as well as display and edit the existing landscape.



<a name="loio9fea4f2d75f9440c8d3679e81fc65c49__prereq_a4t_5rn_c3b"/>

## Prerequisites

-   You've configured transport destinations. For more information, see [Create Transport Destinations](20-configure-landscape/create-transport-destinations-c9905c1.md).

-   You've one of the roles *Administrator*, or *LandscapeOperator* assigned to your user. For more information, see [Security](60-security/security-51939a4.md).




## Context

Use the Transport Landscape Visualization to perform the following tasks:

-   Configure the transport nodes and transport routes of your transport landscape.
-   Display and edit the existing transport landscape.
-   Get an overview of the status of existing imports in the transport nodes.



## Procedure

1.  On the SAP Cloud Transport Management home screen, choose <span class="SAP-icons-V5"></span> Landscape Visualization from the navigation pane.

    All transport nodes and transport routes that are known in SAP Cloud Transport Management service are displayed on the canvas. For all nodes, the import status is displayed. If the status is error or fatal, the node is marked in red. If an import ended with a warning, the node is marked in orange. Virtual transport nodes are represented by a dashed line.

2.  On the icon bar, the following functions are available:


    <table>
    <tr>
    <th valign="top">

    Option
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    :heavy_plus_sign:
    
    </td>
    <td valign="top">
    
    You can create a new transport node. A dialog box opens where you can enter all relevant information for the node.

    See [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Create a Route\)
    
    </td>
    <td valign="top">
    
    You can create a new transport route to connect transport nodes. A dialog box opens where you can enter all relevant information for the route.

    See [Create Transport Routes](20-configure-landscape/create-transport-routes-dddb749.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :pencil2:
    
    </td>
    <td valign="top">
    
    This function is active if you’ve selected a transport node or route in the canvas. You can edit the selected node or route.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :wastebasket:
    
    </td>
    <td valign="top">
    
    This function is active if you’ve selected a transport node or route in the canvas. You can delete the selected node or route.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(See properties\)
    
    </td>
    <td valign="top">
    
    You can display and hide additional properties of a transport node or transport route, such as the description, content type, or destination.

    The properties are displayed in a separate panel on the right side of the screen. Select a node or a route on the canvas to display its properties.

    In the Properties panel, you have the following options for transport nodes:


    <table>
    <tr>
    <th valign="top">

    Option
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Create a job schedule\)
    
    </td>
    <td valign="top">
    
    Opens the job scheduler that allows you to schedule import jobs at regular intervals. See [Schedule Imports](30-using-import-queue/schedule-imports-110a7a4.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Go to this node´s import queue*
    
    </td>
    <td valign="top">
    
    Opens the import queue of the selected transport node.
    
    </td>
    </tr>
    </table>
    

    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Refresh graph\)
    
    </td>
    <td valign="top">
    
    You can refresh the graph, for example, to display changes made to the transport landscape by other users.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Export Landscape\)
    
    </td>
    <td valign="top">
    
    You can export the landscape configuration to a `.zip` file, for example, for backup purposes.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Import Landscape\)
    
    </td>
    <td valign="top">
    
    You can import a landscape configuration `.zip` file that you've previously exported, for example, because you want to replicate an existing landscape in another subaccount.

    The following prerequisites apply to the import:

    -   You need *Administrator* or *LandscapeOperator* authorization.
    -   You can only import a complete landscape. Importing partial landscapes isn't supported.
    -   The landscape configuration to be imported contains only unique transport nodes and routes that don't yet exist in the current transport landscape.
    -   The file to be imported hasn't been modified manually and doesn't exceed 10 MB.
    -   The version of SAP Cloud Transport Management where the landscape configuration was exported from is the same as the version where you want to import the configuration. You can check that the version is identical by comparing the version you can find in the `.zip` file with the current version. You find the current version by selecting your logon email address in the title bar and choosing *About* from the dropdown menu.

    > ### Note:  
    > If a prerequisite isn't fulfilled, you can't import the landscape configuration.

    In the *Landscape Action Logs*, the number of imported transport nodes and routes are logged for the import action.

    > ### Restriction:  
    > You must export and import destinations separately. You must manually maintain credentials after importing a landscape.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :mag:
    
    </td>
    <td valign="top">
    
    Enter any character string in the *Search* field to display a dropdown list of all transport nodes and routes \(called *Lines* here\) that match this string. If you select a node or a route, it’s highlighted in blue.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Legend\)
    
    </td>
    <td valign="top">
    
    You can display a legend of the colors used for the nodes and routes \(called *Lines* in the legend\) on the canvas. If you click on an entry in the legend, all relevant entities are highlighted in blue on the canvas.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Zoom In\)

    <span class="SAP-icons-V5"></span> \(Zoom Out\)
    
    </td>
    <td valign="top">
    
    You can use the functions to zoom to the required size of the transport nodes and routes displayed on the canvas.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :desktop_computer:
    
    </td>
    <td valign="top">
    
    You can automatically fit all transport nodes to the canvas.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Enter Full Screen\)
    
    </td>
    <td valign="top">
    
    If you have large transport landscapes, you can display the canvas in full-screen mode.

    To exit full-screen mode, choose <span class="SAP-icons-V5"></span> \(Exit Full Screen\).
    
    </td>
    </tr>
    </table>
    
3.  For a selected node, you have the following options using the icons in the menu next to each node:


    <table>
    <tr>
    <th valign="top">

    Option
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Create Route\)
    
    </td>
    <td valign="top">
    
    You can create a new transport route to connect the selected transport node with a target node. A dialog box opens where you can enter all relevant information for the route. The selected node is preconfigured as source node.

    See [Create Transport Routes](20-configure-landscape/create-transport-routes-dddb749.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Go to this node´s import queue\)
    
    </td>
    <td valign="top">
    
    You can open the import queue of the selected transport node.

    See [Using the Import Queue](30-using-import-queue/using-the-import-queue-3c4b6f3.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :pencil2:
    
    </td>
    <td valign="top">
    
    You can edit the selected node.

    See [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :wastebasket:
    
    </td>
    <td valign="top">
    
    You can delete the selected node.

    As an alternative, you can use your keyboard´s [Delete\] key.
    
    </td>
    </tr>
    </table>
    
4.  You can edit or delete a selected route using the icons in the icon bar.


**Related Information**  


[Landscape Action Logs](landscape-action-logs-7b630db.md "The landscape action logs display the history of all actions related to landscape configuration.")

