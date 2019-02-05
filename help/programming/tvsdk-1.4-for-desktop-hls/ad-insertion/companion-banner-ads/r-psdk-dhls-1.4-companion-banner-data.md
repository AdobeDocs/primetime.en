---
description: The content of an AdBannerAsset describes a companion banner.
seo-description: The content of an AdBannerAsset describes a companion banner.
seo-title: Companion banner data
title: Companion banner data
uuid: 5ba7ec98-5339-495f-b5d3-e933394b5be1
---

# Companion banner data{#companion-banner-data}

The content of an AdBannerAsset describes a companion banner.

<!--<a id="section_D730B4FD6FD749E9860B6A07FC110552"></a>-->

The `AdPlaybackEvent.AD_STARTED` event returns an `Ad` instance that contains a `companionAssets` property ( `Vector.<AdAsset>`). 
Each `AdAsset` provides information about displaying the asset. 

<table id="table_760C885E2DCA4BE983CC57FDA7BD5B14"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Available information </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> width </td> 
   <td colname="col2"> Width of the companion banner in pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> height </td> 
   <td colname="col2"> Height of the companion banner in pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> resource type </td> 
   <td colname="col2">The resource type for this companion banner: 
    <ul id="ul_A067787FE49E4B6095BE0AC1D447DBB3"> 
     <li id="li_02B7224C67004095B3F6E50FD21E507E">html: The data is in HTML code. </li> 
     <li id="li_5F37E14472424F808C6094F42009E676">iframe: The data is an iframe URL (src). </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> banner data </td> 
   <td colname="col2"> The data of the type that is specified by <span class="codeph"> resourceType</span> for this companion banner. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> static URL </td> 
   <td colname="col2"> <p>Sometimes, the companion banner also has a staticURL that is a direct URL to the image or to a <span class="filepath"> .swf</span> (flash banner). </p> <p>If you do not want to use html or iframe, you can use a direct URL to an image or swf to display the banner in the Flash stage instead. In this case, you can use the staticURL to display the banner. </p> <p>Important:  You must check whether the static URL is a valid string, because this property might not always be available. </p> </td> 
  </tr> 
 </tbody> 
</table>

