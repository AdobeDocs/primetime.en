---
description: You can create a Browserify-compatible player using JS files provided by the Browser TVSDK.
seo-description: You can create a Browserify-compatible player using JS files provided by the Browser TVSDK.
seo-title: Browserify-compatible player
title: Browserify-compatible player
uuid: 1832c826-d5d0-41b0-852f-286c8e4fa0f3
---

# Overview {#browserify-compatible-player-overview}

You can create a Browserify-compatible player using JS files provided by the Browser TVSDK.

Browser TVSDK provides two Browserify-compatible JS files. One is for use with the AdobePSDK module; this is for developing apps without the UI-Framework. The other is for use with the UI-Framework module; it returns the PTP namespace you use for writing apps using the UI-Framework.

To get started with Browserify, run the following setup commands to create [!DNL final.js] files (your Browserify bundle file) inside the [!DNL example] directories under [!DNL samples/browerify/reference] and [!DNL samples/browerify/ui-framework]:

1. Navigate to [!DNL samples/browserify/reference/build]. 
1. Run the following commands:

    1. [!DNL npm install] 
    1. [!DNL node_modules/.bin/grunt]

1. Navigate to [!DNL samples/browserify/ui-framework/build]. 
1. Run the same commands as in Step 2.

With this setup done, you can proceed to create Browserify-compatible TVSDK apps based on the samples provided with the TVSDK. 
