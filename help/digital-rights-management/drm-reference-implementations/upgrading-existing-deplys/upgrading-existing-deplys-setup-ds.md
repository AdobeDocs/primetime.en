---
description: null
seo-description: null
seo-title: Set up a domain server
title: Set up a domain server
uuid: bf85305e-9a00-4bc0-ba36-c870979456e4
---

# Set up a domain server{#set-up-a-domain-server}

To configure a domain server on an existing license server installation: 

1. In the [!DNL tomcat/lib] directory, open the [!DNL flashaccess-refimpl.properties] file.
1. Under the `Domain CA certificate` option, complete the Domain CA certificate.

   This certificate is then used for accepting the domain tokens.
1. Under the `Domain CA credential` option, complete the `Domain CA credential certificate (PFX)` details.

   This certificate is then used for signing domain certificates and tokens.
1. Specify the value for `DomainServerlURL`.

   If this value is set to `NULL`, the domain authentication may succeed. However, while joining the domain, a join domain error might occur.
