---
description: You can set ABR control values only with ABRControlParameters, but you can construct a new one at any time.
seo-description: You can set ABR control values only with ABRControlParameters, but you can construct a new one at any time.
seo-title: Configure adaptive bit rates using ABRControlParameters
title: Configure adaptive bit rates using ABRControlParameters
uuid: d6c528f9-809d-4b4f-bf1d-d54839568ad5
index: n
internal: n
snippet: y
translate: y
---

# Configure adaptive bit rates using ABRControlParameters

The following conditions apply to ` ABRControlParameters`: 
* You must provide values for all parameters at construction time.
* You cannot change individual values after construction time.
* If the parameters that you specify are outside of the allowed range, an ` ArgumentError` is thrown.


>1. Decide on initial, minimum, and maximum bit rates.
>1. Determine the ABR policy:
>    
>    * ` ABR_CONSERVATIVE`
>    * ` ABR_MODERATE`
>    * ` ABR_AGGRESSIVE`

>    
>1. Set the ABR parameter values in the ` ABRControlParameters` constructor and assign them to the Media Player.
>
>   ```
>   java>   public ABRControlParameters(int initialBitRate, 
>     int minBitRate, 
>     int maxBitRate, 
>     ABRControlParameters.ABRPolicy abrPolicy, 
>     int minTrickPlayBitRate, 
>     int maxTrickPlayBitRate, 
>     int maxTrickPlayBandwidthUsage, 
>     int maxPlayoutRate);
>   ```
>
