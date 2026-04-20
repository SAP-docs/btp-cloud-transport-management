<!-- loioa6387045a4824f578db003977462317b -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Obsolete: Receive SAP Cloud Transport Management Actions Using SAP Alert Notification Service

The procedure to configure SAP Alert Notification Service to send notifications for actions started in SAP Cloud Transport Management service was enhanced. It no longer needs the destination to be configured.



<a name="loioa6387045a4824f578db003977462317b__prereq_k2r_wf4_jkb"/>

## Prerequisites

-   You have an active subscription for SAP Cloud Transport Management.
-   Your global account and subaccount are entitled for SAP Alert Notification service.



<a name="loioa6387045a4824f578db003977462317b__context_orn_xf4_jkb"/>

## Context

> ### Note:  
> This topic describes the deprecated method of configuring SAP Alert Notification Service to send notifications for actions started in SAP Cloud Transport Management service using a destination with a fixed name. The destination-based configuration will be removed in Q4 2026.
> 
> You can continue to use it for existing configurations. However, if you are a new user, follow the updated integration method described in [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md). If you want to migrate from the destination-based configuration to the new method before its removal, see [Migrating to SAP Alert Notification Service As a Trusted Internal Service](migrating-to-sap-alert-notification-service-as-a-trusted-internal-service-0914d2c.md).

If there's a service instance of SAP Alert Notification service available in the Cloud Foundry subaccount in which you’re using SAP Cloud Transport Management, configure the `ALERT_NOTIFICATION_SERVICE` destination, which refers to the service instance. This enables SAP Alert Notification service to send notifications for actions started in SAP Cloud Transport Management. In addition, you can create the subscription for receiving notifications in any channel that SAP Alert Notification service supports, by e-mail, or Slack channel, for example.

> ### Note:  
> It's sufficient to configure SAP Alert Notification service in one subaccount. However, you must configure the `ALERT_NOTIFICATION_SERVICE` destination in each subaccount subscribed to SAP Cloud Transport Management from which you want to receive notifications.
> 
> For more information about SAP Alert Notification service, see [SAP Alert Notification Service for SAP BTP](https://help.sap.com/docs/ALERT_NOTIFICATION).



<a name="loioa6387045a4824f578db003977462317b__steps_w5f_zf4_jkb"/>

## Procedure

1.  In the Cloud Foundry space of the subaccount in which you’re using SAP Cloud Transport Management service, in SAP BTP Cockpit, navigate to the *Service Instances* page, and create a service instance for SAP Alert Notification service as described under [Initial Setup](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/812b6e3ed8934648ad15780cd51721ef.html) in the SAP Alert Notification service documentation.

    Under step *8. Obtain the credentials for the Alert Notification service*, choose option *b. Create a Service Key from the Service Key tab* to make the service instance URL and credentials available to you for accessing the service using the SAP Cloud Transport Management service.

2.  In SAP BTP Cockpit of the subaccount in which you’re using SAP Cloud Transport Management, use the SAP Destination service to create a destination with the fixed name `ALERT_NOTIFICATION_SERVICE`.

    1.  Choose *Connectivity* \> *Destinations* \> *New Destination*.

    2.  Enter the following details:


        <table>
        <tr>
        <th valign="top">

        Field
        
        </th>
        <th valign="top">

        Input
        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        *Name*
        
        </td>
        <td valign="top">
        
        Enter `ALERT_NOTIFICATION_SERVICE`.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Type*
        
        </td>
        <td valign="top">
        
        Choose *HTTP*.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Description* \(optional\)
        
        </td>
        <td valign="top">
        
        You can enter a description for the destination.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *URL*
        
        </td>
        <td valign="top">
        
        Enter the value of the *url* attribute from the Service Key of the service instance created in step 1.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Proxy Type*
        
        </td>
        <td valign="top">
        
        Choose *Internet*.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Authentication*
        
        </td>
        <td valign="top">
        
        Choose *OAuth2ClientCredentials*.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Client ID*
        
        </td>
        <td valign="top">
        
        Enter the value of the *client\_id* attribute from the Service Key of the service instance created in step 1.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Client Secret*
        
        </td>
        <td valign="top">
        
        Enter the value of the *client\_secret* attribute from the Service Key of the service instance created in step 1.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Token Service URL*
        
        </td>
        <td valign="top">
        
        Enter the value of the *oauth\_url* attribute from the Service Key of the service instance created in step 1.
        
        </td>
        </tr>
        </table>
        

3.  To enable notifications for actions started in SAP Cloud Transport Management, select the *Perform Notification* checkbox when creating a transport node.

    > ### Note:  
    > The checkbox is displayed only, if the destination to SAP Alert Notification service is configured.

    See also: [Create Transport Nodes](20-configure-landscape/create-transport-nodes-f71a4d5.md)

    > ### Note:  
    > This step isn't necessary when you only want to receive warning notifications about the storage quota in your subscription \(*TmsStorageQuotaUsage*\) event.

4.  To enable storage quota notifications, in SAP Cloud Transport Management, select the *Enable Notification* checkbox under :gear: → <span class="SAP-icons-V5"></span> File Quota.

5.  In SAP Alert Notification service, set up the way in which you want to receive notifications. For more information, see [Managing Subscriptions](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/07fd21e170c7452482c3532c5521bb90.html) in the SAP Alert Notification service documentation.

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





<a name="loioa6387045a4824f578db003977462317b__result_jcf_4sd_ndc"/>

## Results

When an action takes place in SAP Cloud Transport Management for which you've enabled a notification, the notification is sent to the configured channel that contains the details of the action.

Notifications sent using the destination-based configuration contain a *resource name: SAP CP Transport Management Service* entry in the *Resource Details* section.

> ### Note:  
> After migrating to the new method, the *resource name* entry changes to *SAP Cloud Transport Management Service*, and an additional *ans:eventScope: SUBACCOUNT* entry appears in the *Event Tags* section. You can use this to confirm which implementation is active.

*TmsImportFinished*: When the *Forward Mode* of a transport node is set to *Manual*, the notification contains links that allow you to display the transport request, or to forward it or all transport requests in the import queue to the target nodes.

*TmsTransportRequestAdded*: The notification contains links that allow you to display the transport request or to start an import in the transport node. When you select a link, the import queue of the transport node opens with a confirmation prompt for the corresponding actions.

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

**Related Information**  


[Managing Conditions](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/35ca5de101fc4d5791cdbb2df15e9d9b.html)

[SAP Cloud Transport Management Events](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/21c8326478c94d48a2028b0d1d6dd6fd.html)

