---
seo-title: Time-based rules overview
title: Time-based rules overview
uuid: d131a064-4091-4207-a569-e582f88184bc
index: y
internal: n
snippet: y
---

# Time-based rules overview{#time-based-rules-overview}

Primetime DRM uses "soft enforcement" of time-based license restrictions. If a time right expires during playback of a video, the default behaviour of Primetime DRM is to not restrict playback until the next time the video stream is recreated (by calling `Netstream.stop()` and `Netstream.play()`).

While soft enforcement is the default behavior, you can also enable hard enforcement by performing one of the following tasks:

* Have your Video Player periodically poll the license to make sure none of the time restrictions have expired. This can be accomplished by calling `DRMManager.loadVoucher(LOCAL_ONLY).` An error code indicates that the locally-stored license is no longer valid. 
* Whenever the user clicks **[!UICONTROL Pause]**, you can record the current video timestamp and then call `Netstream.stop()`. When the user clicks the Play button, you can seek to the recorded location and then call `Netstream.play()`.
