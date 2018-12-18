---
description: TVSDK applies creative selection rules in the following ways 
seo-description: TVSDK applies creative selection rules in the following ways 
seo-title: Applying creative selection rules
title: Applying creative selection rules
uuid: 3949bc24-3060-408b-adae-947be790a8ff
index: y
internal: n
snippet: y
---

# Applying creative selection rules{#applying-creative-selection-rules}

TVSDK applies creative selection rules in the following ways:

* TVSDK applies all `default` rules first, followed by the zone-specific rules. 
* TVSDK ignores any rules that are not defined for the current zone ID. 
* Once TVSDK applies the default rules, the zone-specific rules can further change the creative priorities based on the `host` (domain) matches on the creative selected by the `default` rules. 

* In the included sample rules file with additional zone rules, once TVSDK applies the `default` rules, if the M3U8 creative domain does not contain [!DNL my.domain.com] or [!DNL a.bcd.com] and the ad zone is `1234`, the creatives are re-ordered and the Flash VPAID creative is played first if available. Otherwise an MP4 ad is played, and so on down to JavaScript. 

* If an ad creative is selected that TVSDK cannot play natively ( [!DNL .mp4], [!DNL .flv], etc.), TVSDK issues a repackaging request.

Note that the ad types that can be handled by TVSDK are still defined through the `validMimeTypes` setting in `AuditudeSettings`. 
