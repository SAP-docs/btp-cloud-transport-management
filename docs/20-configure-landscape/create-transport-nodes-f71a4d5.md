<!-- loiof71a4d5550cd453ea824d5b5c677969d -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Create Transport Nodes

Create transport nodes as representations of the source and target end points of deployment processes in your landscape. Add configuration details as required.



<a name="loiof71a4d5550cd453ea824d5b5c677969d__prereq_bw3_tcd_gcb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *LandscapeOperator* assigned to your user. For more information, see [Security](../60-security/security-51939a4.md).

-   You've configured transport destinations. For more information, see [Create Transport Destinations](create-transport-destinations-c9905c1.md).

-   If you want to use SAP Alert Notification service to send notifications about import actions: You've configured the `ALERT_NOTIFICATION_SERVICE` destination in the subaccounts where you want to use the service.
-   You are on one of the following screens in the SAP Cloud Transport Management UI:
    -   On the *Landscape Visualization* screen, you've chosen :heavy_plus_sign:.
    -   On the *Transport Landscape Wizard* screen, you create a transport node as part of the wizard.
    -   On the *Transport Nodes* screen, you've chosen :heavy_plus_sign:.




## Procedure

1.  On the dialog, enter the necessary information or select the required options in the following fields:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Enter a name of the node.

    The name is case-sensitive.

    > ### Note:  
    > This is important, for example if you use SAP Content Agent service integrated with SAP Cloud Transport Management. In this case, the node name needs to match the `sourceSystemId` parameter of the destination that's necessary for the export of content in the SAP Content Agent user interface. For more information, see [Create TransportManagementService Destination](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/eed66f35f9d148c8ae5b2d46ff097d8c.html?locale=en-US&state=PRODUCTION&version=Cloud).


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    Enter a description.

    > ### Note:  
    > This field is optional.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Tags*
    
    </td>
    <td valign="top">
    
    Use tags to categorize transport nodes by providing additional information, such as project details, or system characteristics.

    You have the following options:

    -   To add a new tag, enter the tag text in the input field and press [Enter\].
    -   To assign an existing tag, start typing the tag text in the input field. Tags that correspond to the character string, appear in a dropdown list. Select the relevant tag for the node.
    -   To remove an assigned tag from the transport node, select the tag's :x: icon.

    Note the following points regarding tags:

    -   In the following situations, a tag is deleted:
        -   When you remove a tag that's associated exclusively to one node.
        -   When you delete a transport node that has a tag exclusively assigned to it.

    -   Searching for tags is currently not possible.
    -   Tags are displayed in the *Tags* column on the *Transport Nodes* screen. They are not visible on other screens, such as the import queue.

    > ### Note:  
    > This field is optional.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Allow Upload to Node*
    
    </td>
    <td valign="top">
    
    To enable the upload of files to this node, select this checkbox.

    If you select the checkbox, files can be added to this node. This is required in the scenario where you want to transport archives that are available on local file systems.

    If external applications upload files using API remote calls, this checkbox must be selected. Otherwise, SAP Cloud Transport Management prevents the upload of files to this node.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Perform Notification*
    
    </td>
    <td valign="top">
    
    If the `ALERT_NOTIFICATION_SERVICE` destination is configured in the subaccount, this checkbox is available.

    You can configure the SAP Alert Notification service to issue notifications for specific events, for example, when an import on this node is started and when it's finished. For more information, see [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](../receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Forward Mode*
    
    </td>
    <td valign="top">
    
    The following forward modes are available:

    -   *Pre-Import* \(default\): When imports of transport requests are started in this node, as a first step, the requests are automatically forwarded to all target transport nodes, before being imported in the current node.
    -   *Post-Import*: Transport requests are automatically forwarded, after they've been imported in the current node, regardless of the import results and the request statuses after the imports. If the import fails, the transport requests are still forwarded to the import queues of the target nodes.
    -   *On Success*: Transport requests are only automatically forwarded, after they've been successfully imported in the current node. An import is successful, if the status of the request after the import is either *Skipped*, *Succeeded*, or *Warning*.
    -   *Manual*: No automatic forwarding of transport requests. A *Forward* button appears in the import queue of this node. You can choose which transports to forward at a later point in time.

        > ### Note:  
        > The manual *Forwarding* function is only available in an import queue, if some prerequisites are fulfilled as described in [Forward Transport Requests](../30-using-import-queue/forward-transport-requests-630fae7.md).



    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Controlled By SAP Solution Manager*
    
    </td>
    <td valign="top">
    
    For target nodes used with Change Request Management or Quality Gate Management of SAP Solution Manager, select this checkbox. As a result, there's no option to manually start imports into such a transport node.

    > ### Note:  
    > This option isn't available when using the *Transport Landscape Wizard*.

    For more information about the integration of SAP Cloud Transport Management in SAP Solution Manager processes, see [Integrations Into Other Cloud Services, Development, and Change Management Processes](../70-integrations/extended-integration-scenarios-7e966f7.md#loio1b3c6637adb54d4bbb1828f911bb9547).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Virtual Node*
    
    </td>
    <td valign="top">
    
    If the transport node doesn't refer to a physical source or target end point of a deployment process, select *Virtual Node*.

    In this case, the node can't have a content type or destination. No import happens. For more information, see [About Transport Nodes](about-transport-nodes-7cd4a78.md).

    > ### Note:  
    > This option isn't available when using the *Transport Landscape Wizard*.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Content Type*
    
    </td>
    <td valign="top">
    
    If you create a transport node pointing to a **target** end point of a deployment process, select the *Content Type* that you want to import into this node from the dropdown box.

    The following content types are available:

    -   *Application Content*
    -   *Multitarget application \(MTA\)*
    -   *BTP ABAP*
    -   *XSC Delivery Unit*

    > ### Note:  
    > If you create a source node, you can leave the *Content Type* and *Destination* fields deselected.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Destination*
    
    </td>
    <td valign="top">
    
    If you create a transport node pointing to a **target** end point of a deployment process, select the *Destination* that you want to use for the import from the dropdown box.

    If you need to create a new destination, use the *Go to Destination View* link to open the *Destinations* editor of your subaccount in SAP BTP Cockpit.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Deployment Strategy*
    
    </td>
    <td valign="top">
    
    For transport nodes with the content type *Multitarget Application* and the *Destination* pointing to Cloud Foundry environment, define a deployment strategy.

    If you use the *default* strategy, the old version of the application is stopped before the deployment. After the import of the new version, the new version is started.

    If you use the *blue-green* strategy, the application is updated without downtime as described in the SAP BTP documentation under [Blue-Green Deployment Strategy](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7c83810c31d842938cbc39c135a2d99f.html).

    > ### Note:  
    > SAP Cloud Transport Management skips the testing phase of the blue-green deployment \(using parameter `--skip-testing-phase`\).

    > ### Note:  
    > This option isn't available when using the *Transport Landscape Wizard*.


    
    </td>
    </tr>
    </table>
    
2.  Choose *OK*.




<a name="loiof71a4d5550cd453ea824d5b5c677969d__result_bjv_lww_fcb"/>

## Results

You've created a transport node.

-   On the *Transport Nodes* screen, the node is added to the list.
-   On the *Landscape Visualization* screen, the node is added to the canvas.
-   When you've added a new tag, it's created and becomes available for selection on other transport nodes.

You have the following options:

-   Edit a transport node.

    -   On the *Transport Nodes* screen, select the radio button in front of the transport node name, and choose :pencil2:.
    -   On the *Landscape Visualization* screen, select a transport node and click on the :pencil2: icon in the side menu, or on the :pencil2: icon in the icon bar.

    Use the :pencil2: function also to assign tags to nodes or remove tags from them.

-   Navigate to the import queue of a transport node:

    -   On the *Transport Nodes* screen, click anywhere in the transport node row.
    -   On the *Landscape Visualization* screen, select the node, and choose the <span class="SAP-icons-V5"></span> \(Go to this node's import queue\) icon.

    The selected configurations are displayed in the header area. Virtual nodes are highlighted using an info label.

-   If the transport node is assigned to transport routes, you can display the assign transport routes:
    -   On the *Transport Nodes* screen, click anywhere in the transport node row, and choose the *Transport Routes* tab.
    -   On the *Landscape Visualization* screen, select the node, choose the <span class="SAP-icons-V5"></span> \(Go to this node´s import queue\) icon, and choose the *Transport Routes* tab.


You can check the details of all actions performed on nodes in the [Landscape Action Logs](../landscape-action-logs-7b630db.md).



<a name="loiof71a4d5550cd453ea824d5b5c677969d__postreq_p1c_zv2_2db"/>

## Next Steps

[Create Transport Routes](create-transport-routes-dddb749.md)

-   **[About Transport Nodes](about-transport-nodes-7cd4a78.md "In SAP Cloud Transport Management service, transport
		nodes represent source or target end points of a deployment process - for example, a Cloud
                            Foundry
		subaccount. Transports take place between transport nodes. ")**  
In SAP Cloud Transport Management service, transport nodes represent source or target end points of a deployment process - for example, a Cloud Foundry subaccount. Transports take place between transport nodes.

