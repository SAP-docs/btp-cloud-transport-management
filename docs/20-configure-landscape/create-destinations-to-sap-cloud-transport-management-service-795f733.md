<!-- loio795f7337e5d943df98c961303b02678b -->

# Create Destinations to SAP Cloud Transport Management Service

If you use SAP Cloud Transport Management service to start the transport directly in your application, a destination to SAP Cloud Transport Management service is required in the source \(development\) environment of your application. This destination is used to export content from your source environment to SAP Cloud Transport Management.



<a name="loio795f7337e5d943df98c961303b02678b__prereq_dk1_hnt_q1c"/>

## Prerequisites

-   You want to start the transport directly in your application.
-   To create the destination to SAP Cloud Transport Management, you have the following information:
    -   You know the fixed name of the destination.

        The destination has a fixed name, for example `TransportManagementService` for SAP Cloud Integration, or `ctms_destination` for SAP Build Work Zone, standard edition.

    -   You know from which service key you retrieve the connection details.

        In general, you retrieve the required connection details from the service key of the SAP Cloud Transport Management instance that is used for the transport. For more information about how to create the service instance and a service key for SAP Cloud Transport Management, see [Creating a Service Instance and a Service Key](../10-initial-setup/creating-a-service-instance-and-a-service-key-f449560.md).





## Context

Destinations contain the connection details for the remote communication of an application.

In the source environment of your application, create a destination to SAP Cloud Transport Management to address the export API of SAP Cloud Transport Management. This destination contains the connection details to SAP Cloud Transport Management service, such as the address of the SAP Cloud Transport Management instance that will be used for the transport as well as authentication details. You retrieve the connection details from the service key of the SAP Cloud Transport Management instance used for the transport.

![](images/Destination_to_Cloud_Transport_Management_1836d59.png)

