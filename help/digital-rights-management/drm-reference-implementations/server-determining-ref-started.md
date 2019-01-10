---
description: null
seo-description: null
seo-title: Check whether the license server started properly
title: Check whether the license server started properly
uuid: a6a034c9-b3c4-4e26-b901-d2c132c00c52
index: y
internal: n
snippet: y
---

# Check whether the license server started properly{#check-whether-the-license-server-started-properly}

 There are several ways to determine whether your Reference Implementation License Server has started correctly. One way is to check the [!DNL catalina.log] logs, but this may not be sufficient, as the license server logs to its own log files. 
1. Check your [!DNL AdobeFlashAccess.log] file.

   This is where the Reference Implementation license server writes log information. The location of this log file is indicated by your [!DNL log4j.xml] file and can be modified to point to any location. By default, the log file is copied to the working directory where you run your `catalina` Tomcat script.
1. Go to the following URL, and verify that the text "License Server is setup correctly" is displayed:

[!DNL http://localhost:8080/flashaccess/license/v4]
