<!-- loio23bb29cbc7ee47e4acfd6a7b3a81808a -->

# Creating Destinations for Deployment of Application Content Transported in an Application-Specific Format

To address the target end point of application-specific content deployment, specify a destination using the details from the provider of the application content.



## Procedure

1.  In SAP BTP Cockpit of your subaccount, choose *Connectivity* \> *Destinations*.

2.  In the *Destinations* editor, choose *Create* \> *From Scratch* \> *Create*.

3.  Enter or select the following values:

    **Destination Settings for Application Content Transported in an Application-Specific Format**


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Description
    
    </th>
    <th valign="top">

    More Information
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Name of the destination
    
    </td>
    <td valign="top" rowspan="5">
    
    -   SAP BTP, Cloud Foundry: [Using the Destinations Editor in the Cockpit](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/565fdb3dd19d4cda80864341dc5a0451.html) 
    -   SAP BTP, Neo: [Configure Destinations from the Cockpit](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/60735ad11d8a488c83537cdcfb257135.html)


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Type*
    
    </td>
    <td valign="top">
    
    *HTTP*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Description*
    
    </td>
    <td valign="top">
    
    The description of the destination is optional.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    The application specifies a URL to the deploy end point of the destination as well as the other details of the destination.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    Please use the authentication type required by the deploying application, for example, *OAuth2ClientCredentials* authentication with a client credential flow. Here, you have to configure a destination with authentication *OAuth2ClientCredentials* where the *Client ID* and the *Client Secret* are needed that you get from the application or service instance created in the target tenant. In addition, you have to specify the *Token Service URL*, pointing to the authentication service used, for example `https://ts.authentication.sap.hana.ondemand.com`, which is also provided by the application or service instance created in the target tenant.
    
    </td>
    </tr>
    </table>
    
4.  Choose *Create* to create the destination.

5.  **Optional:** After creating the destination, click anywhere in the row to display its details.

6.  **Optional:** Choose *Check Connection* to check your destination.

    The result should display *HTTP request \(without authentication\) to *<Name of the destination\>* destination succeeded*.

    > ### Note:  
    > This result means that the URL specified in the destination can be reached. However, such a successful check doesn’t guarantee successful deployment. We recommend that you test the deployment using a test transport after completing all configuration steps required for your transport scenario.
    > 
    > For more information about connection checks, see [Check the Availability of a Destination](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/71ea3ccf4ebc4c63a3989c0b318e3e9b.html).




<a name="loio23bb29cbc7ee47e4acfd6a7b3a81808a__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

