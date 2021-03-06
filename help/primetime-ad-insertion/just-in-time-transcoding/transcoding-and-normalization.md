---
title: Transcoding and Normalization
description: Transcoding and Normalization
copied-description: yes
exl-id: 48d9d971-4b15-4f1b-8740-c21983a3e835
---
# Transcoding and Normalization {#transcoding-and-normalization}

Primetime Ad Insertion will attempt to ensure a consistent viewing experience across content and ads by attempting to match:

1. Source stream codecs and bit rates, while always selecting the highest quality/bitrate creative when transcoding

1. Source stream fragment sizes (HLS/#EXT-X-TARGETDURATION)

1. Preferred creative formats for transcoding

1. Audio auto-leveling to ensure a consistent dB level across all ad creatives.

>[!NOTE]
>
>HLS assets generated by the Primetime Ad Insertion just-in time transcoding produce HLS assets of version 3, regardless of which HLS version is defined in content.
