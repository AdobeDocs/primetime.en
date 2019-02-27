---
description: You can mark, delete, and replace time ranges in VOD streams by using different ad signaling mode and ad metadata combinations. Different combinations of signaling mode and metadata result in different behaviors.
seo-description: You can mark, delete, and replace time ranges in VOD streams by using different ad signaling mode and ad metadata combinations. Different combinations of signaling mode and metadata result in different behaviors.
seo-title: Effect on ad insertion and deletion from ad signaling mode and ad metadata combinations
title: Effect on ad insertion and deletion from ad signaling mode and ad metadata combinations
uuid: 49abab49-4e52-477d-b7ed-688ee63e7473
---

# Effect on ad insertion and deletion from ad signaling mode and ad metadata combinations {#effect-on-ad-insertion-and-deletion-from-ad-signaling-mode-and-ad-metadata-combinations}

You can mark, delete, and replace time ranges in VOD streams by using different ad signaling mode and ad metadata combinations. Different combinations of signaling mode and metadata result in different behaviors.

>[!TIP]
>
>When there is a conflict between time ranges and ad signaling modes, TVSDK gives the time ranges priority.

The following table provides the details about the signaling mode and metadata combination behaviors: 

**Server Map**

| **Ad Metadata** | **Resolvers Created** |**`PlacementInformations` created** | **Resulting behavior** |
|--- |--- |--- |--- |
||Delete|Delete|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE)`|Ranges deleted|
|Delete, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE),` <br>`PlacementInfo (Type.SERVER_MAP, Mode.INSERT)`|Ranges deleted, Ads inserted|
|Auditude|Auditude|`PlacementInfo (Type.SERVER_MAP, Mode.INSERT)`|Ads inserted|
|Replace, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE), PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.REPLACE)`|Ranges replaced|
|Mark|CustomAd|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked|
|Mark, Auditude|CustomAd, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked, no ads inserted|

**Manifest Cues**

| Ad Metadata | Resolvers Created |`PlacementInformations` created | Resulting behavior |
|--- |--- |--- |--- |
|Auditude|Auditude|`PlacementInfo (Type.PRE_ROLL, Mode.INSERT)`|Ads inserted|
|Delete, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE)`<br>`PlacementInfo (Type.PRE_ROLL, Mode.INSERT)`|Ranges deleted, ads inserted|
|Mark, Auditude|Mark, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked, no ads inserted|
|Delete|Delete|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE)`|Ranges deleted|
|Mark|CustomAd|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked|
|Replace, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE), PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.REPLACE)`|Ranges replaced|

**Custom Time Range**

| Ad Metadata | Resolvers Created |`PlacementInformations` created | Resulting behavior |
|--- |--- |--- |--- |
|Delete|Delete|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE)`|Ranges deleted|
|Delete, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE)`|Ranges deleted, no ads inserted|
|Auditude|Auditude|None|No ads inserted|
|Replace, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE), PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.REPLACE)`|Ranges replaced with ads|
|Mark|CustomAd|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked|
|Mark, Auditude|Custom Ad, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked, no ads inserted|

**Not set (default)**

| Ad Metadata | Resolvers Created |`PlacementInformations` created | Resulting behavior |
|--- |--- |--- |--- |
|Delete|Delete|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE)`|Ranges deleted|
|Delete, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE), PlacementInfo (Type.SERVER_MAP, Mode.INSERT)`|Ranges deleted, ads inserted|
|Auditude|Auditude|`PlacementInfo (Type.SERVER_MAP, Mode.INSERT)`|Ads inserted|
|Replace, Auditude|Delete, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.DELETE), PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.REPLACE)`|Ranges replaced with ads|
|Mark|CustomAd|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked|
|Mark, Auditude|CustomAd, Auditude|`PlacementInfo (Type.CUSTOM_TIME_RANGE, Mode.MARK)`|Ranges marked|