---
description: You can use to retrieve information about the media that you can display on the seek bar.
seo-description: You can use to retrieve information about the media that you can display on the seek bar.
seo-title: Display the duration, current time, and remaining time of the video
title: Display the duration, current time, and remaining time of the video
uuid: 3d54cb90-8b86-4808-871b-9eaefdf2420f
index: n
internal: n
snippet: y
translate: y
---

# Display the duration, current time, and remaining time of the video


>1. Wait for your player to be in the INITIALIZED status.
>1. Retrieve the current playhead time using the ` MediaPlayer.currentTime` property.
>   This returns the current playhead position on the virtual timeline in milliseconds. The time is calculated relative to the resolved stream that might contain multiple instances of alternate content, such as multiple ads or ad breaks spliced into the main stream. For live/linear streams, the returned time is always in the playback window range.
>
>   ```
>   function get currentTime():Number;
>   ```

>
>1. Retrieve the playback range of the stream and determine the duration.
>   >1. Use the ` mediaPlayer.playbackRange` property to get the virtual timeline time range.
>   >
>   >   ```
>   >   function get playbackRange():TimeRange;
>   >   ```
>   >
>   >1. Parse the time range using ` mediacore.utils.TimeRange`.
>   >1. To determine the duration, subtract the start from the end of the range.
>   >   This includes the duration of additional content that is inserted into the stream (ads).
>   >
>   >   For VOD, the range always begins with zero and the end value equals the sum of the main content duration and the durations of additional content that is inserted in the stream (ads).
>   >   For a linear/live asset, the range represents the playback window range, and this range changes during playback.
>   >   <!-- PH element: phrases/primetime-sdk-name --> dispatches a ` MediaPlayerItemEvent.ITEM_UPDATED` event to indicate that the media item was refreshed and that its attributes (including the playback range) were updated. 
>   >
>1. Use the methods available on the ` MediaPlayer` and the ` HSlider` class that is publicly available in the Flex SDK to set up the seek-bar parameters.
>
>1. Use a timer to periodically retrieve the current time and update the ` SeekBar`.
