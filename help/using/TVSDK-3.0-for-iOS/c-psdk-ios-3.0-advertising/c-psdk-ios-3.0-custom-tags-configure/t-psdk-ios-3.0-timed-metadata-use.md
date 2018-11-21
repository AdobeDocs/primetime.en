---
description: You can use TimedMetadata when the current playback time matches the start time.
seo-description: You can use TimedMetadata when the current playback time matches the start time.
seo-title: Use timed metadata
title: Use timed metadata
uuid: 8c68c4de-94c8-420e-938c-5a1c90d7c861
index: y
internal: n
snippet: y
---

# Use timed metadata{#use-timed-metadata}

You can use TimedMetadata when the current playback time matches the start time.

To use these saved `PTTimedMetadata` objects during playback, use the saved  dictionary  from [Store timed-metadata objects as they are dispatched](../../c-psdk-ios-3.0-advertising/c-psdk-ios-3.0-custom-tags-configure/t-psdk-ios-3.0-timed-metadata-store.md#task_timed_metadata_store). 

1. Extract and update the current playback time from this notification and find all of the `PTTimedMetadata` objects with start times that match the current playback time.

   You can use these objects to complete various actions.

   For example: 

   ```
   - (void) onMediaPlayerTimeChange:(NSNotification *)notification 
   { 
       CMTimeRange seekableRange = self.player.seekableRange; 
       if (CMTIMERANGE_IS_VALID(seekableRange)) 
       { 
           int currentTime = (int) CMTimeGetSeconds(self.player.currentTime); 
           NSArray *allKeys = timedMetadataCollection ? [timedMetadataCollection allKeys] : [NSArray array]; 
           NSMutableArray *timedMetadatasToDelete = [[[NSMutableArray alloc] init] autorelease]; 
           int count = [allKeys count]; 
     
           for (int i=count - 1; i > -1; i--) 
           { 
              NSNumber *currTimedMetadataTime = allKeys[i]; 
              if ([currTimedMetadataTime integerValue] == currentTime) 
              { 
               /* 
                   Use the timed metadata here and remove it from the collection. 
               */ 
                NSLog (@"IN PLAYBACK TIME %i TO EXECUTE TIMEDMETADATA %@ scheduled at time %f",currentTime,currTimedMetadata.name,CMTimeGetSeconds(currTimedMetadata.time)); 
                 
               PTTimedMetadata *currTimedMetadata = [timedMetadataCollection objectForKey:currTimedMetadataTime]; 
               [timedMetadatasToDelete addObject:currTimedMetadataTime]; 
              } 
           } 
            
           for (int i=0; i<[timedMetadatasToDelete count]; i++) 
           { 
               NSNumber *timedMetadataToDelete = timedMetadatasToDelete[i]; 
               [timedMetadataCollection removeObjectForKey:timedMetadataToDelete]; 
           } 
       } 
   }
   ```

1. Periodically flush stale `PTTimedMetadata` instances from the list to prevent memory from continuously growing.
