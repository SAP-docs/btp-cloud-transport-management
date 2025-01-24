<!-- loio14c6bcdca5ed4065a6789f1e063340fb -->

# \(Deprecated\) Creating Destinations for Deployment of References of SAP BTP, ABAP Environment Using `MANAGE_GIT_REPOSITORY` API and `SAP_COM_0510`

To address the target end point of the deployment process of references of SAP BTP ABAP environment, create a destination to the target instance of SAP BTP ABAP environment where you want to deploy your content references.



<a name="loio14c6bcdca5ed4065a6789f1e063340fb__prereq_cmy_vrc_pwb"/>

## Prerequisites

In the target instance of SAP BTP ABAP environment, you've created an instance of the communication scenario `SAP_COM_0510` using the *Communication Arrangements* app. For this, you've created a communication system with an inbound communication user that uses *User ID and Password* as the *Authentication Method*.

For more information, see the following topics in the documentation of SAP BTP ABAP environment:

-   [How to Create Communication Users](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/0377adea0401467f939827242c1f4014.html?locale=en-US)
-   [How to Create Communication Systems](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/c2234acd55774ebcbedb66744199273e.html?locale=en-US)
-   [How to Create a Communication Arrangement](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/a0771f6765f54e1c8193ad8582a32edb.html?locale=en-US)

-   [Test Integration \(SAP\_COM\_0510\)](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/b04a9ae412894725a2fc539bfb1ca055.html?locale=en-US&)

-   [API to Manage Git Repositories](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/c45f01f6589f4eefafc34d3ad71e6eb5.html?locale=en-US)




<a name="loio14c6bcdca5ed4065a6789f1e063340fb__context_wl5_nn4_4wb"/>

## Context

You can use SAP Cloud Transport Management service to transport references to ABAP coding in Git repositories that was created in SAP BTP ABAP environment.

> ### Note:  
> This topic describes how to create a destination to SAP Cloud Transport Management using the `MANAGE_GIT_REPOSITORIES` API and `SAP_COM_0510`. This is no longer the recommended approach. The communication scenario `SAP_COM_0510` is deprecated. This API supports the import of individual transport requests only. We recommend that you create a destination as described in [Creating Destinations for Deployment of References of SAP BTP, ABAP Environment](creating-destinations-for-deployment-of-references-of-sap-btp-abap-environment-3014453.md).
> 
> If you are already using SAP Cloud Transport Management to transport references of type *BTP ABAP*, you can continue to use them with the current limitations for the duration of the deprecation phase. However, we recommend that you transition to the new API.



<a name="loio14c6bcdca5ed4065a6789f1e063340fb__steps_r53_5rs_gwb"/>

## Procedure

1.  In SAP BTP Cockpit of your subaccount in which you are subscribed to SAP Cloud Transport Management, choose *Connectivity* \> *Destinations* \> *New Destination*.

2.  Enter the following values:

    **Destination Settings for Deployment of References of SAP BTP ABAP environment**


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
    <td valign="top" rowspan="9">
    
    [Using the Destinations Editor in the Cockpit](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/565fdb3dd19d4cda80864341dc5a0451.html)
    
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
    
    The description is optional.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    Enter the service URL of the inbound service *Git Repository - Manage* from the communication arrangement created for the `SAP_COM_0510` communication scenario. For more information, see the *Prerequisites* section.

    > ### Example:  
    > <code>https://<i class="varname">&lt;service-instance&gt;</i>.abap.eu10.hana.ondemand.com/sap/opu/odata/sap/MANAGE_GIT_REPOSITORY</code>


    
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
    
    *BasicAuthentication* 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *User*
    
    </td>
    <td valign="top">
    
    Specify the name of the inbound communication user used for the `SAP_COM_0510` communication arrangement. For more information, see the *Prerequisites* section.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password*
    
    </td>
    <td valign="top">
    
    Specify the password of the inbound communication user used for the `SAP_COM_0510` communication arrangement. For more information, see the *Prerequisites* section.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Use default JDK truststore*
    
    </td>
    <td valign="top">
    
    This checkbox is selected by default.

    If you leave the checkbox selected, the default JDK truststore with certificates provided by SAP are used.

    If you want to change this, see [Use Destination Certificates \(Cockpit\)](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/d3dfd5052fb14a15aad87ebcdb2f23e2.html).
    
    </td>
    </tr>
    </table>
    
3.  Choose *Save* to save your changes.

4.  Use *Check Connection* to check your destination.




<a name="loio14c6bcdca5ed4065a6789f1e063340fb__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

