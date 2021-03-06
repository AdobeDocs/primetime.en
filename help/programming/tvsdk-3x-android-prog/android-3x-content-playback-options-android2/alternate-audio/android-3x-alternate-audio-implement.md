---
description: Alternate audio uses MediaPlayer to play a video that is specified in an M3U8 HLS playlist and that can contain several alternate audio streams.
title: Access alternate audio tracks
exl-id: 88fa8f42-59d7-4a57-90c6-4c23b2ea7e00
---
# Access alternate audio tracks{#access-alternate-audio-tracks}

Alternate audio uses MediaPlayer to play a video that is specified in an M3U8 HLS playlist and that can contain several alternate audio streams.

1. Wait for the `MediaPlayer` to be in at least the `MediaPlayerStatus.PREPARED` status.
1. Listen for the `MediaPlayerEvent.STATUS_CHANGED` event with status `MediaPlayerStatus.PREPARED`.

   This step means that the initial list of audio tracks is available. 

1. Get the available audio tracks from the `MediaPlayerItem` instance.

   ```java
   mediaPlayerItem.getAudioTracks()
   ```

1. (Optional) Present the available tracks to the user.
1. Set the selected audio track on the `MediaPlayerItem` instance.

   ```java
   mediaPlayerItem.selectAudioTrack(audioTrack)
   ```
