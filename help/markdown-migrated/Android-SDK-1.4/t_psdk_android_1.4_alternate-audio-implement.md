---
description: Late-binding audio uses MediaPlayer to play a video that is specified in an M3U8 HLS playlist and that can contain several alternate audio streams.
seo-description: Late-binding audio uses MediaPlayer to play a video that is specified in an M3U8 HLS playlist and that can contain several alternate audio streams.
seo-title: Access alternate audio tracks
title: Access alternate audio tracks
---

# Access alternate audio tracks

>1. Wait for the MediaPlayer to be in at least the PREPARED state.
>   
>1. Listen for this event:
>   `codeph MediaPlayer.PlaybackEventListener.onStateChanged with state MediaPlayer.PlayerState.INITIALIZED`: The initial list of audio tracks is available.
>   
>   
>   
>1. Get the available audio tracks from the `codeph MediaPlayerItem` instance.
>       
>       `codeph mediaPlayerItem.getAudioTracks()`
>   
>1. (Optional) Present the available tracks to the user.
>   
>1. Set the selected audio track on the `codeph MediaPlayerItem` instance.
>       
>       `codeph mediaPlayerItem.selectAudioTrack(audioTrack)`
>   
>   
