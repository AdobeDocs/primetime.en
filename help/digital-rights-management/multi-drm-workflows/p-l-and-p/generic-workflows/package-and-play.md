---
description: You can use ExpressPlay's Bento4 packager to prepare content for any of the DRM solutions supported by Primetime Cloud DRM, powered by ExpressPlay.
seo-description: You can use ExpressPlay's Bento4 packager to prepare content for any of the DRM solutions supported by Primetime Cloud DRM, powered by ExpressPlay.
seo-title: ExpressPlay Packager / Cloud DRM / TVSDK
title: ExpressPlay Packager / Cloud DRM / TVSDK
uuid: 8e1d9d83-85fe-46a5-8d08-216cc409fac2
index: y
internal: n
snippet: y
---

# ExpressPlay Packager / Cloud DRM / TVSDK{#expressplay-packager-cloud-drm-tvsdk}

You can use ExpressPlay's Bento4 packager to prepare content for any of the DRM solutions supported by Primetime Cloud DRM, powered by ExpressPlay.

 This task describes how to use a 3rd-party tool to prepare protected content, in this case *ExpressPlay Bento4 Tools*, for use with a variety of DRM solutions. For additional information, see the *Bento4 tools* documentation on the [ExpressPlay](https://www.expressplay.com/developer/) web site. 
1. Acquire an ExpressPlay account and obtain your ExpressPlay Customer Authenticator information.

   See [Primetime DRM Cloud Quick-start.](../../../multi-drm-workflows/quick-start/quick-start.md)
1. If you are encrypting content for  Primetime Access , acquire the  Primetime Adobe Access  SDK from Adobe, along with the required certificates (License, Transport, and Packaging certs).
1. Supply a Content Encryption Key (CEK) and Content Encryption Key Storage ID (CEKSID) for use across the DRM systems. (You randomly generate these using OpenSSL or similar.)

   The CEK is the actual key you use to encrypt your video file(s). You either store it securely on your own server in your own key management system, or you can make use of ExpressPlay's [key storage solution](http://www.expressplay.com/developer/key-storage/).

   A CEKSID is the identifier for a particular CEK. You don't (usually) pass the encryption key around. For example, when requesting a license token, you provide the CEKSID. 

1. If you are encrypting content for Access, utilize your CEK to create Primetime Access metadata associated with your content.

1. Fragment your content to prepare it for the *Bento4 MP4DASH* tool.

   For this step you can use the *MP4FRAGMENT* tool. You only need to fragment your content once. For example: 

   ```
   ./mp4fragment Unfragmented.mp4 Fragmented.mp4
   ```

1. Use the *Bento4 MPDASH* tool to "DASH-ify" and encrypt your fragmented content.

   Use this command to specify all of the DRM systems you will utilize, and pass in any  Primetime Access  metadata generated from the previous steps. For example: 

   ```
   /mp4dash -f  
   --use-segment-list  
   --use-segment-timeline  
   --encryption-key=<CEKSID>:<CEK>  
   --playready  
   --Widevine  
   --Widevine-header=provider:intertrust#content_id:2a  
   --primetime  
   --primetime-metadata=@AAXS.metadata 
    Fragmented.mp4 -o DASH_OUTPUT
   ```

1. Create a "storefront server".

       This server needs to handle the following operations:

    1. Customer selection of content. This implementation needs to include an endpoint for clients to request a content token for a specific content ID. 
    1. Customer entitlement 
    1. License token (ExpressPlay) requests from the client ( [ExpressPlay license token request / response reference](../../../multi-drm-workflows/license-token-req-resp-ref/license-token-req-resp-ref.md))

1. Create your client.

       The client should include a call to your storefront server. Adobe recommends that the client call the storefront after the user selects some content, and after the user is authenticated. Then, pass the token returned from ExpressPlay to your player to use for license requests. Introductions to implementing the DRM component of your players are here:

    * [Browser TVSDK for HTML5](http://help.adobe.com/en_US/primetime/psdk/browser_tvsdk/index.html#PSDKs-reference-DRM_interface_overview) 
    * [iOS](http://help.adobe.com/en_US/primetime/psdk/ios/index.html#PSDKs-task-Enable_Apple_FairPlay_in_TVSDK_applications)

1. With the license token in hand, the client can now derive the request URL from the token and make the license request to ExpressPlay, and then play the selected, protected content for the user.