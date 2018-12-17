---
description: To allow the ad resolver to work, ad providers, such as Adobe Primetime ad decisioning, require configuration values to enable your connection to the provider.
seo-description: To allow the ad resolver to work, ad providers, such as Adobe Primetime ad decisioning, require configuration values to enable your connection to the provider.
seo-title: Ad insertion metadata
title: Ad insertion metadata
uuid: 44c9aeb4-a41d-4af6-8b2f-23d184eb37d8
index: y
internal: n
snippet: y
---

# Ad insertion metadata{#ad-insertion-metadata}

To allow the ad resolver to work, ad providers, such as Adobe Primetime ad decisioning, require configuration values to enable your connection to the provider.

Browser TVSDK includes the Adobe Primetime ad decisioning library. For your content to include advertising from the Adobe Primetime ad decisioning server, your application must provide the following required AudidtudeSettings information:

* `mediaID`, which is a unique identifier for the video to be played.

  The publisher assigns the mediaID when submitting video content and ad information to the Adobe Primetime ad decisioning server. This ID is used by Adobe Primetime ad decisioning to retrieve related advertising information for the video from the server. 

* (Optional) `defaultMediaId`, which specifies the ads that are served when the following conditions are met:

    * Your request to the ad server is invalid, or the content is incorrectly configured. 
    * Adobe Primetime ad decisioning is experiencing delays in propagating the data. 
    * One of the Adobe Primetime ad decisioning back-end processes is malfunctioning or is unavailable.

  >[!TIP]
  >
  >Adobe recommends using `defaultMediaId`.

* Your `zoneID`, which is assigned by Adobe, identifies your company or website. 
* The domain of your assigned ad server. 
* Other targeting parameters.

  You can include these parameters depending on your needs and the needs of the ad provider.

