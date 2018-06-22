---
description: The reference implementation illustrates how to set up the player for ads, which includes setting up video metadata for ad insertion and resolving the pre-, mid-, and post-roll ads into VOD or live/linear video streams. It also illustrates how to handle clickable ads.
seo-description: The reference implementation illustrates how to set up the player for ads, which includes setting up video metadata for ad insertion and resolving the pre-, mid-, and post-roll ads into VOD or live/linear video streams. It also illustrates how to handle clickable ads.
seo-title: Ad insertion
title: Ad insertion
---

# Ad insertion

The process of setting up a player for ad insertion includes:

* **Input feed: **Populating an input feed with ad metadata. See [Catalog format](c_psdk_ref-catalog-format.md).
* **Reference implementation feed adapter: **Parsing the input feed to populate an ad metadata object.
* **AdsManager:** Using the AdsManager to retrieve the ad metadata and create the corresponding AdProvider.
