---
seo-title: Examining encrypted file content
title: Examining encrypted file content
uuid: 34e079a0-d62b-4ebf-b762-ac68b57f979b
index: y
internal: n
snippet: y
---

# Examining encrypted file content{#examining-encrypted-file-content}

You can examine the contents of an encrypted media file using using the Java API.

To examine encrypted file content:

1. Set up your development environment and include all of the JAR files. See *Setting up the SDK* for your project. 
1. Create a `MediaEncrypter` instance. 
1. Pass the encrypted file to the `MediaEncrypter.examineEncryptedContent` method, which returns a `KeyMetaData` object. 

1. Inspect the information within the `KeyMetaData` object.

For sample code that describes how to extract DRM metadata from an encrypted file, see `com.adobe.flashaccess.samples.mediapackager.ExamineContent` in the Reference Implementation Command Line Tools [!DNL samples/] directory. 
