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

-   **SAP BTP***Service / SAP Cloud Solution*: SAP BTP Service or SAP Cloud Solution in which content is developed.
-   *Content*: Application-specific content and development artifacts to be transported.
-   *Environment*: SAP BTP environment where the content is created, either *SAP BTP ABAP environment*, *Cloud Foundry*, or *Neo*.
-   *Content Type*: Entity to transport that you can select when you create a new node in SAP Cloud Transport Management.
-   *Design Time Integration*: Can the transport be triggered directly in the design time tool of the application where the content is produced?
-   *Content Agent Service*: Is the integration with SAP Cloud Transport Management realized using SAP Content Agent service? \(Cloud Foundry only\)
-   *Solution Export Wizard*: Is the integration with SAP Cloud Transport Management realized using Solution Export Wizard? \(Neo only\)
-   *Continuous Integration \(CI\) Pipeline Upload*: Is there a CI pipeline template available with the option of uploading content to SAP Cloud Transport Management?

    For more information about integration into CI pipelines, see the links to *More Information* listed in the *Integration Scenario*: [Receiving transports comprising release candidates qualified by automated pipelines in SAP Continuous Integration and Delivery service](70-integrations/extended-integration-scenarios-7e966f7.md#loio1b3c6637adb54d4bbb1828f911bb9547__cicd), in particular the series of tutorial videos.

-   *More Information about the Integration*: Link to more information about the integration with SAP Cloud Transport Management in the relevant section of: [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md), where more information is available.

**Table: Content Supported by SAP Cloud Transport Management**


<table>
<tr>
<th valign="top">

SAP BTP Service / SAP Cloud Solution

</th>
<th valign="top">

Content

</th>
<th valign="top">

Content Type

</th>
<th valign="top">

Environment

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

SAP BTP, Cloud Foundry Runtime

</td>
<td valign="top">

HTML5 apps

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/c8bee32a24a7430c8d1803fbc95f855c.html) in the SAP BTP, Cloud Foundry documentation

</td>
</tr>
<tr>
<td valign="top">

Joule Studio in SAP Build

</td>
<td valign="top">

Joule Studio projects \(including Joule skills\)

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes \(for import and export\)

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

[Joule Studio](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__joule)

</td>
</tr>
<tr>
<td valign="top">

SAP Analytics Cloud

</td>
<td valign="top">

Content network packages

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry / Neo

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

[SAP Analytics Cloud](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__analytics)

</td>
</tr>
<tr>
<td valign="top">

SAP API Management

</td>
<td valign="top">

API artifacts

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

[SAP API Management](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__api)

</td>
</tr>
<tr>
<td valign="top">

SAP Asset Performance Management

</td>
<td valign="top">

-   Communication system configurations
-   Coding masks
-   Risk and criticality assessment templates
-   Strategy assessment templates for classes, including associated recommendations



</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Asset Performance Management](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__apm)

</td>
</tr>
<tr>
<td valign="top">

SAP Batch Release Hub for Life Sciences

</td>
<td valign="top">

Configuration settings

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Batch Release Hub for Life Sciences](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__brh4ls)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Apps \(part of SAP Build\)

</td>
<td valign="top">

Projects

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

[SAP Build Apps](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__build_apps)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Process Automation

</td>
<td valign="top">

Projects

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

[SAP Build Process Automation](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__build_pa)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Work Zone, advanced edition

</td>
<td valign="top">

Content

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Build Workzone, advanced edition](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__wz)

</td>
</tr>
<tr>
<td valign="top">

SAP Build Work Zone, standard edition

</td>
<td valign="top">

Content

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Build Workzone, standard edition](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__lps)

</td>
</tr>
<tr>
<td valign="top">

SAP BTP ABAP environment

</td>
<td valign="top">

References to SAP BTP ABAP environment content

</td>
<td valign="top">

BTP ABAP

</td>
<td valign="top">

SAP BTP ABAP environment

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

[SAP BTP, ABAP Environment](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__btp_abap)

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Cloud Foundry Runtime

</td>
<td valign="top">

Java apps

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/c8bee32a24a7430c8d1803fbc95f855c.html) in the SAP BTP, Cloud Foundry documentation

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Cloud Foundry Runtime

