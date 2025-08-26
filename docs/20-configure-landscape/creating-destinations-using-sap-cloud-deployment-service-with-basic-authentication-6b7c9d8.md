<!-- loio6b7c9d89023b43f9a72e881816eb5c52 -->

# Creating Destinations Using SAP Cloud Deployment Service with Basic Authentication

To address the target end point of the deployment process of MTA Deployment on Cloud Foundry, you can create a destination to SAP Cloud Deployment service with classic *Basic* authentication.



<a name="loio6b7c9d89023b43f9a72e881816eb5c52__steps_tyj_zrs_gwb"/>

## Procedure

1.  In SAP BTP Cockpit of your subaccount, choose *Connectivity* \> *Destinations*.

2.  In the *Destinations* editor, choose *Create* \> *From Scratch* \> *Create*.

3.  Enter or select the following values:

    **MTA Deployment on Cloud Foundry with Classic Basic Authentication**


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
    <td valign="top" rowspan="4">
    
    SAP BTP, Cloud Foundry: [Using the Destinations Editor in the Cockpit](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/565fdb3dd19d4cda80864341dc5a0451.html)
    
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
    
    Specify the URL to the SAP Cloud Deployment service as the deploy end point of the destination. To address the SAP Cloud Deployment service, you have the following options:

    -   **Using the names of your org and space**

        <code>https://deploy-service.cf.<i class="varname">&lt;domain&gt;</i>/slprot/<i class="varname">&lt;myorg&gt;</i>/<i class="varname">&lt;myspace&gt;</i>/slp</code>

        -   <code><i class="varname">&lt;domain&gt;</i></code>: Domain of your target subaccount

            The domain is derived from the Cloud Foundry API endpoint that you can find in the SAP BTP Cockpit in the *Overview* of your subaccount.

        -   <code><i class="varname">&lt;myorg&gt;</i>/<i class="varname">&lt;myspace&gt;</i></code>: Names of your org and space

            > ### Note:  
            > You need to escape special characters in your org and space name \(*<myorg\>*/*<myspace\>*\) with a proper URL encoding. For example, replace space characters with `%20`, and commas with `%2C`.


        > ### Example:  
        > -   Sample URL for the Cloud Foundry API endpoint: `api.cf.eu10-004.hana.ondemand.com`, <code><i class="varname">&lt;myorg&gt;</i></code>: `TestOrg`, and <code><i class="varname">&lt;myspace&gt;</i></code>: `TestSpace`:
        > 
        >     `https://deploy-service.cf.eu10-004.hana.ondemand.com/slprot/TestOrg/TestSpace/slp`
        > 
        > -   Sample URL with URL encoding for <code><i class="varname">&lt;myorg&gt;</i></code>: `Example Company Test Org` and <code><i class="varname">&lt;myspace&gt;</i></code>: `Example Company Test Space`:
        > 
        >     `https://deploy-service.cf.eu10-004.hana.ondemand.com/slprot/Example%20Company%20Test%20Org/Example%20Company%20Test%20Space/slp`

    -   **Using the GUID of your space**

        <code>https://deploy-service.cf.<i class="varname">&lt;domain&gt;</i>/slprot/<i class="varname">&lt;my-space-guid&gt;</i>/slp</code>

        -   <code><i class="varname">&lt;domain&gt;</i></code>: Domain of your subaccount

            The domain is derived from the Cloud Foundry API endpoint that you can find in the SAP BTP Cockpit in the *Overview* of your subaccount.

        -   <code><i class="varname">&lt;my-space-guid&gt;</i></code>: GUID of your space

            To retrieve the GUID of your space, use the Cloud Foundry Command Line Interface \(cf CLI\). Log on to your org, and execute the following command: `cf space <my-space-name> --guid`.


        > ### Example:  
        > Sample URL for the Cloud Foundry API endpoint: `api.cf.eu10-004.hana.ondemand.com` and <code><i class="varname">&lt;my-space-guid&gt;</i></code>: `977a24d6-2eaf-432d-a3e1-5294451551a3`:
        > 
        > `https://deploy-service.cf.eu10-004.hana.ondemand.com/slprot/977a24d6-2eaf-432d-a3e1-5294451551a3/slp`



    
    </td>
    <td valign="top">
    
    More information about regions and API endpoints:

    -   [Deploying Applications in Regions](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/350356d1dc314d3199dca15bd2ab9b0e.html?locale=en-US#deploying-applications-in-regions)

    -   [Regions and API Endpoints Available for the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/f344a57233d34199b2123b9620d0bb41.html?locale=en-US).


    More information about cf CLI:

    -   [Working with the Cloud Foundry Command Line Interface](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/2f1d4abd0f9f4760a301f43513d2efa6.html?locale=en-US)



    
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
    
    Specify the user name \(usually, an email address\) of the user that is used for the deployment.

    > ### Note:  
    > -   The user used for the destination must be a valid user on Cloud Foundry environment and it must have the role `SpaceDeveloper` in the target space.
    > 
    > -   The user must be a platform user so that the deployment works for all content types. For more information, see [Platform Users](https://help.sap.com/docs/btp/sap-business-technology-platform/platform-users).
    > 
    > -   The user used for the destination isn’t subject to any Data Protection and Privacy requirements.
    > 
    > -   We recommend that you use a technical user to avoid constraints typically associated with personal users, such as password rotation.

    > ### Restriction:  
    > Basic Authentication only works with users provided by SAP ID. It does not work with custom IAS tenant users. If you want to use a custom identity provider for the platform user used for the deployment, you must use OAuth2Password authentication for the destination. For more information, see [Creating Destinations Using SAP Cloud Deployment Service with OAuth2Password Authentication](creating-destinations-using-sap-cloud-deployment-service-with-oauth2password-authenticati-a26a721.md).


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password*
    
    </td>
    <td valign="top">
    
    Specify the password of the user.
    
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




<a name="loio6b7c9d89023b43f9a72e881816eb5c52__postreq_c2b_3ts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

