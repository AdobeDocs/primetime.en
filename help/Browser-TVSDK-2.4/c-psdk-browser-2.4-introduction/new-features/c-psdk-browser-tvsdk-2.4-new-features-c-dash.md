---
description: Browser TVSDK supports a number of DASH features that you can implement to add functionality to your video applications.
seo-description: Browser TVSDK supports a number of DASH features that you can implement to add functionality to your video applications.
seo-title: Supported DASH features
title: Supported DASH features
uuid: 80127c14-953b-4522-95ec-8e6ceff6175c
index: y
internal: n
snippet: y
---

# Supported DASH features{#supported-dash-features}

Browser TVSDK supports a number of DASH features that you can implement to add functionality to your video applications.

* [DASH Core playback features](../../c-psdk-browser-2.4-introduction/new-features/c-psdk-browser-tvsdk-2.4-new-features-c-dash.md#table_frb_p2g_xx) 
* [DASH Advanced playback features](../../c-psdk-browser-2.4-introduction/new-features/c-psdk-browser-tvsdk-2.4-new-features-c-dash.md#table_grb_p2g_xx) 
* [DASH Content protection features](../../c-psdk-browser-2.4-introduction/new-features/c-psdk-browser-tvsdk-2.4-new-features-c-dash.md#table_hrb_p2g_xx) 
* [DASH Core ad insertion features](../../c-psdk-browser-2.4-introduction/new-features/c-psdk-browser-tvsdk-2.4-new-features-c-dash.md#table_jrb_p2g_xx) 
* [DASH Advanced ad insertion features](../../c-psdk-browser-2.4-introduction/new-features/c-psdk-browser-tvsdk-2.4-new-features-c-dash.md#table_krb_p2g_xx) 
* [DASH Integrations](../../c-psdk-browser-2.4-introduction/new-features/c-psdk-browser-tvsdk-2.4-new-features-c-dash.md#table_lrb_p2g_xx)

>[!TIP]
>
>In the feature matrix tables below,  ![](assets/supported15.png)>
>means that the feature is supported in the current release.

<a id="section_erb_p2g_xx"></a>

The following features are supported: 

<!-- 

<table id="table_lrb_p2g_xx"> 
 <title>DASH integrations</title> 
 <tgroup cols="4"> 
  <colspec colnum="1" colname="col1" colwidth="*" /> 
  <colspec colnum="2" colname="col2" colwidth="*" /> 
  <colspec colnum="3" colname="col3" colwidth="*" /> 
  <colspec colnum="4" colname="col6" colwidth="*" /> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Category </th> 
    <th colname="col2" class="entry"> Content type </th> 
    <th colname="col3" class="entry"> Feature </th> 
    <th colname="col6" align="center" class="entry"> 
     <lines>
       HTML5 FF, IE, Chrome, Android Chrome
     </lines> </th> 
   </tr> 
  </thead> 
  <tbody> 
   <tr> 
    <td colname="col1"> Integrations </td> 
    <td colname="col2"> VOD + Live </td> 
    <td colname="col3"> Adobe Analytics VHL integration </td> 
    <td colname="col6" valign="middle" align="center"><img href="assets/supported15.png" id="image_14D9248BD1D8410E83AD27DB4AB3B6ED" /> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> Integrations </td> 
    <td colname="col2"> VOD + Live </td> 
    <td colname="col3"> Nielsen support </td> 
    <td colname="col6" valign="middle" align="center"><img href="assets/supported15.png" id="image_EFA853CB763446B3B37F2CF6BCC53EE1" /> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> Integrations </td> 
    <td colname="col2"> VOD + Live </td> 
    <td colname="col3"> Billing </td> 
    <td colname="col6" valign="middle" align="center"><img href="assets/supported15.png" id="image_B3A4E5937CEC4052977C08767219BC2B" /> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> Integrations </td> 
    <td colname="col2"> VOD + Live </td> 
    <td colname="col3"> Browserify </td> 
    <td colname="col6" valign="middle" align="center"><img href="assets/supported15.png" id="image_3330E81B86C84AD391AEBFDFE911A47F" /> </td> 
   </tr> 
  </tbody> 
 </tgroup> 
</table>

 -->

#### DASH integrations
|  Category  | Content type  | Feature  |   |
|---|---|---|---|
|  Integrations  | VOD + Live  | Adobe Analytics VHL integration  | ![](assets/supported15.png)

|
|  Integrations  | VOD + Live  | Billing  | ![](assets/supported15.png)

|
|  Integrations  | VOD + Live  | Browserify  | ![](assets/supported15.png)

|

#### DASH advanced ad insertion features (CSAI)
|  Category  | Content type  | Feature  |   |
|---|---|---|---|
|  Ad Insertion  | VOD  | Ad only  | Not Supported  |
|  Ad Insertion  | VOD  | Targeting parameters  | VOD only  |
|  Ad Insertion  | VOD  | Custom Parameters  | VOD only  |
|  Ad Insertion  | VOD + Live  | Custom ad policy  | Not Supported  |
|  Ad Insertion  | VOD + Live  | Lazy ad loading  | Not Supported  |
|  Ad Insertion  | VOD  | Companion ads, banner ads, and clickable ads  | Not Supported  |
|  Ad Insertion  | VOD  | VPAID 2.0  | Not Supported  |

#### DASH core ad insertion features (CSAI)
|  Category  | Content type  | Feature  |   |
|---|---|---|---|
|  Ad Insertion  | VOD + Live  | Pre-roll  | VOD only  |
|  Ad Insertion  | VOD + Live  | Mid-roll  | VOD only  |
|  Ad Insertion  | VOD + Live  | Post-roll  | VOD only  |
|  Ad Insertion  | FER VOD  | Ad Resolution and Behaviors  | Not Supported  |
|  Ad Insertion  | VOD + Live  | Default ad policy  | VOD only  |
|  Ad Insertion  | VOD + Live  | VAST 2.0/3.0  | VOD only  |
|  Ad Insertion  | VOD + Live  | VMAP 1.0  | VOD only  |
|  Ad Insertion  | VOD + Live  | CRS v3.1  | VOD only  |

#### DASH content protection features
<table id="table_hrb_p2g_xx">  
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Category </th> 
   <th colname="col2" class="entry"> Content type </th> 
   <th colname="col3" class="entry"> Feature </th> 
   <th colname="col6" align="center" class="entry"> 
    <lines>
      HTML5 FF, IE, Chrome, Android Chrome
    </lines> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Content Protection </td> 
   <td colname="col2"> VOD + Live </td> 
   <td colname="col3"> AES-128 </td> 
   <td colname="col6" valign="middle" align="center"> Not Supported </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Content Protection </td> 
   <td colname="col2"> VOD + Live </td> 
   <td colname="col3"> Sample-AES </td> 
   <td colname="col6" align="center" valign="middle"> Not Supported </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Content Protection </td> 
   <td colname="col2"> VOD </td> 
   <td colname="col3"> DRM </td> 
   <td colname="col6"> 
    <ul id="ul_irb_p2g_xx"> 
     <li id="li_C4643F2978BC4C8ABDB3E6C72C75A468">Widevine on 
      <ul id="ul_7047EA49AA3F40FE8F90E0ED6C028D83"> 
       <li id="li_B575735388D74D789D56BF373A470A6D">Chrome </li> 
       <li id="li_855146E4AC3A48E69B65F0022E1C0156">Firefox 47+ </li> 
       <li id="li_BC06B0A6EAAC4FC991C713775A8BB4DA">Chromecast </li> 
      </ul> </li> 
     <li id="li_D48B51C2208F423CB85D08886C2E1C66">PlayReady on Internet Explorer on Windows 8.1 and Edge </li> 
     <li id="li_2786AC19387241A296E015EE6FD07F2D">Adobe Access for Windows Firefox (video only) </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### DASH advanced playback features
|  Category  | Content type  | Feature  |   |
|---|---|---|---|
|  Playback  | VOD  | Playback at offset  | ![](assets/supported15.png)

|
|  Playback  | VOD  | Audio-only playback  | ![](assets/supported15.png)

|
|  Playback  | VOD  | Trick play  | ![](assets/supported15.png)

|
|  Playback  | VOD  | Smooth Trick Play  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | ID3 parsing  | Not Supported  |
|  Playback  | VOD  | Multi-period support  | VOD only  |
|  Playback  | VOD + Live  | Tokenized streams  | Not Supported  |
|  Playback  | VOD + Live  | Billing  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | Browserify  | ![](assets/supported15.png)

|

#### DASH core playback features
|  Category  | Content type  | Feature  |   |
|---|---|---|---|
|  Playback  | VOD + Live  | General playback (Play, Pause, Seek)  | ![](assets/supported15.png)

|
|  Playback  | FER VOD  | General playback (Play, Pause, Seek)  | Not Supported  |
|  Playback  | VOD + Live  | Adaptive bit rate  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | 608/708 captions  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | WebVTT  | VOD only  |
|  Playback  | VOD + Live  | Failover  | VOD only  |
|  Playback  | VOD + Live  | QoS and Player notifications  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | Support for cookie headers  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | Setting buffer control parameters  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | Set adaptive bit rate controls  | ![](assets/supported15.png)

|
|  Playback  | VOD + Live  | Custom tags (EventStream)  | VOD only (Inline)  |
|  Playback  | VOD + Live  | Late-binding audio  | VOD only  |
|  Playback  | VOD + Live  | 302 redirect  | VOD only  |

