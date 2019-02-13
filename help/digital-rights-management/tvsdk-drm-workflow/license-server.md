---
seo-title: Primetime DRM license server
title: Primetime DRM license server
uuid: 5be34572-327f-47ff-8b24-17b18f2e258b
---

# Primetime DRM license server {#primetime-drm-license-server}

The Primetime DRM license server is built from the Primetime DRM Java SDK. This server consumes license requests from clients requesting access to protected content. The server has the ability to parse and manipulate the DRM Policy from within the license request, in order to modify or override the policy before using the policy to generate a license for the requesting client.

In order to deploy a Primetime DRM license server, it must first meet **Adobe's Compliance and Robustness rules** for Primetime DRM. Adobe also offers a hosted Primetime DRM licensing service called [Primetime Cloud DRM](../cloud-quick-start/whats-included.md), that you can use as an alternative to hosting your own license server. 
