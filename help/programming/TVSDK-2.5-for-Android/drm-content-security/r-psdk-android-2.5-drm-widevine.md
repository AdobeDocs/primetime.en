---
description: You can use the Android native Widevine DRM with DASH streams.
seo-description: You can use the Android native Widevine DRM with DASH streams.
seo-title: Widevine DRM
title: Widevine DRM
uuid: 1e7d2d3a-ee38-4245-8ac1-868ca09420e0
index: y
internal: n
snippet: y
---

# Widevine DRM{#widevine-drm}

You can use the Android native Widevine DRM with DASH streams.

Call the following `com.adobe.mediacore.drm.DRMManager` API before starting play: 

```java
public static void setProtectionData( 
    String drm,  
    String licenseServerURL,   
    Map<String, String> requestProperties)
```

Arguments:

* `drm` - `"com.widevine.alpha"` for Widevine.

* `licenseServerURL` - The URL of the Widevine license server that receives license requests.
* `requestProperties` - Contains extra headers to include in the outgoing license request.

For example, when using content packaged for Expressplay DRM, use the following code before playing: 

```java
DRMManager.setProtectionData( 
  "com.widevine.alpha",  
  "https://wv.service.expressplay.com/hms/wv/rights/?ExpressPlayToken= 
<i>token</i>",  
  null); 

```

