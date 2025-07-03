<!-- loio110a7a4d19a34a6cb9a5422c5c9eb35b -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Schedule Imports

To run imports of all transport requests in a transport node on a regular basis, you can schedule them to run at regular intervals.



<a name="loio110a7a4d19a34a6cb9a5422c5c9eb35b__prereq_dx4_wsj_wgb"/>

## Prerequisites

-   You have the *TransportOperator* authorization. For more information, see [Security](../60-security/security-51939a4.md).

-   A regular import of all transport requests is allowed in the import queue in which you want to schedule imports.

-   You are in one of the following places in SAP Cloud Transport Management:

    -   In the import queue of a transport node. For more information, see [Prerequisites for Using the Import Queue](prerequisites-for-using-the-import-queue-dd661c7.md).
    -   In the *Properties* panel of a transport node in the *Landscape Visualization*. For more information, see [Using the Landscape Visualization](../using-the-landscape-visualization-9fea4f2.md).




<a name="loio110a7a4d19a34a6cb9a5422c5c9eb35b__context_zly_2bx_rfc"/>

## Context

By default, system administration manually imports transport requests into transport nodes. You can schedule imports in transport nodes to ensure that all transport requests are imported at defined intervals or specific times.

> ### Note:  
> If the available intervals for scheduled imports don't meet your requirements, you can instead define that transport requests are immediately imported when they enter an import queue. For more information, see [Enable Automatic Import](enable-automatic-import-9171d39.md).



## Procedure

1.  Choose <span class="SAP-icons-V5"></span> \(Import Scheduler\).

2.  In the dialog box, you can choose one of the import patterns *Daily* or *Weekly*:


    <table>
    <tr>
    <th valign="top">

    Option
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Daily*
    
    </td>
    <td valign="top">
    
    Choose a time interval for the scheduled daily imports from the dropdown box \(for example, *Every hour*, *Four times per day*\).
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Weekly*
    
    </td>
    <td valign="top">
    
    You have the following options:

    -   Select a time interval for the scheduled weekly import from the dropdown box \(for example, *Every week*, *Every second week*.

    -   Select an *Execution Time*, that is the starting time, for the scheduled imports.
    -   Select the days of the week on which the scheduled imports take place.


    
    </td>
    </tr>
    </table>
    
3.  By default, the import schedule is inactive. To activate the schedule, select the *Active* checkbox.

4.  Choose *Create*.




<a name="loio110a7a4d19a34a6cb9a5422c5c9eb35b__result_jkp_tfj_ygb"/>

## Results

If the schedule is active, the imports of all transport requests in the import queue of the transport node are scheduled with the specified options and will be run as specified.

If you open an import queue with scheduled imports, the header area displays an *IMPORT SCHEDULE DETECTED* button. You can click on this button to display more information about the job status and the next time the job is run.

> ### Note:  
> If the job scheduler has many jobs to process, it's possible that the start time of the job is delayed.

If a scheduled import run failed with a fatal error at least three times in a row over a period of at least three weeks, the schedule is automatically deactivated. The affected transport node is displayed on the SAP Cloud Transport Management home screen in the *Import Schedules* section. If you still need the import schedule, resolve the issue, and reschedule the import.

