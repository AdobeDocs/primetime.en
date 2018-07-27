---
description: Custom ad markers allow you to pass a set of TimeRange specifications that represent timeline segments to .
seo-description: Custom ad markers allow you to pass a set of TimeRange specifications that represent timeline segments to .
seo-title: TimeRange class
title: TimeRange class
uuid: caeafac1-9609-4e51-8d9a-9814ef4c99de
index: n
internal: n
snippet: y
translate: y
---

# TimeRange class


<a id="section_42EB6D62627A424ABA250E3246EFEFC3"></a>

Each `TimeRange` specification in the set represents a segment on the playback timeline that is maintained internally by  <!-- PH element: phrases/primetime-sdk-name --> and that must be appropriately marked as an ad-related period.
The `TimeRange` class is a simple data structure that exposes the start position and the end position on the timeline. These two read-only properties abstract the idea of a time range in the playback timeline. 
>[!TIP]
>
>Both values are expressed in milliseconds.


Here is a summary of the `TimeRange` class: 
```
javapublic final class TimeRange {
    // the start/end values are provided at construction time
    public static TimeRange createRange(long begin, long duration) {...} 

    // only getters are available
    public long getBegin() {...} 
    public long getEnd() {...} 
    public long getDuration() {...}
}

```

