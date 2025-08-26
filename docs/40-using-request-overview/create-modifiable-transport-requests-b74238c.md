<!-- loiob74238c48e774dd2a4a26ce5df6f15b2 -->

# Create Modifiable Transport Requests

Create modifiable transport requests to efficiently manage multiple files in one request.



<a name="loiob74238c48e774dd2a4a26ce5df6f15b2__prereq_axj_wvx_dgc"/>

## Prerequisites

-   You are in the transport requests overview. For more information, see [Managing Transport Requests](managing-transport-requests-d088caa.md).
-   You have at least the authorization of the *ExportOperator* role for the node that serves as the source node. For more information, see [Security](../60-security/security-51939a4.md).



## Context

When creating a modifiable transport request, you select a source node for the transport request and choose whether you want to upload the request to the selected node or not. If it's uploaded to the selected transport node, it's available for import in the import queue of this transport node. Use this option if you want to import content into the source node. If not, the selected transport node is used to export the content and forward it to the import queues of the follow-on nodes.



## Procedure

1.  Choose *Create*.

2.  On the *Create Open Transport Request* dialog, select or enter the following information:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Value
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Source Node*
    
    </td>
    <td valign="top">
    
    Select a source node for the transport request.

    All transport nodes that have file uploads enabled can be selected as source nodes.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Upload in Source Node*
    
    </td>
    <td valign="top">
    
    Select the checkbox if you want to import the transport node in the source node. If not, the source node is used to export the content of the transport request from the source node and forward it to the follow-on nodes.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Content Type*
    
    </td>
    <td valign="top">
    
    Select the content type for the files added to the transport request. Ensure that the selected content type matches the content type of the selected source node.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    Enter a description of the transport request.
    
    </td>
    </tr>
    </table>
    
3.  Choose *Create*.

    You've created a modifiable transport request that's still empty.

    You can add any number of files to the modifiable transport request as required.

4.  To add files to the transport request, click anywhere in the transport request row. On the *Content* tab, choose *Add*.

5.  Choose *Browse*, and select a file from your local file system that matches the content type that you specified for the modifiable transport request.

6.  Choose *Upload*.

    > ### Note:  
    > The content type of the uploaded file must match the content type selected for the transport request.




<a name="loiob74238c48e774dd2a4a26ce5df6f15b2__result_dt3_qjb_jgc"/>

## Results

You've created a modifiable transport request and added files to it.

You can add more files, remove files, and rearrange them as required.

As long as the transport request isn't yet in *Test* mode, it isn't yet visible in any import queue.

After you've added all relevant files, you can test the transport request.



<a name="loiob74238c48e774dd2a4a26ce5df6f15b2__postreq_srf_rrf_ggc"/>

## Next Steps

[Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md)

