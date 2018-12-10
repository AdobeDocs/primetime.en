---
description: You can select the following encryption options when you create a package. However, you cannot modify the encryption options during license acquisition 
seo-description: You can select the following encryption options when you create a package. However, you cannot modify the encryption options during license acquisition 
seo-title: Key Rotation
title: Key Rotation
uuid: 1dbbc9a1-8703-4804-b9d1-918645fe7621
index: y
internal: n
snippet: y
---

# Key Rotation{#key-rotation}

You can select the following encryption options when you create a package. However, you cannot modify the encryption options during license acquisition:

During packaging, content is typically encrypted using the Content Encryption Key (CEK). The client obtains a license containing the CEK to consume the content.

When you enable key rotation, the Rotation Key is used to encrypt the content, and the key can be changed so that each Rotation Key is only used to encrypt a portion of the content. The Rotation Keys are protected using the Content Encryption Key, and the client still obtains a single license containing the CEK to consume the content.

The packager implementation can control the Content Encryption Key and Rotation Keys used, as well as the frequency with which the Rotation Keys change.

>[!NOTE]
>
>Content packaged using key rotation can only be played on Primetime DRM clients version 3.0 or later. Older clients may need to upgrade to play this content.

