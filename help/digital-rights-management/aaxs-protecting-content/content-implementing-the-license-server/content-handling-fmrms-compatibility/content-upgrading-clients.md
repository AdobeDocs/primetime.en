---
seo-title: Upgrading clients
title: Upgrading clients
uuid: 9c9bc7da-2a97-4659-945a-554d778d30a3
---

# Upgrading clients{#upgrading-clients}

If an FMRMS 1.x client contacts a Adobe Access server, the server needs to prompt the client to upgrade.

* The request handler class is `com.adobe.flashaccess.sdk.protocol.compatibility.FMRMSv1RequestHandler`. 
* The request URL is "*Base URL from 1.x content*" + "/edcws/services/urn:EDCLicenseService"

  Unlike other Adobe Access request handlers, this handler does not provide access to any request information or require any response data to be set. Create an instance of the `FMRMSv1RequestHandler`, and then call `close()`

