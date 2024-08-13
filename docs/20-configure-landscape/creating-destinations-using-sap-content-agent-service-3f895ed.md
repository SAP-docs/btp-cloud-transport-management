<!-- loio3f895ed05f2647c5b43e98f0477bedef -->

# Creating Destinations Using SAP Content Agent Service

To address the target end point of the deployment process of MTA Deployment on Cloud Foundry, you can create a destination to SAP Content Agent service.



<a name="loio3f895ed05f2647c5b43e98f0477bedef__steps_c1r_45v_hwb"/>

## Procedure

1.  Create a service instance and a service key in every subaccount in which you want to use SAP Content Agent service for deployment.

    For more information, see [Create Instance](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/1f45ddc3d6194886802924068724b59f.html) and [Create Service Key](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/c0ec2ba3016644a19cd6322fbc72ea2a.html?locale=en-US) in the SAP Content Agent service documentation.

2.  In the subaccount in which you're subscribed to SAP Cloud Transport Management, create a transport destination pointing to SAP Content Agent service.

    For more information, see [Create Target Node Destination](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/06bd9e2d55084eaf9235844118ddb84c.html?locale=en-US) in the SAP Content Agent service documentation.

    > ### Note:  
    > Depending on the content that you want to import, additional transport destinations are required pointing to the service providing the content.
    > 
    > For more information, see [Configure Subaccount](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/606fb4e1c62648dc82ef24b32e7b50cb.html?locale=en-US) in the SAP Content Agent service documentation.




<a name="loio3f895ed05f2647c5b43e98f0477bedef__postreq_atw_3ts_gwb"/>

## Next Steps

[Create Transport Nodes](create-transport-nodes-f71a4d5.md)

