---
description: You can override the default behavior for how TVSDK handles seeks over ads when using custom ad markers.
seo-description: You can override the default behavior for how TVSDK handles seeks over ads when using custom ad markers.
seo-title: Control playback behavior for seeking over custom ad markers
title: Control playback behavior for seeking over custom ad markers
uuid: 452400e2-23a3-4fde-a40d-347c4c024263
index: y
internal: n
snippet: y
---

# Control playback behavior for seeking over custom ad markers{#control-playback-behavior-for-seeking-over-custom-ad-markers}

You can override the default behavior for how TVSDK handles seeks over ads when using custom ad markers.

By default, when a user seeks into or past ad sections that result from the placement of custom ad markers, TVSDK skips the ads. This might differ from the current playback behavior for standard ad breaks. You can set TVSDK to reposition the playhead to the beginning of the most recently skipped custom ad when the user seeks past one or more custom ads. 

1. Call `CustomRangeMetadata.setAdjustSeekPosition` with `true`.

   ```java
   customRangeMetadata.setAdjustSeekPosition (true);
   ```

1. Use `customRangeMetadata` in `MediaPlayerItemConfig`.

   ```java
   // Set customRangeMetadata 
   config.setCustomRangeMetadata(customRangeMetadata); 
    
   // prepare the content for playback by calling replaceCurrentResource 
   mediaPlayer.replaceCurrentResource(mediaResource, config); 
   
   ```

