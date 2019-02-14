---
seo-title: Configuration Validator
title: Configuration Validator
uuid: 60ebd35c-290a-4f08-9bd0-178903857149
---

# Configuration Validator {#configuration-validator}

Adobe recommends running the Configuration Validator utility before starting the server any time changes are made to the configuration file. This utility can detect most configuration errors early, before they cause failures during request processing.

To run the validator, use the command:

```
Validator.bat options  
```

or the command:

```
java -jar libs/flashaccess-validator.jar options 
```

For each of the license server configuration files, the Validator can perform file-based validation, which ensures the XML file is well-formed and conforms to the configuration file schema. To perform file-based validation on the global configuration file, run the command:

```
Validator --file path/flashaccess-global.xml --global
```

To perform file-based validation on the tenant configuration file, run the command:

```
Validator --file path/flashaccess-tenant.xml --tenant
```

The Validator can also perform deployment-based validation; in addition to checking conformity with the schema, this level of validation also checks that the values specified are valid (for example, it ensures that referenced files exist). Deployment-based validation can be performed at two levels:

* Tenant — Validates configuration file and credentials for a specific tenant. To validate the configuration for "tenant1", run the command:

```
Validator --root-path-to-LicenseServer.ConfigRoot -d flashaccessserver/tenant1 -t 
```

* Global — Validates the global configuration file and tenant validation for all tenants. To perform global deployment-based validation, run the command:

```
Validator --root-path-to-LicenseServer.ConfigRoot -g 
```

