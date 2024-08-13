<!-- loio3228b4c9de664dedb36532622d152a5f -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Search and Filter Options in an Import Queue

You have different options to search for transport requests in an import queue and filter for specific criteria.

-   You can search for queue entries in the import queue using the *Search* field:

    -   To search for a transport description, enter any character string.
    -   To search for a transport request ID, enter the complete ID.

-   You can filter queue entries according to the following criteria:


    <table>
    <tr>
    <th valign="top">

    Filter Criterion
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Status* 
    
    </td>
    <td valign="top">
    
    By default, queue entries with the statuses *Initial*, *Repeatable*, *Fatal*, and *Running* are displayed. You can select or deselect status values from the dropdown list.

    > ### Note:  
    > All queue entries that have the status *Succeeded* or *Error* will automatically get the status *Deleted* after a default retention period, the next time when an import is started.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Preset Date Range*
    
    </td>
    <td valign="top">
    
    By default, the queue entries of the last 7 days are displayed. You can select different time intervals from the dropdown box. The timestamp of a queue entry refers to the time of the last status change of the queue entry.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Custom Date*
    
    </td>
    <td valign="top">
    
    You can select a date or a date range from the calendar by choosing <span class="SAP-icons-V5"></span> \(Open Picker\) and clicking on the first and the last date of the date range. If you’ve selected a date range, the value of the preset date range is grayed out and no longer relevant. To clear the date range and return to the preset date range selection, delete the dates from the entry field.
    
    </td>
    </tr>
    </table>
    
    You can reset all filter options to the default values by choosing *Restore*.


