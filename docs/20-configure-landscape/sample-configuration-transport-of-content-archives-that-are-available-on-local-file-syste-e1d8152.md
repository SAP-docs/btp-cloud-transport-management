<!-- loioe1d815266da947189eeda66b6a2a87a6 -->

# Sample Configuration: Transport of Content Archives that are available on Local File Systems

The following sample configuration describes the situation when there's no export integration in the source environment and you want to transport content archives that are available on local file systems.

The content archive has been downloaded or exported from an application in the source DEV environment to a local file system. It is then added to the import queue of the TEST node in SAP Cloud Transport Management service so that it can be imported to the TEST environment.

  
  
**Sample Configuration: Transport of Content Archives that are available on Local File Systems**

![](images/Scenario_MTA_on_File_87b7d2a.png "Sample Configuration: Transport of Content Archives that are available on Local File
					Systems")

You have a cloud application, such as SAP Cloud Integration. For this application, you have different subaccounts, for example, a DEV subaccount, a TEST subaccount, and a PROD subaccount. You create a content archive \(a `.mtar` file, for example\) in the DEV subaccount of the application and you want to transport it to the TEST and PROD subaccounts. You can choose to perform the transport not directly in the application, but to download or export the content archive in the application of the DEV subaccount to your local file system.

To transport the content archive that is available on the local file system, the following entities must be configured:


<table>
<tr>
<th valign="top">

Entities to be configured

</th>
<th valign="top">

Where to configure?

</th>
<th valign="top">

More information

</th>
</tr>
<tr>
<td valign="top">

Transport destinations to the TEST and PROD environments

</td>
<td valign="top">

In the SAP BTP Cockpit of your subaccount in which you are subribed to SAP Cloud Transport Management

</td>
<td valign="top">

[Create Transport Destinations](create-transport-destinations-c9905c1.md) 

</td>
</tr>
<tr>
<td valign="top">

Transport nodes for the TEST and PROD environments, and a transport route between the nodes

</td>
<td valign="top">

In the SAP Cloud Transport Management service

</td>
<td valign="top">

-   [Create Transport Nodes](create-transport-nodes-f71a4d5.md)
-   [Create Transport Routes](create-transport-routes-dddb749.md)



</td>
</tr>
</table>

In SAP Cloud Transport Management, in the import queue of the TEST node, you upload a content archive to an import queue using the *Add* function. The upload process creates a transport request and attaches the content archive to it so that it is available in the import queue of the TEST node for import in the TEST environment. When the import is started in the TEST node, and the default *Pre-Import* forward mode was left unchanged in the TEST node, the transport request is forwarded to the PROD node so that the content archive is available for import in the PROD environment.

> ### Note:  
> For more information about the transport of SAP Cloud Integration content using download, see [Content Transport using MTAR Download](https://help.sap.com/viewer/368c481cd6954bdfa5d0435479fd4eaf/Cloud/en-US/c111710329174ab69127eb76b18d7c2c.html) in the *SAP Cloud Integration* documentation.

