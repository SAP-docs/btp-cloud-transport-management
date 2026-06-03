<!-- loiob5aadd72d88f408490d2078150b5e866 -->

# Grouping Transport Nodes by Tags

Group transport nodes visually based on their assigned tags enabling you to organize and identify related nodes at a glance using your own custom categories, such as regions, environments, projects, or other meaningful classifications.



## Prerequisites

-   Transport nodes have tags assigned to them. For more information, see [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md).
-   You have one of the roles *Administrator* or *LandscapeOperator* assigned to your user. For more information, see [Security](60-security/security-51939a4.md).



## Context

Tag-based grouping visually groups all transport nodes that share a given tag, making it easier to navigate and understand large landscapes. You can apply multiple tags as grouping criteria. Each additional tag introduces a separate group on the canvas.

Note the following points about grouping behavior:

-   Each transport node belongs to exactly one group based on the first matching tag in your selection order.

-   You can adjust the tag order to change the grouping perspective.

-   Transport nodes that don't match any of the selected tags remain ungrouped.

-   Your grouping selection is saved locally and persists across sessions, but isn't shared or stored on the server.




## Procedure

1.  On the SAP Cloud Transport Management home screen, choose *Landscape Visualization* from the navigation pane.

2.  In the *View* toolbar, use the *Group by Tag* selection box to select one or more tags.

    -   1.  Select the dropdown arrow.

    A dropdown menu of all tags that are currently assigned to at least one transport node appears.

2.  Select one or more tags to use as grouping criteria.


    -   Start typing the tag name and choose [Enter\] to confirm your selection.




<a name="loiob5aadd72d88f408490d2078150b5e866__result"/>

## Results

The canvas updates immediately. Transport nodes that share a selected tag are enclosed in a labeled group frame.

If a transport node has multiple tags and more than one of those tags is selected, the node is assigned to the group of the **first matching tag** in the order in which you selected the tags.

The grouping persists across page refreshes for your user session on the current device.

You have the following options:

-   To change the group assignment of such a node, deselect and reselect the tags in the desired order.

-   To remove a grouping, deselect the corresponding tag in the *Group by Tag* dropdown.

    The group frame is removed from the canvas. Nodes that were part of this group revert to their ungrouped position, or are reassigned to another group if they match a remaining selected tag.


