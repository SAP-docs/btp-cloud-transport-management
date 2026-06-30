<!-- loio95d4fc79244f4c93b526a943eef1e274 -->

# Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service

You can configure SAP Alert Notification Service to send notifications for actions started in SAP Cloud Transport Management service.



<a name="loio95d4fc79244f4c93b526a943eef1e274__prereq_k2r_wf4_jkb"/>

## Prerequisites

-   You have an active subscription for SAP Cloud Transport Management.
-   Your global account and subaccounts are entitled for SAP Alert Notification service.



<a name="loio95d4fc79244f4c93b526a943eef1e274__context_orn_xf4_jkb"/>

## Context

> ### Note:  
> If you previously configured the `ALERT_NOTIFICATION_SERVICE` destination to receive notifications, you can continue to use this setup. To switch to the method described here, see [Migrating to SAP Alert Notification Service As a Trusted Internal Service](migrating-to-sap-alert-notification-service-as-a-trusted-internal-service-0914d2c.md). For the outdated configuration steps, see [Obsolete: Receive SAP Cloud Transport Management Actions Using SAP Alert Notification Service](obsolete-receive-sap-cloud-transport-management-actions-using-sap-alert-notification-serv-a638704.md).

SAP Cloud Transport Management uses SAP Alert Notification service as a trusted internal service. This means that no destination configuration is required. As soon as a service instance of SAP Alert Notification service is available in a Cloud Foundry subaccount, you can create subscriptions for SAP Cloud Transport Management events in SAP Alert Notification service. SAP Alert Notification service supports different notification channels, such as e-mail or Slack. When setting up subscriptions you can use conditions to restrict notifications for specific transport nodes.

