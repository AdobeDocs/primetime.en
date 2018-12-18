---
description: null
seo-description: null
seo-title: Disable pre-roll ads
title: Disable pre-roll ads
uuid: 2e307a58-49f2-43d6-908b-97684ad6e3d3
index: y
internal: n
snippet: y
---

# Disable pre-roll ads{#disable-pre-roll-ads}

To disable pre-roll, change the default opportunity generators to not make the pre-roll call. The default opportunity generators is: 

```
@inheritDoc 
*/ 
override protected function doRetrieveGenerators(item:MediaPlayerItem):Vector.<OpportunityGenerator> { 
var result:Vector.<OpportunityGenerator> = new Vector.<OpportunityGenerator>(); 
result.push(new AdSignalingModeOpportunityGenerator()); 
result.push(new SpliceOutOpportunityGenerator()); 
return result; 
}
```

To disable the pre-roll on live streams, change the above to include only the SpliceOutOpportunityGenerator: 

```
@inheritDoc 
*/ 
override protected function doRetrieveGenerators(item:MediaPlayerItem):Vector.<OpportunityGenerator> { 
var result:Vector.<OpportunityGenerator> = new Vector.<OpportunityGenerator>(); 
if (preroll_enabled == true) { result.push(new AdSignalingModeOpportunityGenerator()); } 
 
result.push(new SpliceOutOpportunityGenerator()); 
return result; 
}
```

