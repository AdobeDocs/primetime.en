---
description: An opportunity detector is a TVADK component that detects custom tags in a stream and identifies placement opportunities. These opportunities are sent to the content resolver, which customizes the content/ad insertion workflow based on the placement opportunity properties and metadata.
seo-description: An opportunity detector is a TVADK component that detects custom tags in a stream and identifies placement opportunities. These opportunities are sent to the content resolver, which customizes the content/ad insertion workflow based on the placement opportunity properties and metadata.
seo-title: Customize opportunity detectors and content resolvers
title: Customize opportunity detectors and content resolvers
uuid: 3e70cc19-1af4-4e10-a7af-bc148ca05b61
index: y
internal: n
snippet: y
---

# Customize opportunity detectors and content resolvers{#customize-opportunity-detectors-and-content-resolvers}

An opportunity detector is a TVADK component that detects custom tags in a stream and identifies placement opportunities. These opportunities are sent to the content resolver, which customizes the content/ad insertion workflow based on the placement opportunity properties and metadata.

 TVSDK includes default opportunity detectors:

* `SpliceOutOpportunityDetector`, which understands default ad cues 
* `AdSignalingModeOpportunityGenerator`, which is responsible for creating initial ad placement opportunities based on the ad signaling mode 
* `SpliceOutOpportunityGenerator`, which is responsible for creating ad placement opportunities from any #EXT-X-CUE tag

TVSDK also includes a default content resolver that provides content to be inserted based on the metadata key in the player item:

* `AuditudeResolver`, capable of communicating with Adobe Primetime ad decisioning(previously known as Auditude) servers and returning ad breaks to be placed.

You can override the default opportunity detectors and content resolvers to customize the advertising workflow in the following ways:

* Add support for custom tag detection 
* Recognize custom tags for ad insertion 
* Create a customized ad provider 
* Black out content
