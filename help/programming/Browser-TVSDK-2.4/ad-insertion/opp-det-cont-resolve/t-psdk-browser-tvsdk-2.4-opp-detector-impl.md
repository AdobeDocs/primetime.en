---
description: You can implement your own opportunity generator by extending the OpportunityGenerator interface.
seo-description: You can implement your own opportunity generator by extending the OpportunityGenerator interface.
seo-title: Implement a custom opportunity generator
title: Implement a custom opportunity generator
uuid: 9e2d4043-4945-4274-91c4-dbe4a9144560
index: y
internal: n
snippet: y
---

# Implement a custom opportunity generator{#implement-a-custom-opportunity-generator}

You can implement your own opportunity generator by extending the OpportunityGenerator interface.

1. Create the custom opportunity generator.

   For example: 

   ```js
   /** 
   * Class implementing AdobePSDK.OpportunityGenerator interface 
   */ 
   CustomOpportunityGenerator = function () { 
   }; 
    
   CustomOpportunityGenerator.prototype = { 
       constructor: CustomOpportunityGenerator, 
       configureCallbackFunc: function (item, client, mode, playhead, playbackRange) {  
           // the playhead represents the initial playback position 
           // the playback range represents the initial playback range 
             
           // the item property indicates the current AdobePSDK.MediaPlayerItem associated with this generator 
           // the initial set of timed metadata can be obtain through the item property 
           var timedMetadatas = item.timedMetadata; 
       }, 
       updateCallbackFunc: function (playhead, playbackRange) { 
           // when an opportunity is created by this generator 
           // we need to notify the TVSDK through the client property 
           client.resolve (opportunity); 
       }, 
       … 
   }; 
   
   ```

1. Create the custom content factory, which uses the custom opportunity generator.

   For example: 

   ```js
   /** 
     * Class implementing AdobePSDK.ContentFactory interface 
   */ 
   CustomContentFactory = function () { 
   }; 
    
   CustomContentFactory.prototype = { 
          constructor: CustomContentFactory, 
          retrieveOpportunityGeneratorsCallbackFunc: function (item) { 
               var result = []; 
               result.push (new CustomOpportunityGenerator()); 
               return result; 
       }, 
       … 
   }; 
   
   ```

1. Register the custom content factory for the media stream to be played.

   In UI Framework player, you can specify custom content factory as follows: 

   ```js
   var advertisingFactory = new CustomContentFactory(); 
   var playerWrapper = ptp.videoPlayer('.videoDiv', { 
    player: { 
           mediaPlayerItemConfig: { 
                   advertisingFactory: advertisingFactory 
           }, 
               mediaResource: { 
                   resourceUrl:'Specify Resource Url' 
          } 
     } 
   }); 
   
   ```

