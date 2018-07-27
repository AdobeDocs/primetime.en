---
description: When an entire playlist is missing, for example, when the M3U8 file specified in a top-level manifest file does not download, attempts to recover. If it cannot recover, your application determines the next step.
seo-description: When an entire playlist is missing, for example, when the M3U8 file specified in a top-level manifest file does not download, attempts to recover. If it cannot recover, your application determines the next step.
seo-title: Missing playlist failover
title: Missing playlist failover
uuid: 6a53c416-d60c-4d69-a0d7-187946da1269
index: n
internal: n
snippet: y
translate: y
---

# Missing playlist failover

If the playlist that is associated with the middle-resolution bit rate is missing,  <!-- PH element: phrases/primetime-sdk-name --> searches for a variant playlist at the same resolution. If it finds the same resolution, it starts downloading the variant playlist and the segments from the matching position. If <!-- PH element: phrases/primetime-sdk-name --> does not find the same resolution playlist, it will try to cycle through other bitrate playlists and their variants. An immediately lower bitrate is the first choice, then its variant, and so on. If all of the lower bitrate playlists and their variants are exhausted in the attempt to find a valid playlist, <!-- PH element: phrases/primetime-sdk-name --> will go to the top bitrate and count down from there. If a valid playlist cannot be found, the process fails, and the player moves to the ERROR state.
Your application can determine how to handle this situation. For example, you might want to close the player activity and direct the user to the catalog activity. The event of interest is the ` STATE_CHANGED` event, and the corresponding callback is the ` onStateChanged` method. Here is code that monitors whether the player changes its internal state to ERROR: 

```
javacase ERROR: 
    getActivity().finish(); // this is where we close the current activity (the Player activity) 
    break;
```
For more information, see the ` PlayerFragment.java` file in your SDK: 
```
[…]/samples/PrimetimeReference/src/PrimetimeReference/src/com/adobe/primetime/reference/ui/player/
```

If the client side network is down, you can use this code to verify.

```
psdkutils::PSDKString 
getNetworkDownVerificationUrl() const { return 
_networkDownVerificationUrl; }
```

API will provide the url that is used to verify if the client side network is down. This should be a valid url, which returns http response code 200 on http requests.

```
psdkutils::PSDKErrorCode 
 setNetworkDownVerificationUrl(psdkutils::PSDKString value) {  
_networkDownVerificationUrl = value; return psdkutils::kECSuccess; }
```

If setNetworkDownVerificationUrl is not set, TVSDK uses the MainManifest url by default to figure if the network is down.
