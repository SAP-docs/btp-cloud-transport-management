<!-- loio22e1ed69b9e24701a97955b97fc3ca8c -->

# Sample Configuration Scenario: Transport of Content Archives directly in another Application

The following sample configuration describes the scenario: Transport of content archives directly in another application.

The content archives will be attached to transport requests directly in the application and will be transported along the configured transport routes.

  
  
**Sample Configuration for Scenario: Transport of Content Archives directly in another Application**

![](images/Scenario_Directly_in_Application_dd24c82.png "Sample Configuration for Scenario: Transport of Content Archives directly in
					another Application")

You have a cloud application, such as SAP Cloud Integration. You have different subaccounts, for example, a DEV subaccount, a TEST subaccount, and a PROD subaccount where your application runs. You want to transport content archives \(`.mtar` files, for example\) of this application from one subaccount to another. To perform the transport directly in the application, the following entities must be configured:


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

Transport destinations to the TEST and PROD enviroments

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

Transport nodes for the DEV, TEST, and PROD environments, and transport routes between the nodes

</td>
<td valign="top">

In the SAP Cloud Transport Management service

</td>
<td valign="top">

-   [Create Transport Nodes](create-transport-nodes-f71a4d5.md)
-   [Create Transport Routes](create-transport-routes-dddb749.md)



</td>
</tr>
<tr>
<td valign="top">

A destination from the DEV environment pointing to SAP Cloud Transport Management 

</td>
<td valign="top">

In the DEV environment of the application

</td>
<td valign="top">

[Create Destinations to SAP Cloud Transport Management Service](create-destinations-to-sap-cloud-transport-management-service-795f733.md#loio795f7337e5d943df98c961303b02678b) 

</td>
</tr>
</table>

When you select a content archive for transport, a transport request is created and the content archive is attached to the transport request. The transport request is placed into the import queue of the TEST node so that the content archive is available for import in the TEST environment. Depending on the scenario, the transport request is also available in the DEV node. When the import is started in the TEST node, and the default *Pre-Import*forward mode was left unchanged in the TEST node, the transport request is forwarded to the PROD node so that the content archive is available for import in the PROD environment.

> ### Note:  
> For more information about existing integrations with SAP Cloud Transport Management, see [Integrating the Service](../70-integrations/integrating-the-service-7e966f7.md#loio7e966f73645c42eca1bf19e719b21ceb).

