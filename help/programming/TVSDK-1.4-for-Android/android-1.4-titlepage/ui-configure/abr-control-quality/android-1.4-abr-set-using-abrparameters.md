---
description: You can set ABR control values only with ABRControlParameters, but you can construct a new one at any time.
seo-description: You can set ABR control values only with ABRControlParameters, but you can construct a new one at any time.
seo-title: Configure adaptive bit rates using ABRControlParameters
title: Configure adaptive bit rates using ABRControlParameters
uuid: 14e00c50-a280-4965-a991-9cd2e2ea4006
index: y
internal: n
snippet: y
---

# Configure adaptive bit rates using ABRControlParameters{#configure-adaptive-bit-rates-using-abrcontrolparameters}

You can set ABR control values only with ABRControlParameters, but you can construct a new one at any time.

 The following conditions apply to `ABRControlParameters`:

* You must provide values for all parameters at construction time. 
* You cannot change individual values after construction time. 
* If the parameters that you specify are outside of the allowed range, an `ArgumentError` is thrown.

1. Decide on initial, minimum, and maximum bit rates.
1. Determine the ABR policy:

    * `ABR_CONSERVATIVE` 
    * `ABR_MODERATE` 
    * `ABR_AGGRESSIVE`

1. Set the ABR parameter values in the `ABRControlParameters` constructor and assign them to the Media Player.

   ```java
   public ABRControlParameters(int initialBitRate, 
     int minBitRate, 
     int maxBitRate, 
     ABRControlParameters.ABRPolicy abrPolicy, 
     int minTrickPlayBitRate, 
     int maxTrickPlayBitRate, 
     int maxTrickPlayBandwidthUsage, 
     int maxPlayoutRate);
   ```

