<!-- loio11365bf0a8d448f5ba63abaaae084478 -->

# Customer Data Export

Exporting transport-related action logs, MTA extension descriptors, and the current landscape configuration is possible at any time as part of the user interface of SAP Cloud Transport Management service. Additionally, it is possible to request a final customer data export as part of a decommissioning process.

> ### Recommendation:  
> The service does not alter the uploaded customer content in any way. The content is only persisted for the purpose of executing the deployment or import tasks as required. We recommend that you also store your content in a repository of your own, if required, since the service will remove it after fulfilling its deployment or import tasks.





### Data Export as Part of the Built-In Feature Set

The SAP Cloud Transport Management user interface offers the following built-in download functions to enable data export:


<table>
<tr>
<th valign="top">

Download Function

</th>
<th valign="top">

More Information

</th>
</tr>
<tr>
<td valign="top">

Download transport-related logs and archived transport action logs.

</td>
<td valign="top">

[Transport Action Logs](../transport-action-logs-86319ed.md)

</td>
</tr>
<tr>
<td valign="top">

Download MTA extension descriptors.

</td>
<td valign="top">

[Upload MTA Extension Descriptors](../30-using-import-queue/upload-mta-extension-descriptors-0c7a672.md)

</td>
</tr>
<tr>
<td valign="top">

Export landscape entities, such as transport nodes, routes and their properties.

</td>
<td valign="top">

[Using the Landscape Visualization](../using-the-landscape-visualization-9fea4f2.md)

</td>
</tr>
</table>



### Data Export as Part of the Decommissioning Process

SAP Cloud Transport Management offers a service to extract and create a final export of customer data in the course of a decommissioning process, which will permanently delete all content. Such an export event must take place prior to the purging phase in the decommissioning process. It is important that you consider the Terms and Conditions and their stated timeline when to request such an export.

If required, open an incident using component `BC-CP-LCM-TMS`. Please use the following prefix in the incident subject: `Customer Data Export Request`.

