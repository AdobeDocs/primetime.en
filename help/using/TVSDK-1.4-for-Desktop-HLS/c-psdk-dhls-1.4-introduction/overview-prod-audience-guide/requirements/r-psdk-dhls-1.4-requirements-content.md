---
description: Check the restrictions and requirements for streams and playlists (manifests), including DRM encryption keys.
seo-description: Check the restrictions and requirements for streams and playlists (manifests), including DRM encryption keys.
seo-title: Content and manifest requirements
title: Content and manifest requirements
uuid: 79861e3d-552a-48b5-af73-92dc62b1ad33
index: y
internal: n
snippet: y
---

# Content and manifest requirements{#content-and-manifest-requirements}

Check the restrictions and requirements for streams and playlists (manifests), including DRM encryption keys.

| Include and set the `RESOLUTION` property for each ABR stream in the manifest file. You must use Flash Player 14 or later. |
|---|
|  If the DRM-protected stream is multiple bit rate (MBR), the DRM encryption key used for the MBR should be the same as the key used in all the bit-rate streams.  |
|  Must have the same bit-rate renditions as the renditions of the main content.  |
