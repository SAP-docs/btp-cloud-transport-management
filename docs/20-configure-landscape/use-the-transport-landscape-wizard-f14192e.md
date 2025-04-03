<!-- loiof14192ede8ac4603955b572537d6bec2 -->

# Use the Transport Landscape Wizard

You can use the Transport Landscape Wizard to configure the transport nodes and transport routes of simple transport landscapes.



<a name="loiof14192ede8ac4603955b572537d6bec2__prereq_gs3_c2k_pdb"/>

## Prerequisites

-   You have one of the roles *Administrator* or *LandscapeOperator* assigned to your user. For more information, see [Security](../60-security/security-51939a4.md).

-   You have configured transport destinations. For more information, see [Create Transport Destinations](create-transport-destinations-c9905c1.md).

-   You are on the *Transport Landscape Wizard* screen in the SAP Cloud Transport Management UI.



## Procedure

1.  Under *Selection of Template*, select the number of transport nodes of which your landscape will consist.

    A transport node represents the source or the target end point of a deployment process - for example, a source \(DEV\) and a target \(PROD\) space in a Cloud Foundry subaccount. If you have DEV and PRD account, you need a two-node landscape. If you have an additional TEST account, you need a three-node landscape. For an example, see [Sample Configuration Scenario](sample-configuration-scenario-22e1ed6.md).

2.  Choose *Next*.

3.  For each transport node, enter the data as described under [Create Transport Nodes](create-transport-nodes-f71a4d5.md).

4.  **Optional:** Change the generated names of the transport routes so that you can later identify your transport routes, and enter descriptions.

    For more information, see [Create Transport Routes](create-transport-routes-dddb749.md).

5.  Choose *Next*.

    The next screen shows the steps involved in the generation of the transport landscape.

6.  Choose *Summary*.

    On the *Summary* screen, you see a summary of the transport nodes and transport routes that you created. You can directly go to the nodes or transport routes that you created through the links provided in the *Summary*.

7.  To close the wizard, choose *Finish*.




<a name="loiof14192ede8ac4603955b572537d6bec2__result_szb_pny_32b"/>

## Results

You have configured transport nodes and transport routes for your transport landscape. If required, you can edit the individual entities.

