---
description: 302 redirect optimization minimizes the number of 302 redirect responses, which allows your application to load balance more effectively.
seo-description: 302 redirect optimization minimizes the number of 302 redirect responses, which allows your application to load balance more effectively.
seo-title: HTTP 302 redirect optimization
title: HTTP 302 redirect optimization
uuid: ce43c915-bf5f-48c9-ab39-c74d4c2f1d6b
index: y
internal: n
snippet: y
---

# HTTP 302 redirect optimization{#http-redirect-optimization}

302 redirect optimization minimizes the number of 302 redirect responses, which allows your application to load balance more effectively.

 If a main manifest request is redirected, and 302 optimization is enabled in your player, subsequent requests made for assets from that manifest will use the final domain location, which avoids additional 302 responses. This feature is enabled by default, and you can change this setting.

>[!IMPORTANT]
>
>This feature is supported only in the certified browsers that support the `responseURL` property in the `XMLHttpRequest` object.

For Flash fallback, remember the following information:

* Your end users must have Adobe Flash Player version 23 or later installed. 
* If stream integrity is disabled, 302 redirect is supported on certified browsers only.

