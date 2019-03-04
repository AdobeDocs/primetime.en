---
description: You can set up a user interface control for sound volume.
seo-description: You can set up a user interface control for sound volume.
seo-title: Provide volume control
title: Provide volume control
uuid: 63e96424-54d0-4c16-bd94-2366722f752a
---

# Provide volume control{#provide-volume-control}

You can set up a user interface control for sound volume.

1. Wait for the MediaPlayer instance to be in a valid state for this command, which is any except RELEASED or ERROR.
1. Call `setVolume` on the `MediaPlayer` instance to set the audio volume.

   ```java
   void setVolume(int volume) throws IllegalStateException;
   ```

   The value for the volume represents the requested volume expressed as a proportion of the maximum volume, where 0 is silent and 100 is the maximum volume. 

