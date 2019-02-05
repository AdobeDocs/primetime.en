---
description: In some cases, you need to know whether the media content is live or VOD.
seo-description: In some cases, you need to know whether the media content is live or VOD.
seo-title: Identify whether the content is live or VOD
title: Identify whether the content is live or VOD
uuid: 4d514c46-a1d0-4721-a423-92108126e37e
---

# Identify whether the content is live or VOD{#identify-whether-the-content-is-live-or-vod}

In some cases, you need to know whether the media content is live or VOD.

1. Ensure that the player is in at least the INITIALIZED status.
1. Determine whether the `MediaPlayerItem` content is live (true) or VOD (false).

   ```
   function get isLive():Boolean;
   ```

