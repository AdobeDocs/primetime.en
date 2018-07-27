---
description: Events from indicate the state of the player, errors that occur, the completion of actions that you have requested, such as a video starting to play, or actions that occur implicitly, such as an ad completing.
seo-description: Events from indicate the state of the player, errors that occur, the completion of actions that you have requested, such as a video starting to play, or actions that occur implicitly, such as an ad completing.
seo-title: Listen for Primetime Player events
title: Listen for Primetime Player events
uuid: f581a98f-1633-4659-ac54-5e090855c623
index: n
internal: n
snippet: y
translate: y
---

# Listen for Primetime Player events

Because your application needs to respond to many of these events, you need to implement event-handing routines and register these routines with  <!-- PH element: phrases/primetime-sdk-name --> . The routines call the relevant <!-- PH element: phrases/primetime-sdk-name --> methods to respond appropriately.
Here is some additional information about events: 
* The real-time nature of video playback requires asynchronous (nonblocking) activity for many  <!-- PH element: phrases/primetime-sdk-name --> operations.
* <!-- PH element: phrases/primetime-sdk-name --> supports an event-driven video player.It provides events that correspond to all important steps in the playing process. You register those events with your platform's event mechanism and create event handlers that will be called when those events occur. * `Event Handlers` * are also known as callback routines or event listeners.  <!-- PH element: phrases/primetime-sdk-name --> provides a complete range of methods that can be used by the event handlers.

* Your application generally initiates non-blocking operations, such as requesting that a video start playing.  <!-- PH element: phrases/primetime-sdk-name --> communicates asynchronously with your application by dispatching events, such as when the video starts playing and an event when the video finishes. Other events can indicate status changes in your player and error conditions. Your event handlers take appropriate actions.


