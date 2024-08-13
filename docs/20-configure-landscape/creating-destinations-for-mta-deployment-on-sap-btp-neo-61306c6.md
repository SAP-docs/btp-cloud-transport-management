<!-- loio61306c6ebcb046c2b45ed37bce1afc5a -->

# Creating Destinations for MTA Deployment on SAP BTP, Neo

To address the target end point of MTA deployment on SAP BTP, Neo, specify the URL to the SAP Solution Lifecycle Management service as the deploy end point of the destination.



## Procedure

1.  In SAP BTP Cockpit of your subaccount, choose *Connectivity* \> *Destinations* \> *New Destination*.

2.  Enter the following values:

    **Destination Settings for MTA Deployment on Neo**


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
    <td valign="top" rowspan="3">
    
    -   SAP BTP, Neo: [Configure Destinations from the Cockpit](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/60735ad11d8a488c83537cdcfb257135.html)

    -   [Create HTTP Destinations](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/1e110da0ddd8453aaf5aed2485d84f25.html)


    
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
    
    Specify the URL to the SAP Solution Lifecycle Management service in the following format:

    <code>https://slservice.<i class="varname">&lt;landscape-host&gt;</i>/slservice/slp/basic/<i class="varname">&lt;Technical Name of the Neo subaccount&gt;</i>/slp</code>

    Example: `https://slservice.eu1.hana.ondemand.com/slservice/slp/basic/a123c4567b/slp`
    
    </td>
    <td valign="top">
    
    [Configuring the Access to the Solution Lifecycle Management Service](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/b15a6c5c6c97475f8297f83f83dd4e31.html) 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    *Internet*
    
    </td>
    <td valign="top">
    
    -   SAP BTP, Neo: [Configure Destinations from the Cockpit](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/60735ad11d8a488c83537cdcfb257135.html)

    -   [Create HTTP Destinations](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/1e110da0ddd8453aaf5aed2485d84f25.html)


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    Select *BasicAuthentication*.
    
    </td>
    <td valign="top" rowspan="3">
    
    [Client Authentication Types for HTTP Destinations](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/4e13a04147314e8e9e54321f25d93fdc.html?locale=en-US)
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *User*
    
    </td>
    <td valign="top">
    
    Specify the name of the platform user that is used for the deployment.

    > ### Note:  
    > The user must be a valid user on Neo environment and must have one of the roles as described under [Operating Solutions](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/2abf7d47063542208d0d99f7bc05f4f4.html).
    > 
    > Note that the user used for the destination isn’t subject to any Data Protection and Privacy requirements.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password*
    
    </td>
    <td valign="top">
    
    Specify the password of the platform user.
    
    </td>
    </tr>
    </table>
    
3.  Choose *Save* to save your changes.

    > ### Note:  
    > If you use *Check Connection* to check your destination, the connection test may give the wrong response \(*Connection not ok*\) even though the destination was correctly configured.
    > 
    > It only gives the correct results for *Basic Authentication*.




<a name="loio61306c6ebcb046c2b45ed37bce1afc5a__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

