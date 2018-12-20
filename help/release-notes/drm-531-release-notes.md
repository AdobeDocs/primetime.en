---
title: DRM 5.3.1 Release Notes
seo-title: DRM 5.3.1 Release Notes
description: DRM 5.3.1 Release Notes describe the new features and the known issues in DRM 5.3.1.
seo-description: DRM 5.3.1 Release Notes describe the new features and the known issues in DRM 5.3.1.
uuid: bb61b79f-a5b3-42ed-8016-495b1ac99ea6
contentOwner: dekalra
topic-tags: release-notes
products: SG_PRIMETIME
discoiquuid: b8d4f463-b2ee-4855-9417-2749cbd1640b
index: y
internal: n
snippet: y
---

# DRM 5.3.1 Release Notes{#drm-release-notes}

DRM 5.3.1 Release Notes describe the new features and the known issues in DRM 5.3.1.

## New Features {#new-features}

#### Version 5.3 {#version}

* **Secure Stop - **You can specify whether playback stops or continues at the end of a playback window.
* **Resolution Based Output Protection (RBOP) - **You can specify the output constraints based on pixel resolutions.
* **CDM Gating - **In order to support HTML5, Adobe has updated the Reference Implementation license server included with the Adobe Primetime DRM (formerly Adobe Access DRM) Java SDK to be able to consume all DRM protocol messages at a single URL endpoint. This consolidation of HTTP URL methods is necessary in order to comply with the HTML5 EME (Encrypted Media Extension) specification that is in turn required to be implemented by CDM (Content Decryption Module) DRM vendors. Previously, these were the only URL endpoints exposed by the Reference Implementation license server:

    * /flashaccess/i15n/v3 (Individualization)
    * /flashaccess/license/v5 (License Request)
    * /flashaccess/licenseRet/v5 (License Return)
    * /flashaccess/getServerVersion/v5 (Get Server Version)

Now, all requests (originating from an HTML5 CDM) can be directed to a single endpoint: /req

This change is backwards-compatible with non-CDM platforms, such as Flash Player, Android, iOS.

* **RBOP downscaling - **Specific to the HTML5 space, RBOP contains automatic downscaling capability, where if a bitrate that exceeds the allowable bitrate specified in the DRM policy, the content will be downscaled to the max allowable resolution. For example, if a 1080p stream is streamed to a client that is displaying the content on a non-HDCP compliant monitor, the DRM policy may indicate that the max resolution should be 720p. Primetime DRM will decode the 1080p stream and then downscale it to 720p before rendering it onscreen. If the browser playing the video is then dragged over to a monitor that does support HDCP, Primetime DRM will then stop downscaling the content and allow it to play back at 1080.

## Known Issues {#known-issues}

#### Version 5.3 {#version-1}

* `Hasher.bat (flashaccess-hasher.jar)` outputs log messages to `flashaccess-global.log.`You must ensure that the `flashaccess-global.log` file is in the same directory with Hasher.bat.

* The output of some of the `toJSON()`calls return `Strings` that are not fully JSON compliant or fully compliant in a stand alone manner (i.e., without composition of JSON structures).

* Xbox key server accepts key requests that have the version value not equal to 1.

The Xbox key server should only support key requests that have the version equal to 1, but currently, the server accepts key requests where the version is not 1.

* Xbox key server doesn't validate a policy correctly.

The Xbox key server should not accept policies that are outside of the validity date, but currently, the server accepts them regardless.

* Xbox key server should reject a key request which contains a metadata that was created with wrong packager cert.
* Returned value of some JSON structures are not formatted correctly for Resolution based Output Protection related classes.

Several classes implement a toJSON() method that should return a JSON compliant representation of that object as a String, but currently the returned value is not fully JSON compliant.
