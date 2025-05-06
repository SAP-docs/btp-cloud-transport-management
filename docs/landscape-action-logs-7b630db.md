<!-- loio7b630db668274b6d9cb00c96ebb2a248 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Landscape Action Logs

The landscape action logs display the history of all actions related to the landscape configuration in your SAP Cloud Transport Management subscription.

This includes actions such as create, edit, and delete transport nodes, transport routes, and scheduled import jobs.

To display the landscape action logs, on the SAP Cloud Transport Management home screen, choose <span class="SAP-icons-V5"></span> Landscape Action Logs from the navigation pane.

The log shows a list of landscape actions sorted by the time they were performed. The most recent action is at the top. For each landscape action, the log contains the following information:

-   *Entity Type*

    Examples are *Node*, *Route*, *Job*, *Archive*, and *Wizard*.

-   *Action Type*

    Examples are *Create*, *Edit*, and *Delete*.

-   *Affected Object*

    These are node or route names displayed as navigation links.

    > ### Note:  
    > The action logs for the *Wizard* entity type don't display any affected objects links. The detailed log displays the affected nodes and routes in separate tabs.
    > 
    > Affected objects with the *Delete* action type aren't displayed as links.

-   *Changed By*

    E-mail address or name of the user who has run the landscape action.


You can do the following:

-   Filter the data in the columns *Entity Type*, *Action Type*, *Changed By*, and *Changed On* either by entering any character strings in the respective fields and confirming with [Enter\], or by directly choosing the relevant information from the dropdown boxes.

    > ### Tip:  
    > You can display landscape action logs for a specific time period by using the date picker in the *Changed On* filter. To select the desired time interval, use the left mouse button. Keep the left mouse button pressed or select the start and end dates while holding down the [Shift\] or [CTRL\] key. If you prefer, you can type or edit the time period shown in the *Changed On* filter field.

-   Display the affected transport node or route by clicking the respective link.
-   Display the details of the landscape action by selecting the arrow at the end of the row, or by clicking anywhere in the row.

    For each action, the detailed view contains the data from the previous state \(*Old value*\) and the new state \(*New value*\). For *Create* or *Delete* actions, either the *Old value* state or the *New value* state is *None*.

    Logs related to import schedules are displayed using *cron* expressions.


