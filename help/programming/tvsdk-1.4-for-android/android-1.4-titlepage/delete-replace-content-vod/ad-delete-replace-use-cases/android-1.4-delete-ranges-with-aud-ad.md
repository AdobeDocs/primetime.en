---
description: You can remove TimeRanges between begin and end in localTime from the timeline.
seo-description: You can remove TimeRanges between begin and end in localTime from the timeline.
seo-title: Delete ranges
title: Delete ranges
uuid: 2f4afa0d-69e3-4929-8dbd-b553c8a64d96
index: y
internal: n
snippet: y
---

# Delete ranges{#delete-ranges}

You can remove TimeRanges between begin and end in localTime from the timeline.

>[!NOTE]
>
>If you only want to remove certain ranges from the content, and the ad map must be used as defined by the ad server, create a `CustomRangeMetadata` instance and specify the type as a DELETE operation with the defined custom ranges.

1. Delete ranges with an Adobe Primetime ad decisioning ad.

   ```
   {   
       "properties": [],
       "stream": {
           "manifests": [
               {
                   "url": "http://xyz.cloudfront.net/e2e-vod/cloudfront_vod_hls_tos_30fps.m3u8",
                   "type": "hls"
               }
           ],
        
           "metadata": {
               "time-ranges": {
                   "type": "delete",
                   "time-range-list": [
                       {
                           "begin": 0,
                           "end": 20000
                       },
                       {
                           "begin": 69000,
                           "end": 99000
                       },
                       {
                           "begin": 251000,
                           "end": 281000
                       },
                       {
                           "begin": 514000,
                           "end": 544000
                       }
                   ]
        
               },
               "ad": {
                   "targeting": [
                       {
                           "value": "MulAdsAvail12346",
                           "key": "osmfKeyMulAdsAvail12346"
                       }
                   ],
                   "domain": "sandbox2.auditude.com",
                   "mediaid": "psdk_000105",
                   "zoneid": "121781"
               }     
           }
       },   
       "title": "VOD - DELETE TimeRange with Primetime ad decisioning Ads",
       "thumbnail": {
           "large": "http://example.com",
           "small": "http://example.com"
       },
       "type": "vod",
       "id": "vod_003"
   }
   
   ```

