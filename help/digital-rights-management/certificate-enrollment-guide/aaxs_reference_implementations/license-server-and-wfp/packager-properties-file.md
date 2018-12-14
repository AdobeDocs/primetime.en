---
seo-title: Packager properties file
title: Packager properties file
uuid: e24b6169-7b7e-4535-a295-ec772441bed6
index: y
internal: n
snippet: y
---

# Packager properties file{#packager-properties-file}

Use the [!DNL flashaccess-refimpl-packager.properties] file to configure the Watched Folder Packager component of the reference implementation. At a minimum, be sure to set the license server URL, license server certificate, packager credential, and key protection options. This file also contains the location of each watched folder (packager.watchfolder.source. `n`). Any changes made to the values in this property file will take effect the next time the watched folder packager runs (restarting the server is not required). However, if there is a configuration error in the packager, the watched folder packager thread will exit, and the server will need to be restarted to restart the packager thread. 