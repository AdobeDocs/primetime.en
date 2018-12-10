---
seo-title: Crossdomain DRM policy file
title: Crossdomain DRM policy file
uuid: 9dc6d329-251a-4331-80ba-bf45ab164e14
index: y
internal: n
snippet: y
---

# Crossdomain DRM policy file{#crossdomain-drm-policy-file}

If the license server is hosted on a different domain than the video playback SWF, then a cross-domain DRM policy file ( [!DNL crossdomain.xml]) is needed to enable the SWF to request licenses from a license server. A cross-domain DRM policy file is represented by an XML file that enables the server to indicate that its data and documents are available to SWF files served from other domains. Any SWF file served from a domain specified in the license server’s cross-domain DRM policy file is permitted to access data or assets from that license server.

Adobe recommends that developers follow best practices when deploying the cross-domain policy file by only allowing trusted domains to access the license server and limiting the access to the license sub-directory on the web server.

For more information on cross-domain DRM policy files, see the following locations:

* Web site controls (DRM policy files): [](http://help.adobe.com/en_US/ActionScript/3.0_ProgrammingAS3_Flex/WS5b3ccc516d4fbf351e63e3d118a9b90204-7e08.html) 
* Cross-domain DRM policy file specification: [https://www.adobe.com/devnet/articles/crossdomain_policy_file_spec.html](http://www.adobe.com/devnet/articles/crossdomain_policy_file_spec.html)

