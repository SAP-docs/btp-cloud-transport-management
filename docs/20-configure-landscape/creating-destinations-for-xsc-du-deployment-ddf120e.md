<!-- loioddf120eafed748a3b17da92064ac0878 -->

# Creating Destinations for XSC DU Deployment

Specify <code>https://<i class="varname">&lt;host&gt;</i>/sap/hana/xs/lm/slp/slp.xsjs</code> as the deploy end point of the destination.



## Procedure

1.  In SAP BTP Cockpit of your subaccount, choose *Connectivity* \> *Destinations*.

2.  In the *Destinations* editor, choose *Create* \> *From Scratch* \> *Create*.

3.  Enter or select the following values:

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
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    *Internet*
    
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
    
4.  Choose *Create* to create the destination.

5.  **Optional:** After creating the destination, click anywhere in the row to display its details.

6.  **Optional:** Choose *Check Connection* to check your destination.

    The result should display *HTTP request \(without authentication\) to *<Name of the destination\>* destination succeeded*.

    > ### Note:  
    > This result means that the URL specified in the destination can be reached. However, such a successful check doesn’t guarantee successful deployment. We recommend that you test the deployment using a test transport after completing all configuration steps required for your transport scenario.
    > 
    > For more information about connection checks, see [Check the Availability of a Destination](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/71ea3ccf4ebc4c63a3989c0b318e3e9b.html).




<a name="loioddf120eafed748a3b17da92064ac0878__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

