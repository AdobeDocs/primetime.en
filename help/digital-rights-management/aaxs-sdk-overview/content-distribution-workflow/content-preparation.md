---
description: Any use of Adobe Access consists of two key steps at different points of the workflow. Content preparation must be done once per asset, and results in creating protected content. Content acquisition is done multiple times, once for every consumer that wants to watch that protected asset.
title: Content preparation
exl-id: c658c7e9-2583-4d74-a94b-800023cf5196
---
# Content preparation {#content-preparation}

Any use of Adobe Access consists of two key steps at different points of the workflow. Content preparation must be done once per asset, and results in creating protected content. Content acquisition is done multiple times, once for every consumer that wants to watch that protected asset.

Before making content available for distribution, you must first encode the content in the FLV or F4V video format, create one or more policies specifying usage rules for the content, and package the content using Adobe Access SDK.

The steps to encode, package, and distribute content are as follows: 

1. Encode the content in the FLV or F4V format using encoding tools available from Adobe or from third parties.
1. Create policies specifying the usage rules under which consumers can view the content.

   A policy is the container for the rules and restrictions that determine how, when, and where protected content can be viewed by consumers.

   The packager requires at least one policy with at least one usage rule. You can override the usage rule, and add additional usage rules, when the License Server generates the license. 

1. Package the content and specify what policies to apply.

   Adobe Access SDK encrypts the content using a Content Encryption Key (CEK), and binds one or more policies to the content. The result is a *protected content file *that can only be played by a consumer who has obtained a license from the corresponding License Server.

   During packaging, the content is encrypted using the CEK. The CEK is encrypted using the License Server public key and included in the DRM metadata along with the policies. The DRM metadata is signed using the Packager private key, and the metadata is included in the protected content. 

1. Make the protected content available for distribution to consumers.

   The protected content is typically distributed using a content distribution network (CDN). The CDN can use any mechanism supported by the client runtime, such as Flash Media Server, Adobe HTTP Dynamic Streaming for multiple bitrate streaming, or an HTTP Web Server for progressive download.
