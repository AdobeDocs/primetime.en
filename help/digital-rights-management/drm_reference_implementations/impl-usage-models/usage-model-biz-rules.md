---
description: null
seo-description: null
seo-title: Usage model demo business rules
title: Usage model demo business rules
uuid: 782962ee-5d93-4138-b959-e33e4568e80a
index: y
internal: n
snippet: y
---

# Usage model demo business rules{#usage-model-demo-business-rules}

When a user requests a license, the Reference Implementation server checks the metadata that the client has sent, to determine whether the content was packaged by using the `RI_UsageModelDemo` property. If that is the case, the server applies the following business rules.

* If one of the DRM policies requires authentication:

    * If the request contains a valid authentication token, search for the name of the user in the Customer database table.

      If you cannot locate the name of the user, complete the following tasks:

        * If the `Customer.IsSubscriber` property is set to `true`, you need to generate a license for the *`Subscription`* usage model and send it to the user. 
        
        * Search for a record in the `CustomerAuthorization` database table for the name of the user and the content ID.

      If you can locate the user's record, complete the following tasks:

        * If the `CustomerAuthorization.UsageType` property is set to `DTO`, generate a license for the DTO usage model and send it to the user. 
        
        * If the `CustomerAuthorization.UsageType` property is set to `VOD`, generate a license for the VOD usage model and send it to the user.

      If none of the DRM policies allow for anonymous access, complete the following tasks:

        * If there is not a valid authentication token in the request, you need to return an "authentication required" error. 
        * Otherwise return a "not authorized" error.

* If one of the DRM policies allows for anonymous access, generate a license for the Ad-funded usage model and send it to the user.

