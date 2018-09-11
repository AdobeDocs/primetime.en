---
description: TVSDK includes methods, properties, and events to determine valid rates, current rates, whether trick play is supported, and other functionality that are related to fast forward and rewind.
seo-description: TVSDK includes methods, properties, and events to determine valid rates, current rates, whether trick play is supported, and other functionality that are related to fast forward and rewind.
seo-title: Rate-change API elements
title: Rate-change API elements
uuid: ca5a004b-5eb2-4ed3-9f60-9c4278a685ad
index: y
internal: n
snippet: y
translate: y
---

# Rate-change API elements

TVSDK includes methods, properties, and events to determine valid rates, current rates, whether trick play is supported, and other functionality that are related to fast forward and rewind.


<a id="section_E5D37C71323947E2AED8B866D9835E31"></a>

Use the following API elements to change play rates: 
* `PlaybackRateEvent.getRate`
* `MediaPlayerEvent.RATE_SELECTED`
* `MediaPlayerEvent.RATE_PLAYING`
* `MediaPlayerItem.isTrickPlaySupported`
* `MediaPlayerItem.getAvailablePlaybackRates`, which specifies valid rates.






|  Rate value  | Effect on playback  |
|---|---|
|  2.0, 4.0, 8.0, 16.0, 32.0, 64.0, 128.0  | Switches to fast-forward mode with the specified multiplier faster than normal (for example, 4 is 4 times faster than normal)  |
|  -2.0, -4.0, -8.0, -16.0, -32.0, -64.0 , -128.0  | Switches to fast-rewind mode  |
|  1.0  | Switches to normal play mode (calling `play` is the same as setting the rate property to 1.0)  |
|  0.0  | Pauses (calling `pause` is the same as setting the rate property to 0.0)  |

