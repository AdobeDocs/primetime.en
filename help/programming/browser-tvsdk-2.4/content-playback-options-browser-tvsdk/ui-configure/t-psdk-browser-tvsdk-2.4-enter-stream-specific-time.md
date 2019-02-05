---
description: By default, when playback starts, VOD media starts at 0, and live media starts at the client live point (MediaPlayer.LIVE_POINT). You can override the default behavior.
seo-description: By default, when playback starts, VOD media starts at 0, and live media starts at the client live point (MediaPlayer.LIVE_POINT). You can override the default behavior.
seo-title: Enter a stream at a specific time
title: Enter a stream at a specific time
uuid: 5db73b50-0629-4fb1-8f12-6c88e4cd7109
---

# Enter a stream at a specific time{#enter-a-stream-at-a-specific-time}

By default, when playback starts, VOD media starts at 0, and live media starts at the client live point (MediaPlayer.LIVE_POINT). You can override the default behavior.

1. Pass a position to `MediaPlayer.prepareToPlay`.
1. Browser TVSDK uses this position as the starting point for the asset.

   >[!NOTE]
   >
   >No seek operation is required.

1. If the position is not inside the seekable range, the default positions are used.

   For example: 

   ```js
   var desiredPostion = //choose a value; 
   onStatusChange = function (event) { 
       case AdobePSDK.MediaPlayerStatus.INITIALIZED: 
           console.log("Player Status: INITIALIZED"); 
           player.prepareToPlay(desiredPostion); 
           break; 
   } 
   
   ```

