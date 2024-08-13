<!-- loio66fd7283c62f48adb23c56fb48c84a60 -->

# Initial Setup

Follow the initial setup steps to be able to use SAP Cloud Transport Management service.

You can get started with SAP Cloud Transport Management using the standard procedures for SAP BTP Cloud Foundry environment.

> ### Note:  
> If you are using this service as part of SAP Build Code, follow the [SAP Build Code Initial Setup](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/07698d7c31284e4db370acdf017cfd14.html?version=SHIP) instructions instead.



<a name="loio66fd7283c62f48adb23c56fb48c84a60__section_ilb_db4_ktb"/>

## Prerequisites

-   You're a global account administrator.
-   You've set up your global account and at least one subaccount on SAP BTP. For an overview of the required steps, see [Getting Started in the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/b328cc89ea14484d9655b8cfb8efb508.html)

    > ### Recommendation:  
    > Run SAP Cloud Transport Management service as shared service, by setting it up on a central administrative subaccount, to facilitate role management and allow strict access control.




<a name="loio66fd7283c62f48adb23c56fb48c84a60__section_amj_mp5_ktb"/>

## Context

SAP Cloud Transport Management is offered using the *Consumption-Based Commercial Model*.

Before executing the initial setup, you must determine whether you'll use the service to transport content archives that are available on local file systems, or to transport content archives directly in another application, for example, SAP Cloud Integration, or integrated in SAP Cloud ALM. Depending on the scenario, different configuration steps are involved. For more information about known integrations in SAP Cloud Transport Management, see [Integrating the Service](../70-integrations/integrating-the-service-7e966f7.md#loio7e966f73645c42eca1bf19e719b21ceb).

The following topics contain an overview of the steps involved for each scenario:

-   **[Set Up the Environment to Transport Content Archives directly in an Application](set-up-the-environment-to-transport-content-archives-directly-in-an-application-8d94907.md "Before you can transport content archives directly in an application, cloud administrators perform the following initial setup
		steps.")**  
Before you can transport content archives directly in an application, cloud administrators perform the following initial setup steps.
-   **[Set Up the Environment to Transport Content Archives that are available on a Local File System](set-up-the-environment-to-transport-content-archives-that-are-available-on-a-local-file-s-25a3bb9.md "Before you can transport content archives that are available on a local file system, cloud administrators perform the following setup
		steps.")**  
Before you can transport content archives that are available on a local file system, cloud administrators perform the following setup steps.

**Related Information**  


[SAP Cloud Transport Management Scenarios](../20-configure-landscape/sap-cloud-transport-management-scenarios-0cb16e5.md "You can use SAP Cloud Transport Management to transport content archives directly from within an application's source environment to a target environment. If there's no export integration of SAP Cloud Transport Management in the source environment, you can use the service to upload content archives from a local file system and import them in a target environment.")

[Integrating the Service](../70-integrations/integrating-the-service-7e966f7.md#loio7e966f73645c42eca1bf19e719b21ceb "SAP Cloud Transport Management service is integrated in development and change management processes and with other services. You can also integrate the service in your processes using the APIs that are available on SAP Business Accelerator Hub.")

['Commercial Models' in the 'Best Practices for SAP BTP' guide](https://help.sap.com/docs/BTP/df50977d8bfa4c9a8a063ddb37113c43/38ecf59cdda64150a102cfaa62d5faab.html#loio263d40009a5a4237a62e8f5c05ee641e)