For more information about SAP Alert Notification service, see [SAP Alert Notification Service for SAP BTP](https://help.sap.com/docs/ALERT_NOTIFICATION).



<a name="loio95d4fc79244f4c93b526a943eef1e274__steps_w5f_zf4_jkb"/>

## Procedure

1.  In the Cloud Foundry space of a subaccount where you want to receive notifications for SAP Cloud Transport Management service events, in SAP BTP Cockpit, navigate to the *Service Instances* page, and create a service instance for SAP Alert Notification service as described under [Initial Setup](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/812b6e3ed8934648ad15780cd51721ef.html) in the SAP Alert Notification service documentation.

2.  In SAP Alert Notification service, set up the way in which you want to receive notifications. To do this, create a subscription.

    You can create subscriptions for the following events of SAP Cloud Transport Management:

    -   *TmsImportFinished*: Receive a notification when an import is finished.

        See: [SAP Cloud Transport Management Import Finished](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/e83c3b59ed844964a255f1bcc4e0691d.html)

    -   *TmsImportStarted*: Receive a notification when an import is started.

        See: [SAP Cloud Transport Management Import Started](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/7d7b2ca205494543b03974b95f721fdb.html)

    -   *TmsTransportRequestAdded*: Receive a notification when a transport request is added to an import queue.

        See: [SAP Cloud Transport Request Added](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/17e6d560467b483589229b2c46ec458f.html)

    -   *TmsNodeImportJobDeactivated*: Receive a notification when an import scheduler is disabled because too many imports have failed.

        See: [SAP Cloud Transport Node Import Job Deactivated](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/a9c39656e291471e9ca11c0d63e16f06.html)

    -   *TmsStorageQuotaUsage*: Receive a notification when the storage quota in your SAP Cloud Transport Management subscription has increased over the warning threshold of 85% of the total storage capacity.

        See: [SAP Cloud Transport Storage Quota Usage](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/8344c9d0516c4b0fbbe6d71937884667.html)


    For import-related events \(*TmsImportStarted*, *TmsImportFinished*, *TmsTransportRequestAdded*, *TmsNodeImportJobDeactivated*\), you can use the `tags` *Event Property* as condition to filter notifications. The following options are useful to restrict the notifications to specific nodes.


    <table>
    <tr>
    <th valign="top">

    Tag
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    `tags.nodeName`
    
    </td>
    <td valign="top">
    
    The name of the transport node on which the action was started.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    `tags.nodeId`
    
    </td>
    <td valign="top">
    
    The ID of the transport node.
    
    </td>
    </tr>
    </table>
    
    For multiple transport nodes, you can either create multiple conditions or use an operand to match a selected name range.

    For more information about creating subscriptions in SAP Alert Notification, see [Managing Subscriptions](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/07fd21e170c7452482c3532c5521bb90.html) in the SAP Alert Notification service documentation.

3.  Repeat the previous steps in all subaccounts where you want to receive notifications for SAP Cloud Transport Management events.




<a name="loio95d4fc79244f4c93b526a943eef1e274__result_jcf_4sd_ndc"/>

## Results

When an action takes place in SAP Cloud Transport Management that matches the subscription configured in SAP Alert Notification service, the related notification is sent to the configured channel.

Each notification contains a *resource name: SAP Cloud Transport Management Service* entry in the *Resource Details* section, and an *ans:eventScope: SUBACCOUNT* entry in the *Event Tags* section.

-   *TmsImportFinished*: When the *Forward Mode* of a transport node is set to *Manual*, the notification contains links that allow you to display the transport request, or to forward it or all transport requests in the import queue to the target nodes.

-   *TmsTransportRequestAdded*: The notification contains links that allow you to display the transport request or to start an import in the transport node. When you select a link, the import queue of the transport node opens with a confirmation prompt for the corresponding actions.


> ### Example:  
> 1.  In SAP Alert Notification Service, create a subscription with the name `TmsImport`. \(You can use any name.\)
> 
> 2.  In the *Select Conditions* step, create the following conditions:
>     -   Create a condition with the name `TmsImportStarted`. \(You can use any name.\) For the *Condition* fields, select `eventType` and the operand `Is Equal To`. Set the expected value to `TmsImportStarted`.
> 
>         See: [SAP Cloud Transport Management Import Started](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/7d7b2ca205494543b03974b95f721fdb.html)
> 
>     -   Add a condition with the name `TmsImportFinished`. \(You can use any name.\) For the *Condition* fields, select `eventType` and the operand `Is Equal To`. Set the expected value to `TmsImportFinished`.
> 
>         See: [SAP Cloud Transport Management Import Finished](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/e83c3b59ed844964a255f1bcc4e0691d.html)
> 
>     -   Add a condition with the name `nodeName`. \(You can use any name.\) For the *Condition* fields, select `tags.` and append `nodeName`, that is `tags.nodeName`. As the operand, select `Is Equal To`. Set the expected value to the exact name of the transport name, here `DEV`.
> 
>         See: `tags` *Event Property* in [SAP Cloud Transport Management Import Started](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/7d7b2ca205494543b03974b95f721fdb.html) or [SAP Cloud Transport Management Import Finished](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/e83c3b59ed844964a255f1bcc4e0691d.html)
> 
> 
> 3.  In the *Select Actions* step, create an action with the name `MyEmail`. \(You can use any name.\) Select the *Email* option and enter your e-mail address.
> 
> With this subscription, you get e-mail notifications for every import that starts and finishes in the transport node with the name specified in the `nodeName` condition, here `DEV`.

-   **[Migrating to SAP Alert Notification Service As a Trusted Internal Service](migrating-to-sap-alert-notification-service-as-a-trusted-internal-service-0914d2c.md "Learn how to transition from the deprecated destination-based notification configuration
			(ALERT_NOTIFICATION_SERVICE destination) to the
		new trusted internal service integration. It eliminates manual destination setup and
		requires node-level conditions in subscriptions to manage the notification
		scope.")**  
Learn how to transition from the deprecated destination-based notification configuration \(`ALERT_NOTIFICATION_SERVICE` destination\) to the new trusted internal service integration. It eliminates manual destination setup and requires node-level conditions in subscriptions to manage the notification scope.
-   **[Obsolete: Receive SAP Cloud Transport Management Actions Using SAP Alert Notification Service](obsolete-receive-sap-cloud-transport-management-actions-using-sap-alert-notification-serv-a638704.md "The procedure to configure SAP Alert Notification Service to send notifications for actions
		started in SAP Cloud Transport Management
		service was enhanced. It no longer needs the destination to be configured.")**  
The procedure to configure SAP Alert Notification Service to send notifications for actions started in SAP Cloud Transport Management service was enhanced. It no longer needs the destination to be configured.

**Related Information**  


[Managing Conditions](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/35ca5de101fc4d5791cdbb2df15e9d9b.html)

[SAP Cloud Transport Management Events](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/21c8326478c94d48a2028b0d1d6dd6fd.html)

