---
description: Ad insertion resolves ads for video-on-demand (VOD), for live streaming, and for linear streaming with ad tracking and ad playback. TVSDK makes the required requests to the ad server, receives information about ads for the specified content, and places the ads in the content in phases.
seo-description: Ad insertion resolves ads for video-on-demand (VOD), for live streaming, and for linear streaming with ad tracking and ad playback. TVSDK makes the required requests to the ad server, receives information about ads for the specified content, and places the ads in the content in phases.
seo-title: Insert ads
title: Insert ads
uuid: f6636bfa-c96d-4d9d-987a-60292397525a
---

# Overview {#insert-ads}

Ad insertion resolves ads for video-on-demand (VOD), for live streaming, and for linear streaming with ad tracking and ad playback. TVSDK makes the required requests to the ad server, receives information about ads for the specified content, and places the ads in the content in phases.

An *`ad break`* contains one or more ads that play in sequence. TVSDK inserts ads in the main content as members of one or more ad breaks.

>[!NOTE]
>
>If the ad has errors, TVSDK ignores the ad.