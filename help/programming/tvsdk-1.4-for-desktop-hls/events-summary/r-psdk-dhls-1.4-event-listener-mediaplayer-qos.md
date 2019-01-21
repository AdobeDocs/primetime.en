---
description: TVSDK dispatches quality of service (QoS) events to notify your application about events that could influence the computation of QoS statistics, such as buffering or seeking.
seo-description: TVSDK dispatches quality of service (QoS) events to notify your application about events that could influence the computation of QoS statistics, such as buffering or seeking.
seo-title: QoS events
title: QoS events
uuid: fd657cf0-c6d4-4e9a-b212-7d09d483cae9
index: y
internal: n
snippet: y
---

# QoS events{#qos-events}

TVSDK dispatches quality of service (QoS) events to notify your application about events that could influence the computation of QoS statistics, such as buffering or seeking.

 To be notified about all QoS-related events, register event listeners with the `MediaPlayer` object for the following events: 

|  Event  | Meaning  |
|---|---|
| `BufferEvent. [BUFFERING_END](https://help.adobe.com/en_US/primetime/api/psdk/asdoc-dhls_1.4/com/adobe/mediacore/events/BufferEvent.html#BUFFERING_END)`  | Buffering is complete.  |
| `BufferEvent. [BUFFERING_BEGIN](https://help.adobe.com/en_US/primetime/api/psdk/asdoc-dhls_1.4/com/adobe/mediacore/events/BufferEvent.html#BUFFERING_BEGIN)`  | Buffering has started.  |
| `SeekEvent. [SEEK_COMPLETED](https://help.adobe.com/en_US/primetime/api/psdk/asdoc-dhls_1.4/com/adobe/mediacore/events/SeekEvent.html#SEEK_END)`  | Seeking is complete.  |
| `SeekEvent. [SEEK_BEGIN](https://help.adobe.com/en_US/primetime/api/psdk/asdoc-dhls_1.4/com/adobe/mediacore/events/SeekEvent.html#SEEK_BEGIN)`  | Seeking is starting.  |
| `SeekEvent. [SEEK_POSITION_ADJUSTED](https://help.adobe.com/en_US/primetime/api/psdk/asdoc-dhls_1.4/com/adobe/mediacore/events/SeekEvent.html#SEEK_POSITION_ADJUSTED)`  | TVSDK changed the seek position as a result of current advertising policies.  |

