---
description: Before you can use most of the TVSDK player methods, the player must be in a valid status.
seo-description: Before you can use most of the TVSDK player methods, the player must be in a valid status.
seo-title: Wait for a valid state
title: Wait for a valid state
uuid: ad9df366-c443-4e6b-a7ab-658d5691eb94
index: y
internal: n
snippet: y
---

# Wait for a valid state{#wait-for-a-valid-state}

Before you can use most of the TVSDK player methods, the player must be in a valid status.

 The player moves through various statuses. Waiting for the player to be in the correct status ensures that the media resource has successfully loaded. If the player is not in at least the required status, many player methods throw `IllegalStateException`.

The required status is usually `PTMediaPlayerStatusReady`. 
