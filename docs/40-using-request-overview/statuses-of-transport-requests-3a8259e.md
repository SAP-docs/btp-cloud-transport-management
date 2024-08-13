<!-- loio3a8259eb89314035b8ebf84de9407435 -->

# Statuses of Transport Requests

Transport requests can have different statuses in the import queue that are in turn aggregated into lifecycle statuses displayed in the transport requests overview.

In an import queue of a transport node, a transport request can have one of the following import statuses:


<table>
<tr>
<th valign="top">

Status in Import Queue

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*Deleted*

</td>
<td valign="top">

The transport request was removed from the import queue of the transport node.

For more information, see [Remove Transport Requests](../30-using-import-queue/remove-transport-requests-e4e92ed.md).

</td>
</tr>
<tr>
<td valign="top">

*Error*

</td>
<td valign="top">

The import of the transport request failed due to an error.

</td>
</tr>
<tr>
<td valign="top">

*Fatal*

</td>
<td valign="top">

The import of the transport request failed due to a fatal error.

</td>
</tr>
<tr>
<td valign="top">

*Initial*

</td>
<td valign="top">

The transport request was added to the transport node, but an import wasn´t yet started.

</td>
</tr>
<tr>
<td valign="top">

*Repeatable*

</td>
<td valign="top">

The transport request was earlier in an *Error*, *Skipped*, or *Succeeded* status and was manually reset - with the aim of restarting the import.

</td>
</tr>
<tr>
<td valign="top">

*Running*

</td>
<td valign="top">

The import of the transport request is currently running.

</td>
</tr>
<tr>
<td valign="top">

*Succeeded*

</td>
<td valign="top">

The import of the transport request in the transport node was successful.

</td>
</tr>
<tr>
<td valign="top">

*Skipped*

</td>
<td valign="top">

The import of the transport request in the transport node was intentionally skipped. The *Skipped* status is equivalent to a *Succeeded* status. It can occur in the following situations:

-   For all imports into virtual nodes, since physical imports into virtual nodes aren't possible.
-   For imports of the content types *BTP ABAP* and *application content* in situations where the deploy target has skipped the content deployment of the transport request.



</td>
</tr>
<tr>
<td valign="top">

*Warning*

</td>
<td valign="top">

Warnings occurred during the import of the transport request in the transport node.

</td>
</tr>
</table>

In the transport requests overview, the import statuses of a transport request in the related import queues are aggregated into the following lifecycle statuses:


<table>
<tr>
<th valign="top">

Status in Transport Requests Overview

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

*Active*

</td>
<td valign="top">

In at least one import queue the import status of the transport request isn't *Archived* or *Deleted*.

</td>
</tr>
<tr>
<td valign="top">

*Archived*

</td>
<td valign="top">

In all import queues that the transport request was part of, it was deleted by the automatic cleanup run of SAP Cloud Transport Management. For more information, see [Background Information: Storage Capacity](../50-administration/background-information-storage-capacity-e8d5187.md).

</td>
</tr>
<tr>
<td valign="top">

*Deleted*

</td>
<td valign="top">

In all import queues that the transport request was part of, it has the status *Deleted*.

</td>
</tr>
</table>

