<!-- loioc3c87cbe744b4334a0cf6ca7eb8805cf -->

# Add Files to Import Queues

By adding a file to the import queue, you upload it to the import queue and create a transport request.



<a name="loioc3c87cbe744b4334a0cf6ca7eb8805cf__prereq_o3z_fsd_5cb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *ExportOperator* assigned to your role. For more information, see [Security](../60-security/security-51939a4.md).

-   You’ve selected the *Allow Upload to Node* checkbox for the transport node to which you want to add a file.

-   You want to upload one of the content types *Multitarget Application*, *XSC Delivery Unit*, or *Application Content*. The manual upload of content of type *BTP ABAP* to import queues is not supported. The *Add* button is not available.

-   You are in the import queue of the transport node where you want to add files. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Context

In an import queue of a transport node, you can add content archives that you want to import. If you do this, a transport request is created and it’s added to the import queue of the transport node.

> ### Note:  
> You only need to upload files if you transport content archives that are available on a local file system. If you transport content archives directly in an application, the application adds them to the import queue.

You can upload files up to a maximum size of 1 GB. For each subscription to the service, you can upload files with a total maximum size. You can check how much of your space quota is already in use on the home screen of the SAP Cloud Transport Management UI.

If you upload larger files and depending on your network connection, the upload process can take some time. To monitor the progress of the upload process, you can choose ![](images/Upload_Progress_b2431d6.jpg) \(*Progress details on your current file uploads*\). The progress of all file uploads of your user in the current browser session is displayed.

> ### Note:  
> After an uploaded file was imported in all transport nodes along the configured transport routes, and the queue items aren’t in one of the statuses *Initial*, *Repeatable*, or *Fatal*, SAP Cloud Transport Management automatically deletes the uploaded files after 30 days. The metadata of the transport request isn’t deleted, only the file. The file is also automatically deleted if the transport request is deleted.
> 
> Like this, SAP Cloud Transport Management ensures that the total maximum size isn’t easily reached.



## Procedure

1.  In the import queue, choose *Add*.

2.  In the *Upload a file* dialog box, enter the following details:


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
    
    *Transport Description* 
    
    </td>
    <td valign="top">
    
    Description of the file upload process
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Content Type* 
    
    </td>
    <td valign="top">
    
    If a transport destination is assigned to the transport node, the content type is preselected based on the content type specified in the destination. You can’t change it. If no transport destination is assigned, you must select the content type that you want to upload from the dropdown list.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *File* 
    
    </td>
    <td valign="top">
    
    Select the file that you want to upload. For content type *Multitarget application*, you can upload `*.mtar` files. For content type *XSC Delivery Unit*, you can upload `*.tgz` files. For application-specific content types, you can upload `.zip` files.
    
    </td>
    </tr>
    </table>
    
3.  To upload the file, choose *OK*.

    A transport request with the uploaded file is added to the import queue.

    You can now import it.




<a name="loioc3c87cbe744b4334a0cf6ca7eb8805cf__postreq_r2l_qdt_xxb"/>

## Next Steps

[Import Transport Requests](import-transport-requests-d2005d5.md)

