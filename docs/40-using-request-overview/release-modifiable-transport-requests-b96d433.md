<!-- loiob96d433b67804a928c64f011c5e74f54 -->

# Release Modifiable Transport Requests

Release modifiable transport requests after successful testing to classify them as final.



<a name="loiob96d433b67804a928c64f011c5e74f54__prereq_ohb_q5g_jgc"/>

## Prerequisites

-   You are in the details of a modifiable transport request that you want to release. For more information, see [Displaying Details of Transport Requests](displaying-details-of-transport-requests-0415f2f.md).
-   You have at least the authorization of the *TransportOperator* role. For more information, see [Security](../60-security/security-51939a4.md).



## Procedure

1.  Choose *Release*.

2.  Confirm the dialog box.




<a name="loiob96d433b67804a928c64f011c5e74f54__result_sky_dvg_jgc"/>

## Results

You've released the transport request. Its lifecycle status changes to *Released*. You can no longer modify the transport request.

In the first-level nodes, the transport request is added to the import queues in an *Initial* import status and a *Final* mode.

If the transport request was previously tested in follow-on transport nodes, it gets a *Transient* import status in these import queues, and remains in the *Test* mode, for traceability reasons.

> ### Note:  
> Objects that were imported during the test remain in the tenant.

