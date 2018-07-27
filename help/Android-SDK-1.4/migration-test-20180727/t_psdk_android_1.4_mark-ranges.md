---
description: You can designate time intervals in VOD content as ad breaks.
seo-description: You can designate time intervals in VOD content as ad breaks.
seo-title: Mark ranges
title: Mark ranges
uuid: 9e7b4cce-e83b-4fe2-82a1-556e85afce39
index: n
internal: n
snippet: y
translate: y
---

# Mark ranges

In this case, `TimeRanges` between the `begin` and `end` in `localTime` will be marked as an `AdBreak` in the timeline. Other Ad settings are ignored. 

>[!NOTE]
>
>If you only want to mark certain ranges in the content as ads (with no dynamic ad insertion), create a `CustomRangeMetadata` instance, and specify the type as a MARK operation with the defined custom ranges. 


>1. Mark ranges.
>
>   ```
>   {   
>       "properties": [],
>       "stream": {
>           "manifests": [ {
>               "url": "http://d398890tia84ty.cloudfront.net/e2e-vod/cloudfront_vod_hls_tos_30fps.m3u8",
>               "type": "hls"
>           } ],
>           "metadata": {
>               "time-ranges": {
>                   "type": "mark",
>                   "adjust-seek-position" : true,   
>                   "time-range-list": [ {
>                       "begin": 0,
>                       "end": 15000
>                    },
>                    {
>                        "begin": 69000,
>                        "end": 99000
>                    },
>                    {
>                        "begin": 251000,
>                        "end": 281000
>                    },
>                    {
>                        "begin": 514000,
>                        "end": 544000
>                    } ]
>               }
>           }           
>       },   
>       "title": "VOD - MARK TimeRanges and no ads",
>       "thumbnail": {
>           "large": "http://example.com",
>           "small": "http://example.com"
>          },
>       "type": "vod",
>       "id": "vod_004"
>   }
>   
>   ```
>
