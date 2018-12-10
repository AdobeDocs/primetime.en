---
description: You can configure the reference implementation with the Sun PKCS#11 provider that supports HSM. Although the use of an HSM is not required, it is recommended.
seo-description: You can configure the reference implementation with the Sun PKCS#11 provider that supports HSM. Although the use of an HSM is not required, it is recommended.
seo-title: HSM configuration
title: HSM configuration
uuid: b53b8158-c4f2-4153-a701-b7a2cd8ca78c
index: y
internal: n
snippet: y
---

# HSM configuration{#hsm-configuration}

You can configure the reference implementation with the Sun PKCS#11 provider that supports HSM. Although the use of an HSM is not required, it is recommended.

To use a credential on an HSM, you must create a configuration file for the Sun PKCS#11 provider. For more information, see the [Java PCKS#11 Reference Guide](http://docs.oracle.com/javase/1.5.0/docs/guide/security/p11guide.html).

To verify that your HSM and Sun PKCS#11 configuration file are configured, type the following command by using the keytool that was installed with the Java JDK:

```
keytool -keystore NONE -storetype PKCS11 -providerClass sun.security.pkcs11.SunPKCS11 
  -providerArg pkcs11.cfg -list
```

You have configured the HSM correctly if you can view your credentials in the list.

>[!NOTE] {class="- topic/note "}
>
>As of Java 1.7, 64-bit Sun Java for Windows no longer supports the PKCS#11 interfaces that Adobe Primetime DRM requires to communicate with HSM devices. If you plan to use an HSM, ensure that you use a 32-bit version of Java or use a JDK that supports the full PKCS#11 interfaces.

