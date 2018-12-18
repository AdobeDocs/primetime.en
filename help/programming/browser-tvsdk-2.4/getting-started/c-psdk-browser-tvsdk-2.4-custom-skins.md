---
description: To use the custom skins, you must write the customization similar to default-video-controls.css and refer to this new customization in the player.
seo-description: To use the custom skins, you must write the customization similar to default-video-controls.css and refer to this new customization in the player.
seo-title: Custom skins
title: Custom skins
uuid: bc71926e-0dec-4628-8248-911224a7a6c2
index: y
internal: n
snippet: y
---

# Custom skins{#custom-skins}

To use the custom skins, you must write the customization similar to default-video-controls.css and refer to this new customization in the player.

For example, you can use one of the following options:

* `<link rel="stylesheet" href="css/common_style.css">` 
* `<link rel="stylesheet" href="css/custom-video-controls1.css">`

You can make the following types of changes:

* Foreground color of buttons and text

  All the controls which have a foreground are using the `vid-skin-fgcolor` class. To change the foreground of all the controls, iterate through all the elements with the `vid-skin-fgcolor` class and specify the desired color. 
* Background color of buttons and text

  All the controls that have a foreground are using the `vid-skin-bgcolor` class. To change the foreground of all the controls, iterate through all the elements with `vid-skin-bgcolor` class and specify the desired color. 
* Shape of play head

  The play head can be square or round. To change the play head, add `square` or `round` class to `playhead` element. 
* Style of the buffering spinners

  The reference player provides the following styles of spinners can be displayed as the player buffers content:

    * Overlay-text ( `overlay-text`) 
    * Rectangular Spinner ( `spinner`) 
    * Signal ( `signal`) 
    * Vertical Bars ( `vertical`)     
    
      >[!TIP]
      >
      >To use any of the buffering spinners, you must add the class in the buffering-overlay element. For example, to use `overlay-text`, add the following lines in the `BufferOverlay.js` file:       >
      >
      >```js      >
      >var overlay = document.getElementById("buffering-overlay"); 
      >overlay.classList.add ("spinner");
      >```      >
      >

