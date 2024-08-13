<!-- loio0c7a672bbe85479d96e3e0a19c4364b8 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Upload MTA Extension Descriptors

If an extension descriptor file exists for a Multitarget Application \(MTA\) that you want to import, you can upload it in the import queue of the corresponding transport node of Cloud Foundry environment.



<a name="loio0c7a672bbe85479d96e3e0a19c4364b8__prereq_m12_4mq_4lb"/>

## Prerequisites

-   To upload or delete MTA extension descriptors, you need the *TransportOperator* authorization. For more information, see [Security](../60-security/security-51939a4.md).
-   You are in the import queue of a Cloud Foundry transport node for the Content Type *Multi-Target Application*. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Context

> ### Note:  
> This function is supported for transports in Cloud Foundry environment only.

A Multitarget Application \(МТА\) extension descriptor is a file that contains data complementary to a deployment descriptor. It allows you to customize the MTA deployment for a specific transport node. The file has the extension `.mtaext`. You can upload it in the import queue of a transport node. The MTA extension descriptor is used at import time whenever a transport request that contains a matching MTA version is imported. The following conditions must be met so that an MTA extension descriptor matches an MTA version:

-   The MTA ID is the same as specified using the *extends:* parameter in the MTA extension descriptor file.
-   The version binding defined for the MTA extension descriptor in SAP Cloud Transport Management matches the version of the MTA that is imported.

You can upload an MTA extension descriptor in an import queue at any point in time before the import of the MTA, also before the MTA itself is added to the import queue. It is used at the time of the import.

MTA extension descriptors are not forwarded to any target nodes. Therefore, you must upload an MTA extension descriptor in all import queues where you import the related MTA.

For more information about how to define MTA extension descriptors, see [Defining MTA Extension Descriptors](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/50df803465324d36851c79fd07e8972c.html).



## Procedure

1.  Choose <span class="SAP-icons-V5"></span> \(Open MTA Extension Descriptors\).

    In the dialog box, you see a list of MTA IDs for which MTA extension descriptors were already uploaded in the current import queue, together with the version binding defined for them, and the description.

2.  In the dialog box, you can upload a new extension descriptor. To do this, choose *Add*.

    1.  In the *Add a new MTA Extension Descriptor* dialog box, enter the following details:


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
        
        *MTA Extension File*
        
        </td>
        <td valign="top">
        
        Click anywhere in the input field, or choose *Browse...* to select the MTA extension descriptor that you want to upload in the import queue.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Version Binding*
        
        </td>
        <td valign="top">
        
        You can define for which versions of the MTA you want to use the extension descriptor.

        If you have uploaded an MTA extension descriptor, by default, this field contains an asterisk \(*\**\). This means that the MTA extension descriptor is valid for all versions of the MTA.

        > ### Recommendation:  
        > We recommend that you leave the asterisk unchanged.

        If you want to define that the MTA extension descriptor is valid for a specific version of the MTA only, you can enter the version of the MTA for which the extension descriptor is valid, for example, 1.4.2.

        > ### Note:  
        > You cannot use a combination of both options, for example 1.4.\*.
        > 
        > However, you can have both an extension descriptor that is valid for all versions of an MTA, and extension descriptors for specific versions of the MTA. If both exist for a specific version, SAP Cloud Transport Management will use the specific extension descriptor at for the import.


        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Description*
        
        </td>
        <td valign="top">
        
        By default, the name of the uploaded MTA extension descriptor file is entered as the description. You can change it.
        
        </td>
        </tr>
        </table>
        
    2.  Choose *Submit new descriptor*.


    The MTA extension descriptor that you uploaded is now available in the import queue. It is used when the transport request with the matching MTA version is imported.

3.  In addition, in the *MTA Extension Descriptors* dialog window, you have the following options:


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
    
    Show the content of an MTA extension descriptor file that was already added to the import queue.
    
    </td>
    <td valign="top">
    
    Choose :mag:.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Download an existing extension descriptor.
    
    </td>
    <td valign="top">
    
    Choose <span class="SAP-icons-V5"></span> \(Download MTA Extension File\).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    Remove a selected extension descriptor from the import queue.
    
    </td>
    <td valign="top">
    
    Select the extension descriptors that you want to remove, and choose *Remove*. The file will be removed.
    
    </td>
    </tr>
    </table>
    



<a name="loio0c7a672bbe85479d96e3e0a19c4364b8__result_mmw_g54_wxb"/>

## Results

Uploading and deleting MTA extension descriptors are reflected as actions in the transport action logs. When an extension descriptor is used for an import of an MTA, the transport action logs also contain information about the extension descriptor used.

You can check whether an MTA extension descriptor exists for an existing MTA in the following places: in the import queue by choosing :paperclip:. If an MTA extension descriptor exists, the <span class="SAP-icons-V5"></span> \(An extension descriptor is available for the Multi-Target Application archive.\) icon is displayed next to the name of the `.mtar` file. You can expand the tree to display the MTA ID.

