---
description: When your playback includes advertising, Browser TVSDK dispatches events/notifications in generally expected sequences. Your player can implement actions based on events in the expected sequence.
seo-description: When your playback includes advertising, Browser TVSDK dispatches events/notifications in generally expected sequences. Your player can implement actions based on events in the expected sequence.
seo-title: Order of advertising events
title: Order of advertising events
uuid: 9787e6ac-5e52-4d7d-8fc7-f7609633707c
index: y
internal: n
snippet: y
---

# Order of advertising events{#order-of-advertising-events}

When your playback includes advertising, Browser TVSDK dispatches events/notifications in generally expected sequences. Your player can implement actions based on events in the expected sequence.

<a id="section_69E3CCBC57BB48399799876E83908348"></a>

When playing ads, the order of events is:

* `AdobePSDK.PSDKEventType.AD_BREAK_STARTED` 
* The following are dispatched for every ad in the ad break:

    * `AdobePSDK.PSDKEventType.AD_STARTED` 
    * `AdobePSDK.PSDKEventType.AD_PROGRESS` (multiple times during an ad's playback) 
    * `AdobePSDK.PSDKEventType.AD_COMPLETED`

* `AdobePSDK.PSDKEventType.AD_BREAK_COMPLETED`

The following example shows a typical progression of ad playback events:

```js
player.addEventListener(AdobePSDK.PSDKEventType.AD_BREAK_STARTED, onAdbreakStarted); 
player.addEventListener(AdobePSDK.PSDKEventType.AD_STARTED, onAdStarted); 
player.addEventListener(AdobePSDK.PSDKEventType.AD_PROGRESS, onAdProgress); 
player.addEventListener(AdobePSDK.PSDKEventType.AD_COMPLETED, onAdCompleted); 
player.addEventListener(AdobePSDK.PSDKEventType.AD_BREAK_COMPLETED, onAdbreakCompleted);
```

