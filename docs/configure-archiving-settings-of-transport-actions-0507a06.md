<!-- loio0507a065271e4aabab4dce1babc2a317 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Configure Archiving Settings of Transport Actions

SAP Cloud Transport Management regularly archives transport actions. You can change the default archiving settings for the transport action logs according to your requirements.



<a name="loio0507a065271e4aabab4dce1babc2a317__prereq_vgz_sy1_4bc"/>

## Prerequisites

You are in the *Transport Action Logs* in SAP Cloud Transport Management.



## Context

By default, transport actions in your SAP Cloud Transport Management subscription are archived every **13 weeks** \(roughly every quarter\). All transport action logs **older than 7 years** are moved to an archive file in a secondary storage and then deleted from the database. By default, archived transport action logs contain all information about the transport action including the information about the user running the transport action. After an archiving run, the archive files are available in the *Transport Action Logs* on the *Archived Logs* tab.

To change the archiving settings according to your needs, proceed as follows:



## Procedure

1.  In the *Transport Action Logs*, choose :gear:.

2.  On the *Configure Archiving Settings* dialog box, adjust the following settings:


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
    
    *Archive*/ *Delete*
    
    </td>
    <td valign="top">
    
    *Archive* \(default\):

    During an archiving run, transport actions older than the selected data retention period are moved to an archive file in a secondary storage, and get deleted from the database.

    *Delete*:

    During an archiving run, transport actions that are older than the selected data retention period get permanently deleted from the database. They aren't stored in an archive file.

    > ### Caution:  
    > Use this option with care, for example, when you've already downloaded the transport action logs and stored them locally.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Data Retention Period*
    
    </td>
    <td valign="top">
    
    Select the time period after which you want to archive the transport action logs. You can choose a value between 1 year and 7 years \(default\).

    > ### Note:  
    > Only transport actions that are **older** than the selected data retention period get archived.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Schedule of Archiving Runs*
    
    </td>
    <td valign="top">
    
    Select the time interval for the archiving job to run, such as every 1 week, or every 52 weeks. The default value is 13 weeks.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Anonymize User Data*
    
    </td>
    <td valign="top">
    
    If you want all user-related data, such as user names and e-mail addresses, to be removed from the archived transport actions during an archiving run, select the checkbox. Instead of user data, the transport actions and logs display ***<anonymized\>***.

    > ### Caution:  
    > Once the user information is anonymized during an archiving run, it can't be restored at a later point in time.


    
    </td>
    </tr>
    </table>
    
3.  Save your changes.




<a name="loio0507a065271e4aabab4dce1babc2a317__result_ulh_zx1_4bc"/>

## Results

The archiving job runs as a background job based on the criteria you specified. An archiving run is logged in the *Landscape Action Logs*.

You can access archive files in the transport action logs on the *Archived Logs* tab.

**Related Information**  


[Transport Action Logs](transport-action-logs-86319ed.md "The transport action logs display a history of all actions related to a transport.")

