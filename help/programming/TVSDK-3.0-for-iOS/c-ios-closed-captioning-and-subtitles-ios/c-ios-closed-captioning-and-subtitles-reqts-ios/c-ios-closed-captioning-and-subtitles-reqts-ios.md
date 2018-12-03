---
description: Closed captions and subtitles have some unique differences, and you enable them in different ways.
seo-description: Closed captions and subtitles have some unique differences, and you enable them in different ways.
seo-title: Requirements for subtitles and closed captions
title: Requirements for subtitles and closed captions
uuid: 68179fce-5f8d-41c0-8a0c-635415c2e788
index: y
internal: n
snippet: y
---

# Requirements for subtitles and closed captions{#requirements-for-subtitles-and-closed-captions}

Closed captions and subtitles have some unique differences, and you enable them in different ways.

Subtitle streams run in parallel with the main content. Closed captions are part of the data packets of the MPEG-2 video streams.

You should be aware of the following requirements for closed captions and subtitles:

* **Closed captions**

    * Closed captions are typically in the same language as the audio and also represent background sounds as text. 
    * Closed captions are part of the data packets of the MPEG-2 video streams in the video transmission stream. 
    * Closed captions are supported to the extent provided by the AV Foundation framework.

* **Subtitles**

    * Subtitles are typically in a different language and do not include background sounds. 
    * Subtitles are in streams that run in parallel with the main content.

      The `PTMediaPlayer` plays the main content and ads, where the main content could be live/linear or VOD, and ads could be pre-roll, mid-roll, or post-roll.

  Here are some additional requirements for subtitles in iOS:

    * For timestamps, the `X-TIMESTAMP-MAP` value, which is specified in the header section of the `WebVTT` file, must match the video timestamp. 
    
    * For the system, you must use iOS 6.1 or later.

>[!IMPORTANT]
>
>The requirements for subtitles do not apply to closed captions.

