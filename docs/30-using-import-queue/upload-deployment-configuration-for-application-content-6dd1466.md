<!-- loio6dd14665fa654e8eaa13d883e8f8ec8e -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Upload Deployment Configuration for Application Content

If the deploying application supports a deployment configuration, you can upload it for transport nodes of content type *Application Content*.



## Prerequisites

-   To upload or delete deployment configurations, you need the *TransportOperator* role assigned. For more information, see [Security](../60-security/security-51939a4.md).
-   The deployment tool or application supports deployment configurations. Consult the relevant documentation for more information.
-   You are in the import queue of a transport node for the Content Type *Application Content*. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Context

A deployment configuration is a JSON file that contains data to control aspects of the deployment process, such as target spaces, subfolders, or other deployment tool-specific settings. You can upload it for transport nodes for the Content Type *Application Content*. The supported configuration options and their structure are defined by the deployment tool.

The deployment configuration is stored per transport node. It's passed to the deployment tool in every import triggered for that node, for as long as it remains configured. Only one deployment configuration can be active for a node at a time.

Note the following:

-   The configuration file content isn't logged. Only the upload or deletion actions of configuration files are recorded as transport actions.
-   The transport request log displays the name of the configuration file that was active for the node when the import started.
-   The deployment configuration isn't forwarded to target transport nodes. If you use deployment configurations in multiple nodes in your landscape, you must configure each node separately.

    > ### Note:  
    > Deployment configuration isn't supported for transport nodes with the *Multitarget Application \(MTA\)* content type. For MTA deployments, use MTA extension descriptors instead. For more information, see [Upload MTA Extension Descriptors](upload-mta-extension-descriptors-0c7a672.md).




## Procedure

1.  Choose <span class="SAP-icons-V5"></span> Deployment Configuration in the header action bar.

    The *Deployment Configuration* dialog opens.

2.  In the *Configuration File \(JSON\)* field, click in the *Upload \*.json file* field, and select a JSON file that contains the deployment configuration you want to use for deployment in the current transport node.

    > ### Note:  
    > The file must be a valid JSON file.

    The content of the file is displayed in the *Configuration* preview area.

    The *Description* field is automatically populated with the JSON file name.

3.  Choose *Submit Configuration*.

    The *Description* field is updated with the timestamp of the submission.

4.  In the *Deployment Configuration* dialog, you have the following additional options:


    <table>
    <tr>
    <th valign="top">

    Task
    
    </th>
    <th valign="top">

    How To
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Replace the deployment configuration.
    
    </td>
    <td valign="top">
    
    Open the *Deployment Configuration* dialog, upload a new file, and choose *Submit Configuration*. The existing configuration is replaced immediately.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Delete the deployment configuration.
    
    </td>
    <td valign="top">
    
    Open the *Deployment Configuration* dialog and choose *Delete Configuration*. The deletion is recorded as a transport action.
    
    </td>
    </tr>
    </table>
    



<a name="loio6dd14665fa654e8eaa13d883e8f8ec8e__result"/>

## Results

The deployment configuration is saved for the transport node. It's passed to the deployment tool at every subsequent import for this node.

Uploading and deleting deployment configurations are reflected as *File Upload* and *File Delete* actions in the transport action logs.

When you import a transport request in a node that uses a deployment configuration, the *Log of Transport Request *<Transport Description\>** contains an entry *Deployment configuration: *<file name\>* *. To view this log: In the import queue, in the line of the imported transport request, choose <span class="SAP-icons-V5"></span> \(Display the logs for queue entry\).

