---
seo-title: Handle synchronization requests
title: Handle synchronization requests
uuid: e2623afb-7a57-402d-a8a1-07bcf6324d41
---

# Handle synchronization requests {#handle-synchronization-requests}

If a license specifies synchronization requirements  [Requirements for Synchronization,](../../protecting-content/introduction/usage-rules/authentication/synchronization.md) the client periodically sends synchronization requests to the server, based on the frequency specified in the license. To enable synchronization messages, set `SyncFrequencyRequirements` in a PlayRight.

* The request handler class is `com.adobe.flashaccess.sdk.protocol.sync.SynchronizationHandler` 
* The request message class is `com.adobe.flashaccess.sdk.protocol.sync.SynchronizationRequestMessage` 
* If both the client and server support protocol version 5, the request URL is "License Server URL in metadata: + " [!DNL /flashaccess/sync/v4]". Otherwise, the request URL is “License Server URL in metadata” + " [!DNL /flashaccess/sync/v3]"

Synchronization messages are used to synchronize the client's time with the server's time. If licenses are embedded in the content and do not need to be retrieved from a license server, synchronizing the client's time is important to prevent the client from modifying its clock in order to bypass the license expiration.

Synchronization messages can also be used to communicate the client state information to the server ( `getClientState()`) for rollback detection.

See [Rollback Protection](../../protecting-content/implementing-the-license-server/processing-drm-requests.md#rollback-detection).
