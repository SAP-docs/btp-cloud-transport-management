<!-- loio881d7520f6ff44e18a4ef4411cbdeed2 -->

# Creating Destinations for MTA Deployment on Cloud Foundry

For MTA deployment on Cloud Foundry, you have different options to configure transport destinations to address the target endpoint of the deployment process.



<a name="loio881d7520f6ff44e18a4ef4411cbdeed2__context_wly_zns_gwb"/>

## Context

The following services can be used for deployment:

-   SAP Cloud Deployment service

    Default option for MTA deployment on Cloud Foundry.

    If you want to use a custom identity provider for the platform user used for the deployment, use *OAuth2Password* authentication for the destination.

-   SAP Content Agent service

    To transport content of API Management and SAP Cloud Integration together, use this option.


For more information about the option that is relevant for your use case, also see the application-specific documentation. You can find a list of known integrations and links to application-specific information under [Integrating SAP Cloud Transport Management with Other SAP Cloud Solutions](../10-initial-setup/integrating-sap-cloud-transport-management-with-other-sap-cloud-solutions-ddaa000.md).

For more information about issues that can occur when deploying MTAs in Cloud Foundry, see [Troubleshooting Issues when Transporting Multitarget Applications \(MTAs\)](../troubleshooting-issues-when-transporting-multitarget-applications-mtas-3f7a9bc.md).

-   **[Creating Destinations Using SAP Cloud Deployment Service with OAuth2Password Authentication](creating-destinations-using-sap-cloud-deployment-service-with-oauth2password-authenticati-a26a721.md "To address the target end point of the deployment process of MTA Deployment on Cloud
                                Foundry, you can create a destination to  SAP Cloud Deployment
                                    service with OAuth2Password authentication.")**  
To address the target end point of the deployment process of MTA Deployment on Cloud Foundry, you can create a destination to SAP Cloud Deployment service with *OAuth2Password* authentication.
-   **[Creating Destinations Using SAP Cloud Deployment Service with Basic Authentication](creating-destinations-using-sap-cloud-deployment-service-with-basic-authentication-6b7c9d8.md "To address the target end point of the deployment process of MTA Deployment on Cloud
                                Foundry, you can create a destination to  SAP Cloud Deployment
                                    service with classic Basic authentication.")**  
To address the target end point of the deployment process of MTA Deployment on Cloud Foundry, you can create a destination to SAP Cloud Deployment service with classic *Basic* authentication.
-   **[Creating Destinations Using SAP Content Agent Service](creating-destinations-using-sap-content-agent-service-3f895ed.md "To address the target end point of the deployment process of MTA Deployment on Cloud
                                Foundry, you can create a destination to  SAP Content Agent
                                service.")**  
To address the target end point of the deployment process of MTA Deployment on Cloud Foundry, you can create a destination to SAP Content Agent service.

