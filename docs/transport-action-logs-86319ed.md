<!-- loio86319edd8f1141859e7b1ce6abcd9fdb -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Transport Action Logs

The transport action logs display a history of all actions related to a transport.



<a name="loio86319edd8f1141859e7b1ce6abcd9fdb__section_xff_nwb_mgb"/>

## Transport Action Logs

All transport actions that occur in your SAP Cloud Transport Management subscription such as *Import to Node*, *File Upload*, *Upload to Node*, *Delete Queue Entry*, *Repeat Queue Entry*, *Export to Node*, *Add Queue Entry*, or *Forward Queue Entry* are logged and displayed in the *Transport Action Logs*.

To display the transport action logs, on the SAP Cloud Transport Management home screen, choose <span class="SAP-icons-V5"></span> Transport Action Logs from the navigation pane.



### Transport Actions Tab

By default, the *Transport Actions* tab opens. It displays a list of all transport actions, sorted by the end time of the actions. The most recent action is at the top. For each action, information about the node, action type, user, status, and the end time is displayed.

On the *Transport Actions* tab, you can do the following:

-   Filter the data in the columns *Node*, *Action Type*, *User*, *Status*, and *End Time* either by entering any character strings in the respective fields and choosing [Enter\], or by choosing the relevant information from the dropdown boxes.

    > ### Tip:  
    > You can display transport action logs for a specific time period by using the date picker in the *End Time* filter. To select the desired time interval, use the left mouse button. Keep the left mouse button pressed or select the start and end dates while holding down the [Shift\] or [CTRL\] key. If you prefer, you can type or edit the time period shown in the *End Time* filter input field.

-   Display archived transport actions by selecting the *Include Archived* checkbox.

    By default, the list doesn't show archived transport actions.

-   Display more information about a specific transport action in the *Log of Action* by clicking anywhere in the row of the action.
-   Refresh the status of import actions that are currently running by choosing *Refresh expired actions*.

    By default, SAP Cloud Transport Management refreshes the status of import actions that remain for too long in the *Running* status at regular intervals when you are in the import queue of the transport node. Here, you can manually trigger a refresh.

-   Download transport actions to a `.zip` file by choosing <span class="SAP-icons-V5"></span> \(Download Transport Action Logs\).

    The downloaded `.zip` file contains logs of transport actions in your current subaccount that aren't archived yet, in either plain text \(`.txt`\) or `.csv` format. Depending on the selected format, it includes either multiple`.txt` files, one for each downloaded transport action, or a single `.csv` file containing all downloaded transport actions.

    You have the following download options:

    -   *Plain Text \(Selected Actions\)*:

        Download logs that match your current filter settings in plain text \(`.txt`\) format.

    -   *Plain Text \(All Actions\)*

        Download all logs in plain text \(`.txt`\) format, regardless of the filters applied.

    -   *CSV \(Selected Actions\)*

        Download logs that match your current filter settings in `.csv` format.

    -   *CSV \(All Actions\)*

        Download all logs in `.csv` format, regardless of the filters applied.


    > ### Note:  
    > SAP Cloud Transport Management stores all transport action logs of a subscription until they're archived. If you select the plain text format, the `.zip` file can contain many individual `.txt` files.

-   Change the default archiving settings for transport actions by choosing :gear:.

    By default, SAP Cloud Transport Management archives transport actions older than 7 years every 13 weeks. You can change the default settings. For more information, see [Configure Archiving Settings of Transport Actions](configure-archiving-settings-of-transport-actions-0507a06.md).




### Archived Logs Tab

The *Archived Logs* tab displays a list of archive files, sorted by the date of the archiving run. The most recent file is at the top. For each file, information is displayed about the start time of the earliest and latest transport actions, the number of archived actions, and the size of the archive file.

On the *Archived Logs* tab, you can do the following:

-   Download a selected archive file.

    An archive file is a `.zip` file containing all transport action logs that were archived in a specific time period. For each archived transport action, one `.txt` file exists. This `.txt` file contains the transport action log.

-   Delete a selected archive file.

    > ### Caution:  
    > A deleted archive file can't be restored.




<a name="loio86319edd8f1141859e7b1ce6abcd9fdb__logofaction"/>

## Log of Action: <Transport Action\>

In the detailed view, you find a detailed log containing all messages of a specific transport action.

In the *Log of Action: <Transport Action\>*, you can do the following:

-   Filter the messages by entering any character string in the *Messages* field. In addition, you can narrow down the results according to *Transport Request*, *Transport Status*, *Content*, and *Message Severity* by choosing the relevant criteria from the dropdown boxes.

-   Download all messages of the transport action by choosing <span class="SAP-icons-V5"></span> \(Download transport logs\). Select the format of the downloaded messages: plain text \(`.log`\) or `.csv`.


> ### Note:  
> The *Log of Action* of an archived transport action doesn't display any messages of the transport action. It only displays the header data plus the archiving time. To display the messages of an archived transport action, you can use the download function. The function remains available even after the action was archived.



> ### Note:  
> The log of a transport request, which is displayed when you choose the <span class="SAP-icons-V5"></span> \(Display the logs for this queue entry.\) icon in the import queue, contains all transport actions for this transport request. You can't download the transport log for a transport request.

-   **[Configure Archiving Settings of Transport Actions](configure-archiving-settings-of-transport-actions-0507a06.md "SAP Cloud Transport Management regularly archives
		transport actions. You can change the default archiving settings for the transport action
		logs according to your requirements.")**  
SAP Cloud Transport Management regularly archives transport actions. You can change the default archiving settings for the transport action logs according to your requirements.

