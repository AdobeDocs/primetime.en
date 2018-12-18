---
description: HLS streams that are delivered through a Content Delivery Network (CDN) can sometimes use authentication tokens on the manifest and segment requests for verification. These tokens can be provided as URL parameters or as cookie headers.
seo-description: HLS streams that are delivered through a Content Delivery Network (CDN) can sometimes use authentication tokens on the manifest and segment requests for verification. These tokens can be provided as URL parameters or as cookie headers.
seo-title: Tokenized segment streams
title: Tokenized segment streams
uuid: b17bb5bc-2029-4113-ac44-b1d30aa08ca6
index: y
internal: n
snippet: y
---

# Tokenized segment streams{#tokenized-segment-streams}

HLS streams that are delivered through a Content Delivery Network (CDN) can sometimes use authentication tokens on the manifest and segment requests for verification. These tokens can be provided as URL parameters or as cookie headers.

Tokens provided as cookies on the master manifest (m3u8) response are not shared with the segment (ts) requests even when the segment requests are for the same domain. To enable the sharing of these cookies in a segment request, set the following property on the `PTMetadata` instance provided to the player item:&nbsp; 

```
PTMetadata *metadata = [[[PTMetadata alloc] init] autorelease]; 
[metadata setValue:[NSNumber numberWithBool:YES] forKey:kSyncCookiesWithAVAsset]; 

```

An additional request is made to the master manifest (m3u8) before the stream begins to play.

>[!IMPORTANT]
>
>This cookie-sharing feature is only supported on devices running iOS 8 or above.

