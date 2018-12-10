---
description: To play the DASH content resulting from content packaging, the TVSDK client will need to obtain the content decryption key that was passed during the packaging process in the key acquisition workflow. The client content decryption key is typically delivered to the client by a Widevine/PlayReady license server in response to one or more HTTP/HTTPS posts from the client.
seo-description: To play the DASH content resulting from content packaging, the TVSDK client will need to obtain the content decryption key that was passed during the packaging process in the key acquisition workflow. The client content decryption key is typically delivered to the client by a Widevine/PlayReady license server in response to one or more HTTP/HTTPS posts from the client.
seo-title: Client Key Request workflow overview
title: Client Key Request workflow overview
uuid: 4198804a-2e2e-4f33-8ca7-e1602cbff1e3
index: y
internal: n
snippet: y
---

# Client Key Request workflow overview{#client-key-request-workflow-overview}

To play the DASH content resulting from content packaging, the TVSDK client will need to obtain the content decryption key that was passed during the packaging process in the key acquisition workflow. The client content decryption key is typically delivered to the client by a Widevine/PlayReady license server in response to one or more HTTP/HTTPS posts from the client.

To acquire the content decryption key, the PSDK client must do the following

* Grab the content's pssh box, give it to the platform, and obtain in response a key request. 
* Send the key request out to the appropriate Widevine/PlayReady license server through an HTTP POST. 
* Pass the server's response to the platform which will extract the client content decryption key from the response and use it for content decryption.

To send out the HTTP POST for the key request, your code must pass to the PSDK client the license server URL along with any extra data that needs to be attached to the post. The choice of URL and data to pass depends the Widevine/PlayReady service provider you work with. For example, if you use ExpressPlay for providing the service, you pass in the appropriate ExpressPlay Widevine/PlayReady license server URL and attach to the outgoing key request the ExpressPlay token associated with the content's encryption key. You can get the appropriate ExpressPlay Widevine/PlayReady license server URL from the ExpressPlay documentation. 
