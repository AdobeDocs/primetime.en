---
seo-title: Enhanced License Chaining
title: Enhanced License Chaining
uuid: dc0e0a46-d3cd-44e8-a45d-3e22787be44e
index: y
internal: n
snippet: y
---

# Enhanced License Chaining{#enhanced-license-chaining}

With enhanced license chaining in Adobe Access 3.0, it is recommended to issue both a Leaf and a Root the first time the user requests a license for a particular machine. If the user already has the Root license, the server may issue only a Leaf (call `LicenseRequestMessage.clientHasEnhancedRootForPolicy()` to determine if the client already has a 3.0 Enhanced Root). For subsequent license requests, the client will indicate that it already has a Leaf and a Root, so the server should issue a new Root license. When the enhanced license chaining is used, `setRootKeyRetrievalInfo()` must be called to provide the credentials needed to decrypt the root encryption key in the policy.

>[!NOTE] {class="- topic/note "}
>
>If the policy supports 3.0 Enhanced License Chaining, but the client is Adobe Access 2.0, the server will issue a 2.0 original chained license. To determine the client version, use LicenseRequestMessage.getClientVersion().

