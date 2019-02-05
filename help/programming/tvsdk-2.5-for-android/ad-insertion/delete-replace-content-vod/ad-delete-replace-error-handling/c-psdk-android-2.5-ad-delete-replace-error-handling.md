---
description: TVSDK handles time range errors according to the specific problem by merging or reordering the improperly defined time ranges.
seo-description: TVSDK handles time range errors according to the specific problem by merging or reordering the improperly defined time ranges.
seo-title: Ad deletion and replacement error handling
title: Ad deletion and replacement error handling
uuid: 9a951bc4-b372-4655-8510-3f474171415d
---

# Ad deletion and replacement error handling{#ad-deletion-and-replacement-error-handling}

TVSDK handles time range errors according to the specific problem by merging or reordering the improperly defined time ranges.

TVSDK manages `timeRanges` errors through default merging and reordering processes. First, the player sorts customer-defined time ranges by the *begin* time. Based on this sorting order, if there are subsets and intersections among the ranges, TVSDK merges adjacent ranges and joins these ranges.

TVSDK handles time-range errors with the following options:

* **Out of order** TVSDK reorders the time ranges. 

* **Subset** TVSDK merges the time-range subsets. 

* **Intersect** TVSDK merges the intersecting time ranges. 

* **Replace ranges conflict** TVSDK selects the replace duration from the earliest `timeRange` that appears in the conflicting group.

TVSDK handles signaling-mode conflicts with ad metadata in the following ways:

* If the ad signaling mode conflicts with the time-range metadata, the time-range metadata always has priority.

  For example, if the ad signaling mode is set as server map or manifest cues, and there are also MARK time rangesin the ad metadata, the resulting behavior is that the ranges are marked, and no ads are inserted. 
* For REPLACE ranges, if the signaling mode is set as the server map or manifest cues, the ranges are replaced as specified in the REPLACE ranges, and there is no ad insertion through server map or manifest cues.

  For more information, see the *Signaling Mode / Metadata Combination Behaviors* table in [Effect on ad insertion and deletion from ad signaling mode...](../../../../tvsdk-2.5-for-android/ad-insertion/delete-replace-content-vod/c-psdk-android-2.5-signaling-mode-metadata-combos-android.md#c_psdk_signaling-mode-metadata-combos-android).

Remember the following:

* When the server does not return valid `AdBreaks`, TVSDK generates and processes a `NOPTimelineOperation` for the empty AdBreak, and no ad plays. 

* Although C3 ad delete/replacement is intended to be supported only for VOD, if specified in the ad metadata, time ranges are also processed for live streams.

