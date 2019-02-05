---
seo-title: Using Output Protection Policies
title: Using Output Protection Policies
uuid: f00d2a97-0036-41a6-ab44-391cc40b146e
---

# Using Output Protection Policies{#using-output-protection-policies}

**Widevine output protection policies**

Widevine natively supports both analog and digital output protection restrictions. Refer to the documenation from your Widevine service provider on how to attach these policies to generated licenses.

If you use Expressplay as the Widevine service provider, then attach digital output protection policies at token generation time through the hdcpOutputControl flag: 
Allowed values are 0, 1, 2 where 0 = HDCP_NONE, 1 = HDCP_V1, 2 = HDCP_V2. Both HDCP_V1 and HDCP_V2 enforce HDCP version 1.X and 2.X respectively.

Expressplay currently does not support attaching analog output restrictions

**PlayReady output protection policies**

PlayReady also natively supports both analog and digital output protection restrictions. The output protection level values that you can set. The page [Output Protection Levels](https://msdn.microsoft.com/en-us/library/dn468831.aspx) documents the values that you can set and their expected client behavior.

If you use Expressplay, then attach output protection level values at token generation time via the compressedDigitalAudioOPL, uncompressedDigitalAudioOPL, compressedDigitalVideoOPL, uncompressedDigitalVideoOPL, and the unknownOutputBehavior flag. These are documented at [PlayReady License Token Request](https://www.expressplay.com/developer/restapi/#playready-license-token-request) 
