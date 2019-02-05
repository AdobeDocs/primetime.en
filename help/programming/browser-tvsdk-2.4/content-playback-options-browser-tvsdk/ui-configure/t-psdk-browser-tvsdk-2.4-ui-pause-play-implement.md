---
description: You can add Browser TVSDK behavior to pause and play buttons.
seo-description: You can add Browser TVSDK behavior to pause and play buttons.
seo-title: Play and pause a video
title: Play and pause a video
uuid: 4053ea9e-6b74-41e9-ad04-087ad13e3698
---

# Play and pause a video{#play-and-pause-a-video}

You can add Browser TVSDK behavior to pause and play buttons.

1. Create a pause/play button that does the following.
   1. Wait for your player to be in at least the PREPARED state.
   1. To start playback, call the Browser TVSDK play method:

      ```js   
      play() → {AdobePSDK.PSDKErrorCode.SUCCESS}
      ```

   1. To pause playback, call the Browser TVSDK pause method:

      ```java   
      void pause() throws IllegalStateException;
      ```

1. Listen for the `AdobePSDK.MediaPlayerStatusChangeEvent` event to check for errors or to take other appropriate actions.

   Browser TVSDK triggers this event when pause or play methods are called and passes information about the event object, including the new state, such as `MediaPlayerStatus.PLAYING` or `MediaPlayerStatus.PAUSED`. 

