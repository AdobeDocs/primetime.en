---
description: In certain analytics implementations, the client application may want to provide a different playhead position than the one reported by the TVSDK localTime value. For example, during a LINEAR stream playback, each program’s playhead can be provided relative to it’s start time.
seo-description: In certain analytics implementations, the client application may want to provide a different playhead position than the one reported by the TVSDK localTime value. For example, during a LINEAR stream playback, each program’s playhead can be provided relative to it’s start time.
seo-title: Implement custom time updates
title: Implement custom time updates
uuid: b59a4160-22fc-4f18-97a8-78f6e74bb81a
index: y
internal: n
snippet: y
---

# Implement custom time updates{#implement-custom-time-updates}

In certain analytics implementations, the client application may want to provide a different playhead position than the one reported by the TVSDK localTime value. For example, during a LINEAR stream playback, each program’s playhead can be provided relative to it’s start time.

>[!TIP]
>
>Override this method only if you want to provide a different playhead position than the default position.

1. To override the default playhead position:

   ```
   vaMetadata.currentTimeUpdateBlock = function():Number { 
      if (currentTime == 0) { 
          currentTime = getTimer(); 
      } 
      return ((getTimer() - currentTime) / 1000 + 1000); 
   }
   ```

   >[!IMPORTANT]
   >
   >The values in this code snippet are only samples. You need to use different values for your custom playhead position.
