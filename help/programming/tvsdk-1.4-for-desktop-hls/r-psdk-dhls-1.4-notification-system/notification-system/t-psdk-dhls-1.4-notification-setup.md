---
description: You can listen for notifications and you can add your own notifications to the notification history.
seo-description: You can listen for notifications and you can add your own notifications to the notification history.
seo-title: Set up your notification system
title: Set up your notification system
uuid: 2d1876c7-4ce6-491c-880b-dd94697d4feb
---

# Set up your notification system{#set-up-your-notification-system}

You can listen for notifications and you can add your own notifications to the notification history.

 The core of the Primetime Player notification system is the Notification class, which represents a standalone notification.

The NotificationHistory class provides a mechanism for accumulating notifications. It stores a log of notification ( `NotificationHistoryItem`) objects that represents a collection of Notifications.

To receive notifications:

* Listen for notifications 
* Add notifications to the notification history

1. Listen for state changes.
1. Implement the `MediaPlayer.StatusChangeEvent.STATUS_CHANGED` event listener.
1. TVSDK passes a `MediaPlayer.StatusChangeEvent` instance to the event listener, which contains two parameters:

    * The new state ( `MediaPlayer.Status`) 
    * A `MediaPlayerNotification` object

