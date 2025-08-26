<!-- loiob541b0951b614ef89c111d73a301818f -->

# Processing Modifiable Transport Requests

Modifiable transport requests provide an efficient and flexible way for managing multiple files in one transport request.

Modifiable transport requests allow repeated changes throughout their lifecycle. You can add or remove files to refine the content, instead of creating new requests for each iteration. You can test file deployment as often as needed. After successful testing, you can release modifiable requests.

Processing a modifiable transport request involves the following steps:

1.  **Creation**

    Create a modifiable transport request and add files as required.

    For more information, see [Create Modifiable Transport Requests](create-modifiable-transport-requests-b74238c.md).

2.  **Testing**

    After completing development and consolidating the relevant files for the modifiable transport request, run tests in the relevant transport nodes. This lets you test the import and verify that your content works as expected. You can repeat the tests as often as necessary until you achieve a successful result.

    For more information, see [Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md).

3.  **Release**:

    After successful testing of the modifiable transport request, you can release it. The request is no longer modifiable.

    > ### Note:  
    > You can release modifiable transport requests without testing them. However, we don't recommend this.

    The transport request is added to the import queues of the first-level nodes in an *Initial* status. All previous imports are invalidated.

    > ### Note:  
    > The objects that were imported during the test remain in the tenant.

    For more information, see [Release Modifiable Transport Requests](release-modifiable-transport-requests-b96d433.md).


-   **[Create Modifiable Transport Requests](create-modifiable-transport-requests-b74238c.md "Create modifiable transport requests to efficiently manage multiple files in one
		request.")**  
Create modifiable transport requests to efficiently manage multiple files in one request.
-   **[Test Modifiable Transport Requests](test-modifiable-transport-requests-36de37c.md "Test modifiable transport requests to ensure successful deployment.")**  
Test modifiable transport requests to ensure successful deployment.
-   **[Release Modifiable Transport Requests](release-modifiable-transport-requests-b96d433.md "Release modifiable transport requests after successful testing to classify them as
		final.")**  
Release modifiable transport requests after successful testing to classify them as final.