> ### Recommendation:  
> We recommend that you refer to the documentation of your application for details about how to configure the destination to SAP Cloud Transport Management.
> 
> -   For links to documentation of known integrations into SAP Cloud Transport Management, see [Integration in Development and Change Management Processes and with Other Services](../70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb).
> -   An overview of known content that is supported by SAP Cloud Transport Management is listed under [Overview: Supported Content](../supported-content-types-8961dcb.md#loio0dccbb6ee1714240b9b9bedc1a240a7e).



<a name="loio795f7337e5d943df98c961303b02678b__steps-unordered_jjz_k55_q1c"/>

## Procedure

-   SAP BTP, Cloud Foundry Environment

    The specific details for your application may depend on different criteria, such as whether SAP Content Agent service is used to export the content into `.mtar` files before handing them over to SAP Cloud Transport Management.

    For SAP Cloud Integration content, see [Enabling Content Transport, Cloud Foundry Enviroment](https://help.sap.com/docs/CLOUD_INTEGRATION/368c481cd6954bdfa5d0435479fd4eaf/452c677debfc4fda904310560ab03743.html?locale=en-US).

    For an example, see [Example: Destination to SAP Cloud Transport Management](create-destinations-to-sap-cloud-transport-management-service-795f733.md#loio75fe5d4b4fa3492c87ef6be32ea0b819).

-   SAP BTP, Neo Environment

    If your application runs in the SAP BTP, Neo environment, you define the destinations to SAP Cloud Transport Management in the SAP Solution Lifecycle Management service.

    For more information about how to configure destinations in SAP BTP, Neo, see [Set Up Direct Uploads of MTA Archives Using the Transport Management Service](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/af84d67f4be24542ac5e46f613a99435.html?locale=en-US).

    For SAP Cloud Integration, see also [Enabling Content Transport, Neo Environment](https://help.sap.com/docs/CLOUD_INTEGRATION/368c481cd6954bdfa5d0435479fd4eaf/425db2bb73e74783801df7a1d81cacfc.html?locale=en-US).


**Related Information**  


[Integration in Development and Change Management Processes and with Other Services](../70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb "SAP Cloud Transport Management is used to transport content of other cloud services. For the following integrations, more information is available:")

<a name="loio75fe5d4b4fa3492c87ef6be32ea0b819"/>

<!-- loio75fe5d4b4fa3492c87ef6be32ea0b819 -->

## Example: Destination to SAP Cloud Transport Management

The following is a sample configuration of a destination to SAP Cloud Transport Management to transport SAP Cloud Integration content in SAP BTP, Cloud Foundry.

In this example, SAP Content Agent service is used to export the integration content to `.mtar` files and to hand them over to SAP Cloud Transport Management.

The destination contains the connection details to the SAP Cloud Transport Management instance to which SAP Content Agent service sends the exported SAP Cloud Integration content.

You retrieve the required connection details from the service key of the SAP Cloud Transport Management instance that is used for the transport.





### Destination Details

The table contains the details of a destination to SAP Cloud Transport Management for SAP Cloud Integration using SAP Content Agent service for export purposes.

You can use the data in the example to adapt it to your use case.


<table>
<tr>
<th valign="top">

Field

</th>
<th valign="top">

Value

</th>
<th valign="top" colspan="2">

Description

</th>
</tr>
<tr>
<td valign="top">

*Name*

</td>
<td valign="top">

`TransportManagementService` 

</td>
<td valign="top" colspan="2">

Fixed name of the transport destination to SAP Cloud Transport Management.

</td>
</tr>
<tr>
<td valign="top">

*Type*

</td>
<td valign="top">

*HTTP* 

</td>
<td valign="top" colspan="2">

Destination type

</td>
</tr>
<tr>
<td valign="top">

*Description*

</td>
<td valign="top">

Destination to SAP Cloud Transport Management Service

</td>
<td valign="top" colspan="2">

Description for your reference.

This field is optional.

</td>
</tr>
<tr>
<td valign="top">

*URL*

</td>
<td valign="top">

`https://transport-service-app-backend.ts.cfapps.eu10.hana.ondemand.com`

</td>
<td valign="top" colspan="2">

Value of `uri` from the service key of your SAP Cloud Transport Management service instance.

The URL is used to address the SAP Cloud Transport Management instance in the subaccount where it is required.

</td>
</tr>
<tr>
<td valign="top">

*Proxy Type*

</td>
<td valign="top">

*Internet* 

</td>
<td valign="top" colspan="2">

 

</td>
</tr>
<tr>
<td valign="top">

*Authentication* 

</td>
<td valign="top">

*OAuth2ClientCredentials* 

</td>
<td valign="top" colspan="2">

 

</td>
</tr>
<tr>
<td valign="top">

*Client ID* 

</td>
<td valign="top">

`sb-8721drsr-o89j-kl54-bb82-1abc3456u789|alm-ts-backend|i1234`

</td>
<td valign="top">

Value of `clientid` \(`uaa` section\) from the service key of your SAP Cloud Transport Management service instance.

</td>
<td valign="top" rowspan="6">

The details in these fields are required for user authentication and authorization.

The values of `clientid` and `clientsecret` in the `uaa` section basically represent the user used for the destination and the permissions of this user.

The URL in the `uaa` section addresses the authentication service of SAP BTP in the subaccount where you've subscribed to SAP Cloud Transport Management.

The *Token Service URL* value is primarily used for authentication in the user authentication and authorization process. It routes to the authentication service of SAP Business Technology Platform \(SAP BTP\).

When the SAP BTP authentication service receives a request, it verifies the user and the subaccount information. If the verification succeeds, the service generates a token. This token is like a secret identifier that's used to authenticate subsequent requests from the client.

Once a token is generated, subsequent requests or API calls can be made without the need for re-authentication. Overall, the *Token Service URL* value enables secure communication, ensuring that only authenticated requests are processed.

</td>
</tr>
<tr>
<td valign="top">

*Client Secret* 

</td>
<td valign="top">

`nYZdDk9QA3HMjcFTV2icbcCV4zwa`

</td>
<td valign="top">

Value of `clientsecret` \(`uaa` section\) from the service key of your SAP Cloud Transport Management service instance.

</td>
</tr>
<tr>
<td valign="top">

*Token Service URL Type* 

</td>
<td valign="top">

*Dedicated* 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Token Service URL* 

</td>
<td valign="top">

<code>https://<i class="varname">&lt;host&gt;</i>.authentication.eu10.hana.ondemand.com/oauth/token</code>

</td>
<td valign="top">

Value of `url` \(`uaa` section\) from the service key of your SAP Cloud Transport Management service instance.

Append `oauth/token` to the URL retrieved from the service key.

</td>
</tr>
<tr>
<td valign="top">

*Token Service User* 

</td>
<td valign="top">

No inputs required

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Token Service Password* 

</td>
<td valign="top">

No inputs required

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

*Additional Properties* 

</td>
<td valign="top">

`sourceSystemId` = `DEV_NODE`

</td>
<td valign="top" colspan="2">

1.  Choose *New Property*.

2.  As the key, enter `sourceSystemId` \(value is case-sensitive\).

3.  As the value, enter the name that you want to use as the source node of the transport route, for example, `DEV_NODE`.

    Reuse the value as the name of the source transport node later.




</td>
</tr>
</table>



### More Information

Creating a service key for SAP Cloud Transport Management instance and configuring the destination:

-   SAP Cloud Integration documentation on SAP Help Portal: [Enabling Content Transport, Cloud Foundry Enviroment](https://help.sap.com/docs/CLOUD_INTEGRATION/368c481cd6954bdfa5d0435479fd4eaf/452c677debfc4fda904310560ab03743.html?locale=en-US)
-   SAP Content Agent service documentation on SAP Help Portal: [Create TransportManagementService Destination](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/eed66f35f9d148c8ae5b2d46ff097d8c.html?locale=en-US)

