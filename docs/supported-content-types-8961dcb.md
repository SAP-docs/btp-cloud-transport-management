<!-- loio8961dcb3edc84a76b84b29565833067b -->

# Supported Content Types

SAP Cloud Transport Management service can be used to transport the following entities, called content types:



-   **Multitarget Application** archives \(MTAs -`.mtar` files\) between different spaces in SAP BTP subaccounts

    MTAs can consist of a cloud application itself, or content created in a cloud application, which you want to transport between two subaccounts. For example, SAP Cloud Integration content is packaged and transported as an MTA.

    > ### Restriction:  
    > Transporting MTAs without modules is not supported.

-   **BTP ABAP**: references to ABAP objects in a Git repository between different SAP BTP ABAP environment instances. A reference can consist of the name of the software component, the commit ID, the branch name, and the tag name. When a reference of type *BTP ABAP* is imported, the referenced content of the Git repository is pulled to the target instance.
-   **Application content** transported in an application-specific format between different cloud subaccounts and tenants

    In general, application content is packed in archive files, for example, `.zip` files, or `.rar` files. The archives can contain any kind of application-specific content. The application that has created such an archive file must provide a method to deploy the application-specific content into the target environment. This means, such an archive file can only be used for transport if the application-specific deployment service in the target environment is able to handle it. For more information, see the documentation of the individual applications.

-   **Delivery units** \(DUs\) of SAP HANA XS classic model between different SAP HANA instances that are assigned to cloud subaccounts

These content types \(files or references\) can be transported in one of the following scenarios:

-   Directly from within another application
-   They are uploaded from a Continuous Integration pipeline.
-   They are available on local file systems.

<a name="loio0dccbb6ee1714240b9b9bedc1a240a7e"/>

<!-- loio0dccbb6ee1714240b9b9bedc1a240a7e -->

## Overview: Supported Content

The table contains a list of development artifacts and application-specific content that can be transported using SAP Cloud Transport Management service.

The table contains the following information:

-   *Content*: Application-specific content and development artifacts to be transported.

-   *Environment*: SAP BTP environment where the content is created, either *SAP BTP ABAP environment*, *Cloud Foundry*, or *Neo*.
-   *Content Type*: Entity to transport that you can select when you create a new node in SAP Cloud Transport Management. See [Supported Content Types](supported-content-types-8961dcb.md#loio8961dcb3edc84a76b84b29565833067b).
-   *Design Time Integration*: Can the transport be triggered directly in the design time tool of the application where the content is produced?
-   *Content Agent Service*: Is the integration with SAP Cloud Transport Management realized using SAP Content Agent service? \(Cloud Foundry only\)
-   *Solution Export Wizard*: Is the integration with SAP Cloud Transport Management realized using Solution Export Wizard? \(Neo only\)
-   *Continuous Integration \(CI\) Pipeline Upload*: Is there a CI pipeline template available with the option of uploading content to SAP Cloud Transport Management?

    For more information about integration into CI pipelines, see the links to *More Information* listed in the *Integration Scenario*: [Receiving transports comprising release candidates qualified by automated pipelines in SAP Continuous Integration and Delivery service](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cicd), in particular the series of tutorial videos.

-   *More Information about the Integration*: Link to more information about the integration with SAP Cloud Transport Management in the relevant section of:[Integration in Development and Change Management Processes and with Other Services](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb), where more information is available.

**Table: Content Supported by SAP Cloud Transport Management**


<table>
<tr>
<th valign="top">

Content

</th>
<th valign="top">

Environment

</th>
<th valign="top">

Content Type

</th>
<th valign="top">

Design Time Integration

</th>
<th valign="top">

Content Agent Service

</th>
<th valign="top">

Solution Export Wizard

</th>
<th valign="top">

CI Pipeline Upload

</th>
<th valign="top">

Remarks

</th>
<th valign="top">

More Information about the Integration

</th>
</tr>
<tr>
<td valign="top">

Reference to SAP BTP ABAP environment content

</td>
<td valign="top">

SAP BTP ABAP environment

</td>
<td valign="top">

BTP ABAP

</td>
<td valign="top">

Yes

</td>
<td valign="top">

n/a

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Export to SAP Cloud Transport Management takes place using the *Manage Software Components* app.

</td>
<td valign="top">

[SAP BTP, ABAP Environment](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__btp_abap)

</td>
</tr>
<tr>
<td valign="top">

API Management content

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes \(for content selection and deployment\)

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Using API management UI

</td>
<td valign="top">

[SAP API Management](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__api)

</td>
</tr>
<tr>
<td valign="top">

Destination

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

Yes

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Using the integration of SAP Destination Service in SAP Content Agent service. Note that secrets and passwords are not transported.

</td>
<td valign="top">

[SAP Content Agent Service](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cas)

</td>
</tr>
<tr>
<td valign="top">

HTML5 app

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Java app

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

NodeJs app

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

SAP Build Apps projects

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes \(for export and import\)

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Build Apps](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__build_apps)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Process Automation projects

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes \(for export and import\)

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Build Process Automation](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__build_pa)

