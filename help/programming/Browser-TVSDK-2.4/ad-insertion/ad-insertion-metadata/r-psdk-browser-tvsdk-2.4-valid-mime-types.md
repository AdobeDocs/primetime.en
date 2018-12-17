---
description: An ad might have multiple creative, out of which one is selected to be played.
seo-description: An ad might have multiple creative, out of which one is selected to be played.
seo-title: Valid mime types
title: Valid mime types
uuid: 349d6699-a927-4b7e-bc97-52a349f0e9a9
index: y
internal: n
snippet: y
---

# Valid mime types{#valid-mime-types}

An ad might have multiple creative, out of which one is selected to be played.

With mime types, you can specify which creative type users can prioritize. The mime types that are specified by users and the mime types that are supported by Browser TVSDK are used to determine which creative will be prioritized.

To set the valid mime types in Browser TVSDK:

```js
var auditudeSettings = new AdobePSDK.AuditudeSettings(); 
var mimeTypes = [“video/mp4”, “application/x-mpegURL”]; 
auditudeSettings.validMimeTypes = mimeTypes; 

```

where `mimeTypes` is an array of strings, and each string represents a mime type.

In case multiple media files are returned for an ad, the selection depends upon the order in which the media files appear in `validMimeTypes` array. The mime types that have lower index are given a preference over the ones with higher index. 
