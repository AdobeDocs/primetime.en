---
description: To receive notifications about tags in the manifest, register the appropriate event listener(s).
seo-description: To receive notifications about tags in the manifest, register the appropriate event listener(s).
seo-title: Add listeners for timed metadata notifications
title: Add listeners for timed metadata notifications
uuid: c10b7f5a-93e5-422c-842d-8ae4a45a27c9
index: y
internal: n
snippet: y
---

# Add listeners for timed metadata notifications{#add-listeners-for-timed-metadata-notifications}

To receive notifications about tags in the manifest, register the appropriate event listener(s).

You can monitor timed metadata by listening for the following events, which notify your application of related activity:

* `MediaPlayerItemEvent.ITEM_CREATED`: The initial list of `TimedMetadata` objects is available after the `MediaPlayerItem` is created.

  This event notifies your application when this happens. 

* `MediaPlayerItemEvent.ITEM_UPDATED`: For live/linear streams where the manifest/playlist refreshes periodically, additional custom tags might appear in the updated playlist/manifest, so additional `TimedMetadata` objects might be added to the `MediaPlayerItem.timedMetadata` property.

  This event notifies your application when this happens. 

* `TimedMetadataEvent.TIMED_METADATA_AVAILABLE`: Each time a new `TimedMetadata` object is created, this event is dispatched by the MediaPlayer.

  This event is not dispatched for the `TimedMetadata` object created during the initialization phase.

1. Implement the appropriate listeners.

   ```
   private function onItemCreated(event:MediaPlayerItemEvent):void { 
       var timedMetadataCollection:Vector.<TimedMetadata> = event.item.timedMetadata; 
       // process the timed metadata collection 
   } 
         
   private function onItemUpdated(event:MediaPlayerItemEvent):void { 
       var timedMetadataCollection:Vector.<TimedMetadata> = event.item.timedMetadata; 
       // process the timed metadata collection 
   } 
         
   private function onTimedMetadataAvailable(event:TimedMetadataEvent):void { 
       var timedMetadata:TimedMetadata = event.timedMetadata; 
       // process timed metadata 
   }
   ```

1. Register the event listeners.

   ```
   player.addEventListener(MediaPlayerItemEvent.ITEM_CREATED, onItemCreated); 
   player.addEventListener(MediaPlayerItemEvent.ITEM_UPDATED, onItemUpdated); 
   player.addEventListener(TimedMetadataEvent.TIMED_METADATA_AVAILABLE,  
                           onTimedMetadataAvailable);
   ```

ID3 metadata are dispatched through the same `TimedMetadataEvent.TIMED_METADATA_AVAILABLE`. This should not cause any confusion, however, because you can use a TimedMetadata objtec's `type` property to differentiate between TAG and ID3. For more information about ID3 tags, see [Get ID3 tags](../../../TVSDK-1.4-for-Desktop-HLS/r-psdk-dhls-1.4-notification-system/notification-system/t-psdk-dhls-1.4-id3-metadata-retrieve.md).