</td>
<td valign="top">

NodeJs apps

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/c8bee32a24a7430c8d1803fbc95f855c.html) in the SAP BTP, Cloud Foundry documentation

</td>
</tr>
<tr>
<td valign="top">

SAP Datasphere

</td>
<td valign="top">

Content packages

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Datasphere](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__datasphere)

</td>
</tr>
<tr>
<td valign="top">

SAP Destination Service

</td>
<td valign="top">

Destinations

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

[SAP Content Agent Service](70-integrations/extended-integration-scenarios-7e966f7.md#loio1b3c6637adb54d4bbb1828f911bb9547__cas)

</td>
</tr>
<tr>
<td valign="top">

SAP Digital Manufacturing

</td>
<td valign="top">

Production process designs

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Digital Manufacturing](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__dmc)

</td>
</tr>
<tr>
<td valign="top">

SAP Entitlement Management

</td>
<td valign="top">

Configuration content

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Entitlement Management](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__entitlement)

</td>
</tr>
<tr>
<td valign="top">

SAP Excise Tax Management

</td>
<td valign="top">

Warehouses

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Excise Tax Management](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__etm)

</td>
</tr>
<tr>
<td valign="top">

SAP Group Reporting Data Collection

</td>
<td valign="top">

Forms and folders

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Group Reporting Data Collection for SAP S/4HANA](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__grdc)

</td>
</tr>
<tr>
<td valign="top">

SAP HANA Deployment Infrastructure \(HDI\)

</td>
<td valign="top">

HDI content

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

SAP Integration Suite

</td>
<td valign="top">

Integration packages \(integration flows, value mappings, APIs\)

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Cloud Foundry

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

Using the [SAP Integration Suite](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cloud_integration) UI

</td>
<td valign="top">

[SAP Integration Suite](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cloud_integration)

</td>
</tr>
<tr>
<td valign="top">

SAP Intelligent Clinical Supply Management

</td>
<td valign="top">

Configuration settings

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Intelligent Clinical Supply Management](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__icsm)

</td>
</tr>
<tr>
<td valign="top">

SAP Mobile Services

</td>
<td valign="top">

Application configurations

</td>
<td valign="top">

MTA

</td>
<td valign="top">

 

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

[SAP Mobile Services](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__mobile)

</td>
</tr>
<tr>
<td valign="top">

SAP Profitability and Performance Management Cloud Standard Model

</td>
<td valign="top">

Environments

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

[SAP Profitability and Performance Management Cloud](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__papm)

</td>
</tr>
<tr>
<td valign="top">

SAP Risk and Assurance Management

</td>
<td valign="top">

In-house business content \(controls, automated procedures, manual procedures and regulations\)

</td>
<td valign="top">

Application Content

</td>
<td valign="top">

Cloud Foundry

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

The *Manage Business Content Packages* app is used to activate and transport in-house business content packages.

</td>
<td valign="top">

[SAP Risk and Assurance Management](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__GRCFC)

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

Authorization groups

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

Destinations

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

HTML5 apps

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

HTML 5 roles

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

Java apps

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP Integration Suite

</td>
<td valign="top">

Content

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

[SAP Integration Suite](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md#loioddaa000bc92c43d8bd09f4e2c8ca05eb__cloud_integration)

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

SAP Fiori apps

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

SAP Fiori Portal

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP BTP, Neo application runtime

</td>
<td valign="top">

SAP Fiori roles

</td>
<td valign="top">

MTA

</td>
<td valign="top">

Neo

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

Content is developed and transported as part of another application.

</td>
<td valign="top">

Specific information: See the documentation of the application.

General information: [Integration with Transport Management Tools](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/905baea4d6c7404290bff6c042184b4e.html) in the SAP BTP, Neo documentation.

</td>
</tr>
<tr>
<td valign="top">

SAP HANA XS classic model

</td>
<td valign="top">

Delivery units \(DU\)

</td>
<td valign="top">

XSC DU

</td>
<td valign="top">

Neo

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
-   For more information about the integration of specific content in SAP Cloud Transport Management, see [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md).


