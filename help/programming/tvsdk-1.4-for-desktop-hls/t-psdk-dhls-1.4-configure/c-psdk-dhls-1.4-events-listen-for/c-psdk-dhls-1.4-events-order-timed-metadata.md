---
description: TVSDK dispatches timed metadata events and generates timed metadata whenever default or custom tags are encountered or when a playlist changes in a manifest. Events are dispatched in the order in which they appear in the manifest.
seo-description: TVSDK dispatches timed metadata events and generates timed metadata whenever default or custom tags are encountered or when a playlist changes in a manifest. Events are dispatched in the order in which they appear in the manifest.
seo-title: Timed metadata events
title: Timed metadata events
uuid: 69c43701-6ffa-45fe-a104-fe81391222e7
index: y
internal: n
snippet: y
---

# Timed metadata events{#timed-metadata-events}

TVSDK dispatches timed metadata events and generates timed metadata whenever default or custom tags are encountered or when a playlist changes in a manifest. Events are dispatched in the order in which they appear in the manifest.

Your player implements actions based on the following events:

* `TimedMetadataEvent.TIMED_METADATA_ID3_ADDED`: Dispatched when an ID3 timed metadata was processed. 
* `TimedMetadataEvent.TIMED_METADATA_SKIPPED`: Dispatched when timed metadata was processed and no opportunity was detected.

