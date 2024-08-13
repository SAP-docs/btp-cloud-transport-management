<!-- loio23bb29cbc7ee47e4acfd6a7b3a81808a -->

# Creating Destinations for Deployment of Application Content Transported in an Application-Specific Format

To address the target end point of application-specific content deployment, specify a destination using the details from the provider of the application content.



## Procedure

1.  In SAP BTP Cockpit of your subaccount, choose *Connectivity* \> *Destinations* \> *New Destination*.

2.  Enter the following values:

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
    
3.  Choose *Save* to save your changes.

    > ### Caution:  
    > If you use *Check Connection* to check your destination: The check doesn't provide correct results for destinations using any authentication other than Basic authentication, for example OAuth2ClientCredentials authentication. It's possible that the check displays an error, even though the destination was configured correctly. It only gives the correct results for Basic authentication.
    > 
    > We recommend that you test the deployment using a test transport after completing all configuration steps.




<a name="loio23bb29cbc7ee47e4acfd6a7b3a81808a__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

