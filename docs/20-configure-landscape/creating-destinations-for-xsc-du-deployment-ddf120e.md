<!-- loioddf120eafed748a3b17da92064ac0878 -->

# Creating Destinations for XSC DU Deployment

Specify <code>https://<i class="varname">&lt;host&gt;</i>/sap/hana/xs/lm/slp/slp.xsjs</code> as the deploy end point of the destination.



## Procedure

1.  In SAP BTP Cockpit of your subaccount, choose *Connectivity* \> *Destinations* \> *New Destination*.

2.  Enter the following values:

    **Destination Settings for XSC DU Deployment**


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
    
    Specify the URL in the following format: <code>https://<i class="varname">&lt;host&gt;</i>/sap/hana/xs/lm/slp/slp.xsjs</code>

    Example: `https://demoabcd12345.hana.ondemand.com/sap/hana/xs/lm/slp/slp.xsjs`

    You can find the host of the SAP HANA database in the URL, if you choose *Administration Tools: SAP HANA Cockpit*, or in the SAP HANA Web-based Development Workbench.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    *Internet*
    
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

4.  Use *Check Connection* to check your destination.




<a name="loioddf120eafed748a3b17da92064ac0878__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