</td>
</tr>
<tr>
<td valign="top">

SAP Cloud Integration content

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes \(for content selection and deployment\)

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Using SAP Cloud Integration UI

</td>
<td valign="top">

[SAP Cloud Integration](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cloud_integration)

</td>
</tr>
<tr>
<td valign="top">

SAP HANA Deployment Infrastructure \(HDI\) content

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

SAP Analytics Cloud \(content network packages\)

</td>
<td valign="top">

Cloud Foundry / Neo

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Analytics Cloud](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__analytics)

</td>
</tr>
<tr>
<td valign="top">

SAP Batch Release Hub for Life Sciences \(configuration settings\)

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Export to SAP Cloud Transport Management takes place using the *Transport Configuration Settings* app.

</td>
<td valign="top">

[SAP Batch Release Hub for Life Sciences](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__brh4ls)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Work Zone, advanced edition content

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Using the integration of SAP Build Work Zone, standard edition in SAP Build Work Zone, advanced edition

</td>
<td valign="top">

[SAP Build Workzone, advanced edition](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__wz)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Work Zone, standard edition content

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Build Workzone, standard edition](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__lps)

</td>
</tr>
<tr>
<td valign="top">

SAP Datasphere \(content packages\)

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Datasphere](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__datasphere)

</td>
</tr>
<tr>
<td valign="top">

SAP Entitlement Management \(configuration content\)

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Entitlement Management](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__entitlement)

</td>
</tr>
<tr>
<td valign="top">

SAP Excise Tax Management \(warehouses\)

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Warehouse address details are not transported with a warehouse. They must be maintained in the *Address Types for Warhouses* app.

</td>
<td valign="top">

[SAP Excise Tax Management](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__etm)

</td>
</tr>
<tr>
<td valign="top">

SAP Group Reporting Data Collection \(forms and folders\)

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

In the *Manage Packages* app, forms and folders can be exported to SAP Cloud Transport Management.

</td>
<td valign="top">

[SAP Group Reporting Data Collection for SAP S/4HANA](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__grdc)

</td>
</tr>
<tr>
<td valign="top">

SAP Intelligent Clinical Supply Management \(configuration settings\)

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

Export to SAP Cloud Transport Management takes place using the *Transport Configuration Settings* app.

</td>
<td valign="top">

[SAP Intelligent Clinical Supply Management](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__icsm)

</td>
</tr>
<tr>
<td valign="top">

SAP Mobile Services application configurations

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

Yes

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Mobile Services](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__mobile)

</td>
</tr>
<tr>
<td valign="top">

Authorization group

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Destination

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

HTML5 app

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

HTML 5 role

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Java app

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

SAP Cloud Integration content

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Yes

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

[SAP Cloud Integration](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cloud_integration)

</td>
</tr>
<tr>
<td valign="top">

SAP Fiori app

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

SAP Fiori Portal

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

Only complete Portal sites

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

SAP Fiori role

</td>
<td valign="top">

Neo

</td>
<td valign="top">

MTA

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Delivery unit \(DU\) of SAP HANA XS classic model

</td>
<td valign="top">

Neo

</td>
<td valign="top">

XSC DU

</td>
<td valign="top">

No

</td>
<td valign="top">

n/a

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
<td valign="top">

On Delivery Unit \(DU\) level

</td>
<td valign="top">

 

</td>
</tr>
</table>



<a name="loio0dccbb6ee1714240b9b9bedc1a240a7e__section_yrc_5vk_5cb"/>

## More Information

-   [Multitarget Applications in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/d04fc0e2ad894545aebfd7126384307c.html)
-   [Multitarget Applications for the Neo Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/e1bb7eb746d34237b8b47035adff5022.html)
-   For more information about the integration of specific content in SAP Cloud Transport Management, see [Integration in Development and Change Management Processes and with Other Services](70-integrations/integrating-the-service-7e966f7.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb).


