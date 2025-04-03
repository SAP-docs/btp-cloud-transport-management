<!-- loio3e7b04236d804a4eb80e42c6360209f1 -->

# Configuring the Landscape

Before you can use SAP Cloud Transport Management service to transport cloud applications or application content \(such as SAP Integration Suite content, for example\) between different environments, you must configure your landscape for transports.

You can use SAP Cloud Transport Management to transport content archives directly from within an application's source environment to a target environment. In this case, SAP Cloud Transport Management service must be configured to integrate with another application whose content archives you want to transport. You can then use SAP Cloud Transport Management to import the content archives in the target environments of the application.

The configuration involves the following steps:



![](images/Image_Map_MTA_attachment_with_TMS_d1c42a2.png)



> ### Note:  
> If there's no export integration of SAP Cloud Transport Management available in the source environment, you can use the service to upload content archives from a local file system and import them in a target environment. In this case, you don't need to create a destination to the service.

-   **[Sample Configuration Scenario](sample-configuration-scenario-22e1ed6.md "The following sample configuration describes a scenario where you start the transport of
		content archives directly in your application or service.")**  
The following sample configuration describes a scenario where you start the transport of content archives directly in your application or service.
-   **[Create Transport Destinations](create-transport-destinations-c9905c1.md "In SAP Cloud Transport Management service, transport destinations are used to address the target end
		point of a deployment process. ")**  
In SAP Cloud Transport Management service, transport destinations are used to address the target end point of a deployment process.
-   **[Create Transport Nodes](create-transport-nodes-f71a4d5.md "Create transport nodes as representations of the source and target end points of
		deployment processes in your landscape. Add configuration details as required. ")**  
Create transport nodes as representations of the source and target end points of deployment processes in your landscape. Add configuration details as required.
-   **[Create Transport Routes](create-transport-routes-dddb749.md "In SAP Cloud Transport Management, transport routes
		are used to connect transport nodes.")**  
In SAP Cloud Transport Management, transport routes are used to connect transport nodes.
-   **[Use the Transport Landscape Wizard](use-the-transport-landscape-wizard-f14192e.md "You can use the Transport Landscape Wizard to configure the transport nodes and
		transport routes of simple transport landscapes.")**  
You can use the Transport Landscape Wizard to configure the transport nodes and transport routes of simple transport landscapes.
-   **[Create Destinations to SAP Cloud Transport Management Service](create-destinations-to-sap-cloud-transport-management-service-795f733.md#loio795f7337e5d943df98c961303b02678b "If you use SAP Cloud Transport Management service to
		start the transport directly in your application, a destination to SAP Cloud Transport Management service is required in the source
		(development) environment of your application. This destination is used to export content
		from your source environment to SAP Cloud Transport Management.")**  
If you use SAP Cloud Transport Management service to start the transport directly in your application, a destination to SAP Cloud Transport Management service is required in the source \(development\) environment of your application. This destination is used to export content from your source environment to SAP Cloud Transport Management.

