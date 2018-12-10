---
seo-title: Monitoring
title: Monitoring
uuid: dd8880f1-3aa4-45e3-9cd2-6655b8aa8f8f
index: y
internal: n
snippet: y
---

# Monitoring{#monitoring}

The Individualization server and Key Generation server each have a status page, which you can use to determine the health of the servers.

* **Individualization status page:** [!DNL http://[SERVER:PORT]/flashaccess/status]

    * Reports “Alive” if the app server is running and the app can make a GET request to the Key Generation server 
    * The page reports either “Alive” or nothing. No info about the application is revealed, so this page could be used for monitoring from outside the firewall.

* **Key Generation status page:** [!DNL http://[SERVER:PORT]/flashaccess-kgs/status]

    * Reports "Alive" if the app server is running 
    * All Key Generation URLs must only be accessible internally

* **Individualization Statistics page:** [!DNL http://[SERVER:PORT]/flashaccess/admin/appstats]

    * Includes statistics about the Individualization server, such as number of requests served and the number of keys available in the cache 
    * This page must only be accessible internally

* **Key Generation Statistics page:** [!DNL http://[SERVER:PORT]/flashaccess-kgs/appstats]

    * Includes statistics about the Key Generation server, such as the number of requests served and the number of key files available on disk 
    * All Key Generation URLs must only be accessible internally

