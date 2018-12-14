---
description: 302 redirect optimization minimizes the number of 302 redirect responses, which allows your application to load balance more effectively.
seo-description: 302 redirect optimization minimizes the number of 302 redirect responses, which allows your application to load balance more effectively.
seo-title: Disable or enable 302 redirect optimization
title: Disable or enable 302 redirect optimization
uuid: 653e76ea-316b-4e0a-b419-aa74f01fcc78
index: y
internal: n
snippet: y
---

# Disable or enable 302 redirect optimization{#disable-or-enable-redirect-optimization}

302 redirect optimization minimizes the number of 302 redirect responses, which allows your application to load balance more effectively.

<a id="example_B886777252B745AAB48B1FCC42C97A25"></a>

If a main manifest request is redirected, and 302 optimization is enabled in your player, subsequent requests made for assets from that manifest will use the final domain location, which avoids additional 302 responses.

This feature is enabled by default, and you can change this setting.

Use the `useRedirectedUrl` property to turn 302 redirect on (true) or off (false). 
For example: 

```java
// Set useRedirectedUrl property to false 
NetworkConfiguration networkConfiguration = new NetworkConfiguration(); 
networkConfiguration.setUseRedirectedUrl(false); 
 
//Set NetworkConfiguration as Metadata: 
MetadataNode resourceMetadata = new MetadataNode();  
resourceMetadata.setNode(DefaultMetadataKeys.NETWORK_CONFIGURATION.getValue(),  
                         networkConfiguration); 
 
//Call MediaResource.createFromURL to set the metadata: 
MediaResource resource = MediaResource.createFromURL(url, resourceMetadata); 
  
//Load the resource 
mediaPlayer.replaceCurrentItem(resource);
```
