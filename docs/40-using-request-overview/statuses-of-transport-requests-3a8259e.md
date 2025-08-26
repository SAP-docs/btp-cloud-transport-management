<!-- loio3a8259eb89314035b8ebf84de9407435 -->

# Statuses of Transport Requests

A transport request can have an import status in an import queue and a lifecycle status in the transport requests overview.

Import statuses of transport requests in import queues:


<table>
<tr>
<th valign="top">

Import Status in Import Queue

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

The transport request was added to the transport node, but an import hasn't yet started.

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

*Transient*

</td>
<td valign="top">

A modifiable transport request was previously tested in the transport node and then released. Releasing the request changes its status to *Transient* in the import queues of follow-on transport nodes. This ensures the traceability of these requests.

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

Lifecycle statuses of transport requests:


<table>
<tr>
<th valign="top">

Lifecycle Status in Transport Requests Overview

</th>
<th valign="top">

Description

</th>
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
<tr>
<td valign="top">

*Modifiable*

</td>
<td valign="top">

The transport request is modifiable. For more information, see [Processing Modifiable Transport Requests](processing-modifiable-transport-requests-b541b09.md).

</td>
</tr>
<tr>
<td valign="top">

*Released*

</td>
<td valign="top">

In at least one import queue the import status of the transport request isn't *Archived* or *Deleted*.

</td>
</tr>
</table>

