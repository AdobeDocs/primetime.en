---
seo-title: Examining encrypted file content
title: Examining encrypted file content
uuid: 2132fac7-5f11-4308-b511-ed4f216527a6
---

# Examining encrypted file content {#examining-encrypted-file-content}

To examine the contents of an FLV or an F4V file by using the Java API, perform the following steps:

1. Set up your development environment and include all of the JAR files mentioned in [Setting up the development environment](../../aaxs-protecting-content/content-setting-up-the-sdk/content-setting-up-the-dev-env.md) within your project. 
1. Create a `MediaEncrypter` instance. 
1. Pass the encrypted file to the `MediaEncrypter.examineEncryptedContent` method, which returns a `KeyMetaData` object. 
1. Inspect the information within the `KeyMetaData` object.

For sample code demonstrating how to extract DRM metadata from an encrypted file, see `com.adobe.flashaccess.samples.mediapackager.ExamineContent` in the Reference Implementation Command Line Tools “samples” directory. 
