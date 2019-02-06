---
seo-title: Minimum Client Version
title: Minimum Client Version
uuid: 9f39e4e7-64eb-43ea-b194-b744838a411e
---

# Minimum Client Version{#minimum-client-version}

Adobe Access 2.0.2 and higher introduce some new usage rules, which are not understood by Adobe Access 2.0 clients. By setting the minimum supported client version ( `HandlerConfiguration.setMinSupportedClientVersion()`), the license server can control how older clients will behave when they encounter licenses with these usage rules. Based on this setting, the server can indicate whether older clients can ignore the usage rules they do not understand or whether older clients will not be able to consume licenses with those usage rules.

For example,

* If the license specifies the device capabilities requirements ( [Device capabilities required to play protected content](../../../aaxs-protecting-content/content-introduction/content-usage-rules/content-runtime-application-restrictions/content-device-capabilities.md)), Adobe Access clients 2.0.2 and higher can enforce those requirements. 
* If the license server does not want content to play on clients that do not understand the device capabilities requirements , set the minimum supported client version to 2 (for 2.0.2). This will prevent the server from issuing licenses to Adobe Access clients before 2.0.2. The minimum client version will also be enforced if the license is transferred from one client to another. 
* If the license server wants to allow older clients to ignore the device capabilities requirements, set the minimum supported client version to 1 (for Adobe Access 2.0). The server will issue a license to any client version 2.0 and higher. If the client upgrades or transfers the license to another client with version 2.0.2 or higher, the device capabilities requirements in the license will be enforced, since the client would now support that usage rule.

