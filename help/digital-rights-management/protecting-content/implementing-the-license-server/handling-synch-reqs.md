---
seo-title: Handle synchronization requests
title: Handle synchronization requests
uuid: 1f589e1e-2a66-464c-86ca-3c3633efd678
index: y
internal: n
snippet: y
---

# Handle synchronization requests{#handle-synchronization-requests}

If a license specifies synchronization requirements ( [Requirements for Synchronization,](c_-synchronization.md)) the client periodically sends synchronization requests to the server, based on the frequency specified in the license. To enable synchronization messages, set `SyncFrequencyRequirements` in a PlayRight.

* The request handler class is `com.adobe.flashaccess.sdk.protocol.sync.SynchronizationHandler` 
* The request message class is `com.adobe.flashaccess.sdk.protocol.sync.SynchronizationRequestMessage` 
* If both the client and server support protocol version 5, the request URL is "License Server URL in metadata: + " [!DNL /flashaccess/sync/v4]". Otherwise, the request URL is “License Server URL in metadata” + " [!DNL /flashaccess/sync/v3]"

Synchronization messages are used to synchronize the client’s time with the server’s time. If licenses are embedded in the content and do not need to be retrieved from a license server, synchronizing the client’s time is important to prevent the client from modifying its clock in order to bypass the license expiration.

Synchronization messages can also be used to communicate the client state information to the server ( `getClientState()`) for rollback detection.

See [Rollback Protection](c_content-rollback-detection.md). 
