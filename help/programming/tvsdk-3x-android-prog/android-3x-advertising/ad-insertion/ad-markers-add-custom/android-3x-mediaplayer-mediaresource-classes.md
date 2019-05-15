---
description: A MediaResource represents the content that is about to be loaded by the MediaPlayer instance.
seo-description: A MediaResource represents the content that is about to be loaded by the MediaPlayer instance.
seo-title: MediaPlayer and MediaResource classes
title: MediaPlayer and MediaResource classes
uuid: e198f599-22ca-4ea4-bbbb-e239c79174ae
---

# MediaPlayer and MediaResource classes {#mediaplayer-and-mediaresource-classes}

A MediaResource represents the content that is about to be loaded by the MediaPlayer instance.

<!--<a id="section_431AB7221E0249BF949EC72EEB9B428A"></a>-->

TVSDK provides the means to load and prepare content for playback by using the `replaceCurrentResource` method in `MediaPlayer`. This method takes two arguments, an instance of `MediaPlayerResource` and, optionally, an instance of `MediaPlayerItemConfig`, which you can use to pass application-defined custom parameters.

* For more details see [Reuse or remove a MediaPlayer instance](../../../../tvsdk-3x-android-prog/android-3x-content-playback-options-android2/mediaplayerobjects-working-with/android-3x-mediaplayer-reuse-or-remove.md). 
* For details of `MediaPlayerResource`, see [Create a media resource](../../../../tvsdk-3x-android-prog/android-3x-content-playback-options-android2/mediaplayer-initialize-for-video/android-3x-media-resource-create.md).