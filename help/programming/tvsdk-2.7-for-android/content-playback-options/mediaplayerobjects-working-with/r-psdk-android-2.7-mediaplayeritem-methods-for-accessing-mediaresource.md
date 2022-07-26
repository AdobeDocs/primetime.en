---
description: The methods in the MediaPlayerItem class allow you to obtain information about the content stream represented by a loaded MediaResource.
title: MediaPlayerItem methods for accessing MediaResource information
exl-id: 5e4434ce-d2b1-4b7b-b3d1-77f62ff46d36
---
# MediaPlayerItem methods for accessing MediaResource information {#mediaplayeritem-methods-for-accessing-mediaresource-information}

The methods in the MediaPlayerItem class allow you to obtain information about the content stream represented by a loaded MediaResource.

<table frame="all" colsep="1" rowsep="1" id="table_F6006A9167044AC087A6ECB20B8CCD5D"> 
 <thead> 
  <tr rowsep="1"> 
   <th colname="2" class="entry"> Method </th> 
   <th colname="3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Ad tags</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt;String&gt; getAdTags() </span> </td> 
   <td colname="3"> Provides the list of ad tags that are used for the ad placement process. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Live stream</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean isLive(); </span> </td> 
   <td colname="3"> True if the stream is live; false if it is VOD. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>DRM protected</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean isProtected(); </span> </td> 
   <td colname="3"> True if the stream is DRM protected. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt;DRMMetadataInfo&gt; getDRMMetadataInfos(); </span> </td> 
   <td colname="3"> Lists all the DRM metadata objects discovered in the manifest. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Closed captions</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean hasClosedCaptions(); </span> </td> 
   <td colname="3"> True if closed-caption tracks are available. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt;ClosedCaptionsTrack&gt; getClosedCationsTracks(); </span> </td> 
   <td colname="3"> Provides a list of available closed-caption tracks. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> ClosedCaptionsTrack get SelectedClosedCaptionsTrack(); </span> </td> 
   <td colname="3"> Retrieves the current closed caption track selected with <span class="codeph"> SelectClosedCaptionsTrack </span>. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> selectClosedCaptionsTrack ( ClosedCaptionsTrack closedCaptionsTrack) </span> </td> 
   <td colname="3"> Sets a closed-caption track to be the current closed-caption track. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Alternate audio tracks</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean hasAlternateAudio(); </span> </td> 
   <td colname="3"> True if the stream has alternate audio tracks. <p>Note:  The main (default) audio track is also part of the alternate audio track list. </p> <p>TVSDK for Android considers the main audio track to be one of the items in the alternate audio track list. Because of this, the only case where <span class="codeph"> MediaPlayerItem.hasAlternateAudio </span> returns false is when the stream has no audio at all. If the content has only one audio track, this method returns true, and <span class="codeph"> MediaPlayerItem.getAudioTracks </span> returns a list with a single element (the default audio track). </p> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt;AudioTrack&gt; getAudioTracks(); </span> </td> 
   <td colname="3"> Provides a list of available alternate audio tracks. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> AudioTrack getSelectedAudioTrack(); </span> </td> 
   <td colname="3"> Retrieves the audio track selected with <span class="codeph"> selectAudioTrack </span>. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> selectAudioTrack ( AudioTrack audioTrack ) </span> </td> 
   <td colname="3"> Selects an audio track to be the current audio track. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Timed metadata</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean hasTimedMetadata(); </span> </td> 
   <td colname="3"> True if the stream has associated timed metadata. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt;TimedMetadata&gt; getTimedMetadata(); </span> </td> 
   <td colname="3"> Provides a list of the timed metadata objects associated with the stream. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Multiple profiles (bit rates)</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean isDynamic(); </span> </td> 
   <td colname="3"> True if the stream is a multiple bit rate (MBR) stream. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt;Profile&gt; getProfiles(); </span> </td> 
   <td colname="3"> Provides a list of the associated bit rate profiles. For each profile, you can retrieve its bit rate and the height and width of the profile. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> Profile getSelectedProfile() </span> </td> 
   <td colname="3"> Retrieves the currently selected profile. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Trick play</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> boolean isTrickPlaySupported(); </span> </td> 
   <td colname="3"> True if the player supports fast forward, rewind, and resume. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> List&lt; Float&gt; getAvailablePlaybackRates() </span> </td> 
   <td colname="3"> Provides the list of available playback rates in the context of the trick-play feature. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> Float getSelectedPlaybackRate() </span> </td> 
   <td colname="3"> Retrieves the currently selected playback rate. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> MediaPlayerItemConfig getConfig() </span> </td> 
   <td colname="3"> Returns the <span class="codeph"> MediaPlayerItemConfig </span> instance associated with this item. </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <b>Media resource</b> </td> 
   <td colname="3"> </td> 
  </tr> 
  <tr rowsep="1"> 
   <td colname="2"> <span class="codeph"> MediaResource getResource(); </span> </td> 
   <td colname="3"> Returns the media resource associated with this item. </td> 
  </tr> 
  <tr rowsep="0"> 
   <td colname="2"> <span class="codeph"> int getResourceId() </span> </td> 
   <td colname="3"> Returns the media identifier associated with this item. This ID is set when the item is loaded using <span class="codeph"> MediaPlayerItemLoader.load </span>. </td> 
  </tr> 
 </tbody> 
</table>
