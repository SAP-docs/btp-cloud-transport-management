<!-- loio0914d2c78d3a49fe9d7c95a021c4ff45 -->

<link rel="stylesheet" type="text/css" href="css/sap-icons.css"/>

# Migrating to SAP Alert Notification Service As a Trusted Internal Service

Learn how to transition from the deprecated destination-based notification configuration \(`ALERT_NOTIFICATION_SERVICE` destination\) to the new trusted internal service integration. It eliminates manual destination setup and requires node-level conditions in subscriptions to manage the notification scope.



## Context

> ### Note:  
> This topic is relevant for you if you previously set up notifications using the `ALERT_NOTIFICATION_SERVICE` destination. If you're a new user, follow the steps in [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md) instead.

The integration of SAP Alert Notification Service and SAP Cloud Transport Management was enhanced. SAP Cloud Transport Management now uses SAP Alert Notification Service as a trusted internal service, which eliminates the need to configure the `ALERT_NOTIFICATION_SERVICE` destination.

The destination-based configuration continues to work until its removal in Q4 2026. In addition, the new integration takes effect immediately for all transport nodes that weren't previously configured for notifications in the subaccount where the SAP Alert Notification service instance exists.

This has the following immediate effects:

-   If you have existing SAP Alert Notification service subscriptions for SAP Cloud Transport Management events and haven't set `tags.nodeName` or `tags.nodeId` conditions in SAP Alert Notification service: Notifications are sent for **all** transport nodes in that subaccount, not only for the nodes where you previously enabled the *Perform Notification* checkbox.

-   If you've used the configuration in SAP Alert Notification service also to receive notifications from subaccounts other than the one with the SAP Alert Notification service instance: These other subaccounts don't receive additional notifications.


We recommend that you add node-level conditions to your existing SAP Alert Notification service subscriptions to receive notifications only for nodes you previously configured for notifications. You can do this at any point before or after the removal of the destination-based integration.

Upon removal in Q4 2026, the following changes are in place:

-   SAP Cloud Transport Management no longer uses the `ALERT_NOTIFICATION_SERVICE` destination.

    If you have multiple subaccounts and used the previous configuration of SAP Cloud Transport Management events in SAP Alert Notification service for multiple subaccounts, this is no longer supported. You must create an instance of in SAP Alert Notification service in each subaccount where you want to receive events and configure the SAP Cloud Transport Management events separately in each SAP Alert Notification service instance.

-   The *Perform Notification* checkbox is removed from the transport node creation dialog.

    Use node-level conditions in SAP Alert Notification service to restrict notifications to specific transport nodes.

-   The *Enable Notification* checkbox is removed from the *File Quota* settings.

    It's sufficient to configure the *TmsStorageQuotaUsage* event in SAP Alert Notification service to receive notifications when the storage quota reaches the threshold.




## Procedure

1.  To restrict notifications to specific transport nodes, add node-level conditions to your existing subscriptions in SAP Alert Notification service:

    1.  In your SAP Alert Notification service instance, open an existing subscription and go to the *Select Conditions* step.
    2.  Create a new condition. From the *Condition* dropdown, select `tags.` and append `nodeName` or `nodeId`. The complete value is `tags.nodeName` or `tags.nodeId`.

    3.  Select an operand to match the required nodes. For example, select `Is Equal To` to target a single transport node, and set the expected value to <code><i class="varname">&lt;Name of a Transport Node&gt;</i></code> or <code><i class="varname">&lt;ID of a Transport Node&gt;</i></code>, for example `DEV`.

        If you want to receive notifications for multiple specific nodes, create one condition per node.

    4.  Assign the new condition or conditions to all existing subscriptions that you want to restrict.

    For more information, see [Managing Conditions](https://help.sap.com/docs/ALERT_NOTIFICATION/5967a369d4b74f7a9c2b91f5df8e6ab6/35ca5de101fc4d5791cdbb2df15e9d9b.html) in the SAP Alert Notification documentation.

2.  **Optional:** Only possible before removal of destination-based integration: Clear the *Perform Notification* checkbox on the relevant transport nodes.

    Once cleared, the trusted internal service integration is used for that node, and the destination is no longer required.

3.  **Optional:** Only possible before removal of destination-based integration: Clear the *Enable Notification* checkbox under :gear: → *File Quota*.

4.  **Optional:** Delete the `ALERT_NOTIFICATION_SERVICE` destination from SAP BTP Cockpit to clean up your subaccounts.

5.  If you have multiple subaccounts where you want to receive notifications, create new service instances of SAP Alert Notification service in these subaccounts and follow the steps described in [Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md).




## Results

When SAP Cloud Transport Management uses SAP Alert Notification service as a trusted internal service, notifications for SAP Cloud Transport Management events contain a *resource name: SAP Cloud Transport Management Service* entry in the *Resource Details:* section, and an additional *ans:eventScope: SUBACCOUNT* entry in the *Event Tags:* section.

When SAP Cloud Transport Management uses the destination-based integration, the notification contains a *resource name: SAP CP Transport Management Service* entry in the *Resource Details:* section.

**Related Information**  


[Receive Notifications for SAP Cloud Transport Management Actions Using SAP Alert Notification Service](receive-notifications-for-sap-cloud-transport-management-actions-using-sap-alert-notifica-95d4fc7.md "You can configure SAP Alert Notification Service to send notifications for actions started in SAP Cloud Transport Management service.")

