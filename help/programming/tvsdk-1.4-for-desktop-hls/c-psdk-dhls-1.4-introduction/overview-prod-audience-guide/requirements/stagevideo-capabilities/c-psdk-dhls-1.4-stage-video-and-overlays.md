---
description: You can use HTML overlays with StageVideo to display UI elements in the Flash display list video plane. This plane is above the StageVideo plane, so StageVideo always displays behind any Flash display list elements.
seo-description: You can use HTML overlays with StageVideo to display UI elements in the Flash display list video plane. This plane is above the StageVideo plane, so StageVideo always displays behind any Flash display list elements.
seo-title: StageVideo and HTML Overlays
title: StageVideo and HTML Overlays
uuid: 84e862ab-4c35-47a2-9c4e-f792d3ef5363
---

# StageVideo and HTML Overlays{#stagevideo-and-html-overlays}

You can use HTML overlays with StageVideo to display UI elements in the Flash display list video plane. This plane is above the StageVideo plane, so StageVideo always displays behind any Flash display list elements.

HTML overlays are UI elements that you can display in the Flash display plane on video that is rendered by `StageVideo` on its own plane. Before Flash 15, you could not use HTML overlays when hardware acceleration was not available. Starting in Flash 15, HTML overlays display when `StageVideo` falls back to software rendering.

>[!IMPORTANT]
>
>Depending upon your system's capabilities, performance can degrade to a greater or lesser degree when you use HTML overlays.

Consider the following information:

* In Flash Player 15:

    * You can use HTML overlays whether hardware acceleration is available. 
    * To use HTML overlays, set `wmode` to `opaque`.

* In Flash Player 14:

    * When hardware acceleration is available, `StageVideo` resides below the Flash display list, so you can use HTML overlays. 
    * When hardware acceleration is not available, video is rendered on top of all other elements in the browser, which prevents the use of HTML overlays.

Here are the minimum browser requirements to use HTML overlays with `StageVideo`:

* Firefox version 4 and later 
* Safari version 4 and later 
* Internet Explorer:

    * Version 9+ on Windows 7 and later 
    * Version 10+ on Windows XP

* Chrome version 26 and later 

  >[!IMPORTANT]
  >
  >Chrome Pepper on Windows XP and Windows Vista is not supported.

