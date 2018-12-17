---
description: You can control the visibility of closed captions. When visibility is on, the currently selected track is displayed.
seo-description: You can control the visibility of closed captions. When visibility is on, the currently selected track is displayed.
seo-title: Control closed-caption visibility
title: Control closed-caption visibility
uuid: fe1353eb-9c2a-4a59-bba5-1731e6357599
index: y
internal: n
snippet: y
---

# Control closed-caption visibility{#control-closed-caption-visibility}

You can control the visibility of closed captions. When visibility is on, the currently selected track is displayed.

>[!TIP]
>
>If you change which track is current, the visibility setting remains the same.

If closed caption text is displayed when the player enters the seek mode, the text is no longer displayed after the seek completes. Instead, after a few seconds, Browser TVSDK displays the next closed caption text in the video after the ending seek position. 

>[!TIP]
>
>The visibility values for closed captions are controlled with `MediaPlayer.VISIBLE` and `MediaPlayer.INVISIBLE`.

1. Use the `MediaPlayer.ccVisibility` property to access the current visibility setting for the closed captions.

