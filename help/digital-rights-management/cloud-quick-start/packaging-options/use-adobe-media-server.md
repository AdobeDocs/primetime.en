---
seo-title: Use Adobe Media Server
title: Use Adobe Media Server
uuid: c7a7246d-b1ec-4760-90d6-fadfeefe3b4c
index: y
internal: n
snippet: y
---

# Use Adobe Media Server{#use-adobe-media-server}

Some customers may already be using Adobe Media Server and want to maintain that content delivery model. If this is the case, the required Primetime Cloud DRM-specific data can be harvested from either of the configuration files included in this kit to populate the JIT (Just In Time) XML configuration for AMS.

For example:

```xml
<?xml version="1.0"?>
<Application>
  <HDS>
    <HLS>
      <Encryption enabled="true" protection-scheme="AdobeAccessV4">
        <AdobeAccessV4>
          <ContentID>SampleVideo</ContentID>
          <CommonKeyPath>common-key.bin</CommonKeyPath>
          <LicenseServerURL>
            http://access.adobeprimetime.com/flashaccessserver/axs_prod
          </LicenseServerURL>
          <KeyServerURL>
            https://access.adobeprimetime.com:443/faxsks/axs_prod/key
          </KeyServerURL>
          <TransportCertPath>cert/Cloud DRM-transport.cer</TransportCertPath>
          <LicenseServerCertPath>cert/Cloud DRM-license.cer</LicenseServerCertPath>
          <PackagerCredentialPath>cert-from-adobe.pfx</PackagerCredentialPath>
          <PackagerCredentialPwd>pass-for-cert-from-adobe</PackagerCredentialPwd>
          <PolicyPath>policy_ios_localkeyserver.pol</PolicyPath>
        </AdobeAccessV4>
      </Encryption>
    </HLS>
  </HDS>
</Application>
```

