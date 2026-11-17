<!-- loiof810a356cd384f25b8c5a2027e32e7f7 -->

# Disable the Import

To prevent imports from happening in a specific transport node, you can disable the import for the transport node.



<a name="loiof810a356cd384f25b8c5a2027e32e7f7__prereq_gw4_sk4_wxb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *TransportOperator* assigned to your role. For more information, see [Security](../60-security/security-51939a4.md).

-   You are in the transport node where you want to disable the import. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).



## Procedure

1.  In the transport node, choose *Import Settings* \> *Disable Import*.

2.  **Optional:** In the *Confirmation* dialog box, enter a reason for disabling the import.

3.  Confirm that you want to disable the import.




<a name="loiof810a356cd384f25b8c5a2027e32e7f7__result_ufx_ql4_wxb"/>

## Results

A disabled import has the following effects:

-   No imports are run in this node. This is also true for scheduled imports.
-   Other actions can take place in this node, such as adding files to the import queue.
-   For nodes with *Manual Forward Mode* enabled, forwarding is allowed. It's, however, not possible to change the status of entries that can't be forwarded yet, because they aren't yet in a status that allows forwarding \(*Succeeded*, *Warning*, or *Error*\).

    If automatic forwarding is enabled in the preceding node of the current node, transport requests are also still forwarded to the import queue of the current transport node.

-   The header area displays an *Import Disabled* status. If you hover over the status, the reason is displayed.
-   The action of disabling the import is logged in the Landscape Action Logs together with the reason, if a reason exists.
-   The *Disable Import* option changes to *Enable Import*.

To re-enable the import, choose *Import Settings* \> *Enable Import*.

