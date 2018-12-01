---
description: You can control the visibility of closed captions. When visibility has been enabled, the currently selected track is displayed. If you change which track is current, the visibility setting remains the same.
seo-description: You can control the visibility of closed captions. When visibility has been enabled, the currently selected track is displayed. If you change which track is current, the visibility setting remains the same.
seo-title: Control closed-caption visibility
title: Control closed-caption visibility
uuid: e350cdc4-d333-4592-9427-69d625ec9d06
index: y
internal: n
snippet: y
---

# Control closed-caption visibility{#control-closed-caption-visibility}

You can control the visibility of closed captions. When visibility has been enabled, the currently selected track is displayed. If you change which track is current, the visibility setting remains the same.

>[!TIP]
>
>If closed caption text is displayed when the player enters seek mode, the text no longer displays after the seek completes. Instead, after a few seconds, TVSDK displays the next closed caption text in the video after the ending seek position. 
>
>The visibility values for closed captions are defined in `MediaPlayer.Visibility`. >
>```java>
>enum Visibility {  
>    VISIBLE,  
>    INVISIBLE 
>}
>```>

1. Wait for the `MediaPlayer` to be in at least the PREPARED status.

   For more information, see  ui-state-prepared-wait-for .
1. To get the current visibility setting for closed captions, use the getter method in `MediaPlayer`, which returns a visibility value.

   ```java
   MediaPlayer.Visibility getCCVisibility() throws MediaPlayerException;
   ```

1. To change the visibility for closed captions, use the setter method, passing a visibility value from `MediaPlayer.Visibility`.

   For example: 

   ```java
   mediaPlayer.setCCVisibility(MediaPlayer.Visibility visibility);
   ```

