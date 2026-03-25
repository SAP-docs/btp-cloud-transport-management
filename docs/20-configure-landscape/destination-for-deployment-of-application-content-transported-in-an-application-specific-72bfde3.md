<!-- loio72bfde3669004a74849f64a8136cdcdd -->

# Destination for Deployment of Application Content Transported in an Application-Specific Format Using mTLS Authentication

Configuration of destinations using mTLS authentication enables secure deployment of application-specific content by using `X.509` client certificates instead of client secrets. This approach enhances security and can be used when deploying application content.



## Prerequisites

The deploying application or service supports the mTLS credentials type.



## Context

You can use Mutual Transport Layer Security \(mTLS\) for authentication for a destination that points to application-specific content deployment. This type uses an mTLS certificate instead of a client secret. For more information, see [OAuth with X.509 Client Certificates](https://help.sap.com/docs/CP_CONNECTIVITY/14ad6e76ba9b44f682154bb90686ae84/2c162aaa9e464480b2307879d1b865f5.html). Create a certificate configuration that contains a valid `X.509` client certificate. For SAP Cloud Transport Management, use the `pkcs#1` format for the client certificate. You need a `.pem` \(privacy enhanced mail\) file that contains both the certificate and the private key.

The general process is as follows:

1.  Create a service key for the deploying application or service using the `X.509` credential type.
2.  Extract the `certificate` and `key` information from the service key into one single certificate file of type `.pem`.
3.  Upload the `.pem` file certificate to Destination service.
4.  Create a destination using mTLS by using the certificate as the *Token Service Key Store Location*.



## Procedure

1.  Create a Service Key

    On the target tenant, start creating a service key for the deploying application or service as described in [Service Keys](https://help.sap.com/docs/SERVICEMANAGEMENT/09cc82baadc542a688176dce601398de/6fcac08409db4b0f9ad55a6acd4d31c5.html).

    To obtain an `X.509` credential type, add the following parameters in JSON format:

    > ### Sample Code:  
    > ```
    > {
    >   "xsuaa": 
    > 	{
    >   		"credential-type": "x509",
    >   		"x509": {
    >     		"key-length": 2048,
    >     		"validity": 7,
    >     		"validity-type": "DAYS"
    >   		}
    > 	}
    > }
    > ```

    For more information about the parameters, see [Parameters for X.509 Certificates Managed by SAP Authorization and Trust Management Service](https://help.sap.com/docs/CP_AUTHORIZ_TRUST_MNG/ae8e8427ecdf407790d96dad93b5f723/436ed684eadc4045881e59bd1048d98d.html).

    ![Parameters to add in Service Key](images/JSON_parameters_for_service_key_for_mTLS_03adb53.png)

    See also: [Enable mTLS Authentication to SAP Authorization and Trust Management Service for Your Application](https://help.sap.com/docs/CP_AUTHORIZ_TRUST_MNG/ae8e8427ecdf407790d96dad93b5f723/aa803382970c41d2970c7bf265475dfb.html).

    Since you've created a service key using the `X.509` credential type, the JSON structure contains ***certificate*** and ***key*** attributes in the ***uaa*** section that you can use to create the certificate `.pem` file.

2.  Extract the `certificate` and `key` information from the service key into one single certificate file of type `.pem`.

    > ### Note:  
    > Both the certificate and the private key are Base64 encoded with the appropriate prefix and postfix.

    Follow these steps to format and create certificate and private key files, and then combine them into one `.pem` file:

    1.  In service key, find the client certificate under the ***certificate*** attribute and the private key under the ***key*** attribute. Ensure that the ***credential-type*** is ***x509***. In some service keys, the ***certificate*** and ***key*** attributes appear directly in the root JSON object.

    2.  Copy the ***certificate*** attribute from the service key into a text editor. Replace all `\n` characters with actual line breaks. You can also try some online tools to unescape the characters. Save the file with a `.pem` extension. For example: `certificate.pem`

        For UNIX, you can use this command:

        > ### Sample Code:  
        > ```
        > echo "-----BEGIN CERTIFICATE-----\nMIIabcde (...) fghIJKLMNO\n----END CERTIFICATE-----\n" > cert.pem
        > ```

    3.  Copy the ***key*** attribute into a text editor. Replace all `\n` characters by actual line breaks. Save the file with a `.pem` extension. For example: `key.pem`.

        For UNIX, you can use this command:

        > ### Sample Code:  
        > ```
        > echo "-----BEGIN RSA PRIVATE KEY-----\nMIIpqrstuvw (...) xyz\n (...) abc==\n-----END RSA PRIVATE KEY-----\n" >> cert.pem
        > ```

    4.  Create a new file. Paste the contents of `key.pem` first, then paste the contents of `certificate.pem`. Save the file. For example: `finalcertificate.pem`.

        The content of the file looks like this. Multiple `CERTIFICATE` sections are possible:

        > ### Sample Code:  
        > ```
        > -----BEGIN RSA PRIVATE KEY-----
        > MIIEp 
        > (...)
        > Opdd/v4TWiDpkSesxtdui4dLJPMllIXSumpEgC5oyQ==
        > -----END RSA PRIVATE KEY-----
        > -----BEGIN CERTIFICATE-----
        > MIIF
        > (...)
        > s6fZmG7TuZxQg==
        > -----END CERTIFICATE-----
        > -----BEGIN CERTIFICATE-----
        > MIIGZjC
        > (...)
        > DvAhf6Q==
        > -----END CERTIFICATE-----
        > 
        > ```


3.  Upload the certificate for the destination.

    In the target tenant, upload the `.pem` file as described in *Upload Certificates* in [Manage Destination Certificates](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/df1bb55a526942b9bee78fea2ebb3162.html).

    The certificate is available for selection as `tokenService.KeyStoreLocation` in the destination configuration.

4.  Create a destination to address the target end point of application-specific content deployment.

    To create the destination, follow the steps described in [Creating Destinations for Deployment of Application Content Transported in an Application-Specific Format](creating-destinations-for-deployment-of-application-content-transported-in-an-application-23bb29c.md) and use the following values:

    **Values of Destination for Deployment of Application Content Transported in an Application-Specific Format Using mTLS Authentication**


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Name of the destination
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Type*
    
    </td>
    <td valign="top">
    
    *HTTP*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    *Internet*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    `url` value from the service key of the deploying application or service
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    Select *OAuth2ClientCredentials*.

    [OAuth Client Credentials Authentication](https://help.sap.com/docs/CP_CONNECTIVITY/14ad6e76ba9b44f682154bb90686ae84/4e1d742a3d45472d83b411e141729795.html)
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Client ID*
    
    </td>
    <td valign="top">
    
    `clientid` value from the service key of the deploying application or service
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Use mTLS for token retrieval*
    
    </td>
    <td valign="top">
    
    Select the checkbox.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Token Service Key Store Location*
    
    </td>
    <td valign="top">
    
    Select the certificate that you've uploaded in the previous step.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Token Service Key Store Password*
    
    </td>
    <td valign="top">
    
    This is the password that protects the certificate. For this use case, you can leave it empty.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Token Service URL*
    
    </td>
    <td valign="top">
    
    `certurl` value from the service key of the deploying application or service

    If the URL in the service key is a base URL, append `/oauth/token`.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Token Service URL Type*
    
    </td>
    <td valign="top">
    
    *Dedicated*
    
    </td>
    </tr>
    </table>
    



## Example

> ### Example:  
> You can use mTLS for deployments using SAP Content Agent service. The following topics in the SAP Content Agent service documentation contain related information:
> 
> -   [Create Service Key](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/c0ec2ba3016644a19cd6322fbc72ea2a.html)
> -   [Create Target Node Destination](https://help.sap.com/docs/CONTENT_AGENT_SERVICE/ae1a4f2d150d468d9ff56e13f9898e07/06bd9e2d55084eaf9235844118ddb84c.html)

