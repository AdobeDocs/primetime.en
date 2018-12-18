---
description: The MediaPlayerItem.timedMetadata property gives you access to all the TimedMetadata objects created from playlist/manifest tags or from ID3 tags within the media stream. The MediaPlayerItem.hasTimedMetadata property indicates whether a subscribed custom tag is present in the current media.
seo-description: The MediaPlayerItem.timedMetadata property gives you access to all the TimedMetadata objects created from playlist/manifest tags or from ID3 tags within the media stream. The MediaPlayerItem.hasTimedMetadata property indicates whether a subscribed custom tag is present in the current media.
seo-title: Notifications for manifest tags
title: Notifications for manifest tags
uuid: 87bee41b-b44e-4d12-afd2-7a63023f992c
index: y
internal: n
snippet: y
---

# Notifications for manifest tags{#notifications-for-manifest-tags}

The MediaPlayerItem.timedMetadata property gives you access to all the TimedMetadata objects created from playlist/manifest tags or from ID3 tags within the media stream. The MediaPlayerItem.hasTimedMetadata property indicates whether a subscribed custom tag is present in the current media.

You can monitor timed metadata by listening for the following events, which notify your application of related activity:

* `MediaPlayerItemEvent.ITEM_CREATED`: The initial list of `TimedMetadata` objects is available after the `MediaPlayerItem` is created. This event notifies your application when this happens. 

* `MediaPlayerItemEvent.ITEM_UPDATED`: For live/linear streams where the manifest/playlist refreshes periodically, additional custom tags might appear in the updated playlist/manifest, so additional TimedMetadata objects might be added to the `MediaPlayerItem.timedMetadata` property. This event notifies your application when this happens. 

* `TimedMetadataEvent.TIMED_METADATA_AVAILABLE`: Every time that a new `TimedMetadata` object is created, this event is dispatched by the `MediaPlayer`. This event is not dispatched for the `TimedMetadata` object created during the initialization phase.

