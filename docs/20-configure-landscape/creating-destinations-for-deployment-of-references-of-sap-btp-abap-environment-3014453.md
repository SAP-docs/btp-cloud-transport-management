<!-- loio30144538f2c247be9e1a076754e06bb8 -->

# Creating Destinations for Deployment of References of SAP BTP, ABAP Environment

To address the target end point of the deployment process of references of SAP BTP ABAP environment, create a destination to the target instance of SAP BTP ABAP environment where you want to deploy your content references.



<a name="loio30144538f2c247be9e1a076754e06bb8__prereq_cmy_vrc_pwb"/>

## Prerequisites

In the target instance of SAP BTP ABAP environment, you've created an instance of the communication scenario `SAP_COM_0948` using the *Communication Arrangements* app. For this, you've created a communication system with an inbound communication user that uses *User ID and Password* as the *Authentication Method*.

For more information, see the following topics in the documentation of SAP BTP ABAP environment:

-   [How to Create Communication Users](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/0377adea0401467f939827242c1f4014.html?locale=en-US)
-   [How to Create Communication Systems](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/c2234acd55774ebcbedb66744199273e.html?locale=en-US)
-   [How to Create a Communication Arrangement](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/a0771f6765f54e1c8193ad8582a32edb.html?locale=en-US)

-   [API for Managing Software Components](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/61f4d47af1394b1c8ad684b71d3ad6a0.html?locale=en-US)




<a name="loio30144538f2c247be9e1a076754e06bb8__context_wl5_nn4_4wb"/>

## Context

You can use SAP Cloud Transport Management service to transport references to ABAP coding in Git repositories that was created in SAP BTP ABAP environment.

This topic describes how to create a destination to SAP Cloud Transport Management using the `MANAGE_SOFTWARE_COMPONENTS` API and `SAP_COM_0948`. This is the recommended approach. This API supports the import of all transport requests in an import queue. For selected transport requests, *Import Upto* is available which ensures that all previous transport requests in an import queue are imported together with the selected request.



<a name="loio30144538f2c247be9e1a076754e06bb8__steps_r53_5rs_gwb"/>

## Procedure

1.  In SAP BTP Cockpit of your subaccount in which you are subscribed to SAP Cloud Transport Management, choose *Connectivity* \> *Destinations*.

2.  In the *Destinations* editor, choose *Create* \> *From Scratch* \> *Create*.

3.  Enter or select the following values:

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
    
    Enter the service URL of the inbound service from the communication arrangement created for the `SAP_COM_0948` communication scenario. For more information, see the *Prerequisites* section.

    > ### Example:  
    > <code>https://<i class="varname">&lt;service-instance&gt;</i>.abap.eu10.hana.ondemand.com/sap/opu/odata4/sap/a4c_mswc_api/srvd_a2x/sap/manage_software_components/0001/</code>


    
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
    
    Specify the name of the inbound communication user used for the `SAP_COM_0948` communication arrangement. For more information, see the *Prerequisites* section.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password*
    
    </td>
    <td valign="top">
    
    Specify the password of the inbound communication user used for the `SAP_COM_0948` communication arrangement. For more information, see the *Prerequisites* section.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Use default client truststore*
    
    </td>
    <td valign="top">
    
    This checkbox is selected by default.

    If you leave the checkbox selected, the default client truststore with certificates provided by SAP are used.

    If you want to change this, see [Use Destination Certificates \(Cockpit\)](https://help.sap.com/docs/CP_CONNECTIVITY/b865ed651e414196b39f8922db2122c7/d3dfd5052fb14a15aad87ebcdb2f23e2.html).
    
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




<a name="loio30144538f2c247be9e1a076754e06bb8__postreq_kht_jts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

-   **[\(Deprecated\) Creating Destinations for Deployment of References of SAP BTP, ABAP Environment Using MANAGE\_GIT\_REPOSITORY API and SAP\_COM\_0510](deprecated-creating-destinations-for-deployment-of-references-of-sap-btp-abap-environment-14c6bcd.md "To address the target end point of the deployment process of references of SAP BTP ABAP
                                    environment, create a destination to the target instance of SAP BTP ABAP
                                    environment where you want to deploy your content references.")**  
To address the target end point of the deployment process of references of SAP BTP ABAP environment, create a destination to the target instance of SAP BTP ABAP environment where you want to deploy your content references.

**Related Information**  


[More information about exporting references of SAP BTP, ABAP Environment: How to Export Using SAP Cloud Transport Management](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/b837a3b4226843cb86e8c35d2f35e6fa.html)

[Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](../10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md "Configuration steps for integrating SAP Cloud Transport Management with other SAP cloud solutions are determined by the type of content being transported and how the integration was realized. Get an overview of known integrations and links to further information.")

