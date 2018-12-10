---
seo-title: Usage rules
title: Usage rules
uuid: 9d9b14bc-d35f-4889-86e4-58817a436767
index: y
internal: n
snippet: y
---

# Usage rules{#usage-rules}

With the Adobe Access Server for Protected Streaming, all usage rules are specified on the server through configuration files. Any usage rules specified in the protected content are overridden, so it is recommended to use a simple anonymous policy during content packaging. Usage rules that are configurable can be set on a per-tenant basis.

The Adobe Access Server for Protected Streaming supports the following usage rules:

* Output Protection 
* Adobe® AIR®, SWF, iOS, and Android Application Restrictions 
* DRM and Runtime Module Restrictions 
* Jailbreak detection enforcement (on Adobe Access platforms that support jailbreak detection) 
* License Caching is disabled by default. License caching can be enabled by specifying the caching end date or an amount of time caching is allowed (starting when the license is issued). 
* Multiple Play Rights, which lets you specify different combinations of Output Protection, Application Restrictions, and DRM/Runtime Restrictions. For example, it is possible to specify different Output Protection requirements for each client platform by using the DRM Module Restriction with Output Protection.

>[!NOTE] {class="- topic/note "}
>
>To support remote key delivery to iOS devices, the policy used at packaging time must have remote key delivery enabled. This setting cannot be modified through the tenant configuration on the server. ***Adobe Primetime is required to build iOS applications that can play Adobe Access-protected content.***

