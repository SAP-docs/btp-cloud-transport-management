<!-- loio9fea4f2d75f9440c8d3679e81fc65c49 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Using the Landscape Visualization

Use the Transport Landscape Visualization to configure the transport nodes and transport routes of your transport landscape, as well as display and edit the existing landscape.



<a name="loio9fea4f2d75f9440c8d3679e81fc65c49__prereq_a4t_5rn_c3b"/>

## Prerequisites

-   You've configured transport destinations. For more information, see [Create Transport Destinations](20-configure-landscape/create-transport-destinations-c9905c1.md).

-   You have one of the roles *Administrator*, or *LandscapeOperator* assigned to your user. For more information, see [Security](60-security/security-51939a4.md).




## Context

Use the Transport Landscape Visualization to perform the following tasks:

-   Configure the transport nodes and transport routes of your transport landscape.
-   Display and edit the existing transport landscape.
-   Get an overview of the status of existing imports in the transport nodes.



## Procedure

1.  On the SAP Cloud Transport Management home screen, choose <span class="SAP-icons-V5"></span> Landscape Visualization from the navigation pane.

    The canvas displays all transport nodes and transport routes that are known in SAP Cloud Transport Management service. For each transport node, the overall import status is displayed.

    -   When the overall status is *Error* or *Fatal*, the node displays an <span class="SAP-icons-V5"></span> \(Error\) icon and it's marked in red.

    -   When an import ended with a warning, the node displays a :exclamation: icon and it's marked in orange.

    -   When all imports were successful, the node displays a <span class="SAP-icons-V5"></span> \(Success\) icon and it's marked in green.


    Important node configurations are indicated by additional icons. For example, when imports are scheduled for this node, the <span class="SAP-icons-V5"></span> \(Import Scheduler\) icon is displayed, or when automatic import is enabled, the <span class="SAP-icons-V5"></span> \(Automatic Import Enabled\) icon is displayed.

    Virtual transport nodes are represented by a dashed line.

    The graph overview on the right provides a thumbnail view of the entire landscape. You can use it to navigate more easily in larger landscapes.

    The dropdown menus offer options to adjust the orientation and placement of nodes on the canvas.

2.  Using the icons in the icon bar, you can do the following:


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
    
    Create a new transport node. A dialog box opens where you can enter all relevant information for the node.

    See [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Create a Route\)
    
    </td>
    <td valign="top">
    
    Create a new transport route to connect transport nodes. A dialog box opens where you can enter all relevant information for the route.

    See [Create Transport Routes](20-configure-landscape/create-transport-routes-dddb749.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Refresh graph\)
    
    </td>
    <td valign="top">
    
    Refresh the graph, for example, to display changes made to the transport landscape by other users.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Export Landscape\)
    
    </td>
    <td valign="top">
    
    Export the landscape configuration to a `.zip` file, for example, for backup purposes.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Import Landscape\)
    
    </td>
    <td valign="top">
    
    Import a landscape configuration `.zip` file that you've previously exported, for example, because you want to replicate an existing landscape in another subaccount.

    The following prerequisites apply to the import:

    -   You need *Administrator* or *LandscapeOperator* authorization.
    -   You can only import a complete landscape. Importing partial landscapes isn't supported.
    -   The landscape configuration to be imported contains only unique transport nodes and routes that don't yet exist in the current transport landscape.
    -   The file to be imported hasn't been modified manually and doesn't exceed 10 MB.
    -   The version of SAP Cloud Transport Management where the landscape configuration was exported from is the same as the version where you want to import the configuration. You can check that the version is identical by comparing the version you can find in the `.zip` file with the current version. You find the current version by selecting :gear: in the title bar and choosing *About* from the dropdown menu.

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
    
    Display a legend of the colors used for the nodes and routes \(called *Lines* in the legend\) on the canvas. If you click on an entry in the legend, all relevant entities are highlighted in blue on the canvas.
    
    </td>
    </tr>
    </table>
    
3.  When you select a node, a context menu opens next to it. It provides the following options:


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
    
    <span class="SAP-icons-V5"></span> \(Node Details\)
    
    </td>
    <td valign="top">
    
    Display additional properties of a transport node, such as the description, content type, or destination, in a popover.

    The popover provides the following options:

    -   Use the action icons to enable or disable automatic import in the transport node, or create or edit a job schedule.

        > ### Note:  
        > If an automatic import or job scheduling is enabled, the respective icon has a green background.

    -   Edit the selected node.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Go to Node´s Import Queue\)
    
    </td>
    <td valign="top">
    
    Open the import queue of the transport node.

    See [Using the Import Queue](30-using-import-queue/using-the-import-queue-3c4b6f3.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    <span class="SAP-icons-V5"></span> \(Create Route\)
    
    </td>
    <td valign="top">
    
    Create a new transport route to connect the selected transport node with a target node. A dialog box opens where you can enter all relevant information for the route. The selected node is preconfigured as source node.

    See [Create Transport Routes](20-configure-landscape/create-transport-routes-dddb749.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :wastebasket:
    
    </td>
    <td valign="top">
    
    Delete the node.

    As an alternative, you can use your keyboard's [Delete\] key.
    
    </td>
    </tr>
    </table>
    
4.  When you select a route, a context menu opens next to it. It provides the following options:


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
    
    <span class="SAP-icons-V5"></span> \(Route Details\)
    
    </td>
    <td valign="top">
    
    Display the properties of a transport route: the description, source node, and target node, as well as edit the route.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    :wastebasket:
    
    </td>
    <td valign="top">
    
    Delete the route.
    
    </td>
    </tr>
    </table>
    

**Related Information**  


[Landscape Action Logs](landscape-action-logs-7b630db.md "The landscape action logs display the history of all actions related to the landscape configuration in your SAP Cloud Transport Management subscription.")

