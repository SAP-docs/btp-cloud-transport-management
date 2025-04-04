<!-- loioa90d808cde2f4e78942c82f7bd750844 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Options to Display Information about Transport Requests

For each transport request displayed in the import queue, you can display additional information.

In the import queue, the transport requests are displayed together with their ID \(*Transport Request* column\) description, owner, status, node in which they were added to the queue \(*Entry Node* column\), and timestamp. For each transport request, you have the following options:


<table>
<tr>
<th valign="top">

Function

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

Click anywhere in the row of the transport request.

</td>
<td valign="top">

You can go to the Transport Request viewer to view additional information, such as all transport nodes where the transport request is used, more information about the attached content, and the action log. For more information, see [Display Details of Individual Transport Requests](../40-using-request-overview/display-details-of-individual-transport-requests-0415f2f.md).

</td>
</tr>
<tr>
<td valign="top">

:paperclip:

</td>
<td valign="top">

You can display the name of the attached file in a popover.

For `.mtar` files, you can display additional information about the content of the file.

> ### Note:  
> You can display the same information on the *Content* tab in the Transport Request viewer. For more information, see [Display Details of Individual Transport Requests](../40-using-request-overview/display-details-of-individual-transport-requests-0415f2f.md).



</td>
</tr>
<tr>
<td valign="top">

<span class="SAP-icons-V5"></span> \(Display the logs for queue entry\)

</td>
<td valign="top">

You can display the *Log of Transport Request <Request ID\>*. It displays the actions for the transport request in the current transport node.

> ### Note:  
> For MTA deployment on Cloud Foundry, the log of the transport request contains a link to the MTA operation logs for the deploy operation. Like this, you can obtain these logs without using the Cloud Foundry command-line interface \(`cf cli`\).
> 
> Note that the MTA operation logs expire within three days after the operation.
> 
> For more information, see [Multitarget Application Commands for the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/65ddb1b51a0642148c6b468a759a8a2e.html?locale=en-US&state=PRODUCTION&version=Cloud)



</td>
</tr>
</table>

